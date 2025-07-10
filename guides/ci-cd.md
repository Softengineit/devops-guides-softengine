# CI/CD avec GitHub Actions

Ce guide explique comment configurer des pipelines CI/CD pour tester, construire, et déployer vos projets avec **GitHub Actions**.

## Objectifs
- **CI** : Tester et valider chaque modification (linting, tests unitaires).
- **CD** : Construire des images Docker et déployer automatiquement sur des serveurs ou stores.

## Workflow type
1. **Déclencheur** : Push ou PR sur `main` ou `dev`.
2. **Étapes CI** :
   - Checkout du code.
   - Installation des dépendances.
   - Linting (ex. : ESLint, Flake8).
   - Tests (unitaires, intégration).
3. **Étapes CD** :
   - Construction d’une image Docker.
   - Push vers GitHub Container Registry.
   - Déploiement via Ansible (serveurs) ou Fastlane (apps mobiles).

## Exemple : Workflow Node.js
```yaml
name: CI/CD Node.js
on:
  push:
    branches: [ main, dev ]
  pull_request:
    branches: [ main, dev ]

jobs:
  ci:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: '20'
      - run: npm ci
      - run: npm run lint
      - run: npm test

  build-docker:
    needs: ci
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: |
          docker login ghcr.io -u ${{ github.actor }} -p ${{ secrets.GHCR_TOKEN }}
          docker build -t ghcr.io/your-org/your-app:${{ github.sha }} .
          docker push ghcr.io/your-org/your-app:${{ github.sha }}
```

## Bonnes pratiques
- **Cachez les dépendances** : Utilisez `actions/cache` pour accélérer les builds.
- **Sécurisez les secrets** : Stockez les clés (ex. : `GHCR_TOKEN`) dans GitHub Secrets.
- **Testez localement** : Validez vos workflows avec `act` avant de pousser.
- **Modularité** : Réutilisez les workflows dans les templates (voir [templates.md](templates/templates.md)).