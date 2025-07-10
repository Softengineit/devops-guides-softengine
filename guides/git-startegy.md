# Stratégie Git

Ce guide explique comment organiser les branches, commits, et pull requests (PRs) pour une collaboration fluide et un historique clair. Nous utilisons **GitFlow** comme stratégie de branchement.

## Modèle de branches
- **main** : Code stable, prêt pour la production.
- **dev** : Point d’intégration pour les nouvelles fonctionnalités.
- **feature/nom** : Pour les nouvelles fonctionnalités (ex. : `feature/add-login`).
- **bugfix/nom** : Pour corriger des bugs (ex. : `bugfix/fix-crash`).
- **hotfix/nom** : Pour des correctifs urgents en production (ex. : `hotfix/security-patch`).

## Processus
1. **Créer une branche** :
   ```bash
   git checkout dev
   git pull origin dev
   git checkout -b feature/add-login
   ```
2. **Faire des commits** (format **Conventional Commits**) :
   ```bash
   git commit -m "feat(login): add user authentication endpoint"
   ```
   Types : `feat` (nouvelle fonctionnalité), `fix` (correction), `docs` (documentation), `refactor` (refonte), `test` (tests), `chore` (maintenance).
3. **Pousser et créer une PR** :
   ```bash
   git push origin feature/add-login
   ```
   Créez une PR vers `dev` sur GitHub avec une description claire.
4. **Revue et fusion** :
   - Au moins un relecteur doit approuver la PR.
   - Résolvez les conflits avec `git rebase origin/dev` si nécessaire.
   - Fusionnez via l’interface GitHub et supprimez la branche.
5. **Préparer une release** :
   - Créez une branche `release/x.y.z` depuis `dev`.
   - Fusionnez dans `main` et `dev` après validation.
   - Ajoutez un tag : `git tag v1.2.0 && git push origin v1.2.0`.

## Bonnes pratiques
- **Commits atomiques** : Un commit = une modification logique.
- **Noms de branches clairs** : Utilisez `feature/nom`, `bugfix/nom`, etc.
- **Rebase avant fusion** : Alignez votre branche avec `dev` pour éviter les conflits.
- **Protégez main et dev** : Configurez des règles sur GitHub (Settings > Branches).