# Bonnes pratiques de sécurité

Ce guide détaille les pratiques pour sécuriser vos projets et pipelines.

## Gestion des secrets
- **Stockage** : Utilisez **GitHub Secrets** pour les clés API, mots de passe, et tokens (ex. : `GHCR_TOKEN`, `SSH_PRIVATE_KEY`).
- **Accès** : Limitez l’accès aux secrets aux administrateurs.
- **Exemple** :
  ```yaml
  env:
    API_KEY: ${{ secrets.API_KEY }}
  ```

## Protection des branches
- **Branches protégées** : Configurez `main` et `dev` dans GitHub (Settings > Branches > Add rule).
  - Exigez une PR approuvée.
  - Exigez des tests CI réussis.
- **Commande** :
  ```bash
  git push origin main # Doit échouer si non autorisé
  ```

## Scans de sécurité
- **Dependabot** : Activez les alertes pour les dépendances vulnérables (Settings > Security & analysis).
- **CodeQL** : Configurez l’analyse statique dans GitHub Actions pour détecter les failles.
- **Exemple** :
  ```yaml
  name: CodeQL Analysis
  on: [push, pull_request]
  jobs:
    analyze:
      runs-on: ubuntu-latest
      steps:
        - uses: github/codeql-action/init@v3
        - uses: github/codeql-action/analyze@v3
  ```

## Bonnes pratiques
- **Pas de secrets dans le code** : Vérifiez avec `git-secrets` ou similaires.
- **Environnements séparés** : Utilisez des environnements distincts (dev, staging, prod).
- **Logs** : Activez le monitoring avec Sentry ou Grafana pour tracer les anomalies.