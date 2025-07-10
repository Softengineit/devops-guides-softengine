# Exercice Git Débutant : Créer un plan de cours textuel

## Objectif
Cet exercice vous apprend à initialiser un dépôt GitHub pour organiser un plan de cours fictif en fichiers texte, à modifier un fichier existant, et à soumettre vos modifications via une pull request (PR). Vous travaillerez seul, en utilisant des fichiers texte simples.

## Tâches spécifiques
1. **Créer un dépôt GitHub** :
   - Créez un dépôt nommé `course-plan` sur GitHub.
   - Ne cochez aucune option (README, `.gitignore`).
   - Notez l’URL du dépôt (ex. : `https://github.com/votre-utilisateur/course-plan.git`).

2. **Initialiser le dépôt localement** :
   - Créez un dossier vide nommé `course-plan`.
   - Initialisez un dépôt Git dans ce dossier.
   - Connectez-le au dépôt GitHub distant.

3. **Créer la branche principale** :
   - Créez une branche nommée `main`.
   - Poussez cette branche vers GitHub.

4. **Créer une branche de développement** :
   - À partir de `main`, créez une branche `dev`.
   - Poussez `dev` vers GitHub.

5. **Créer une branche pour le plan** :
   - À partir de `dev`, créez une branche nommée `feature/add-course-plan`.

6. **Ajouter un fichier README** :
   - Créez un fichier `README.md` à la racine avec le contenu suivant :
     ```markdown
     # Plan de Cours
     Ce dépôt contient un plan de cours fictif pour une formation.
     ```
   - Enregistrez le fichier.

7. **Ajouter un plan de cours** :
   - Créez un dossier `plans` à la racine.
   - Créez un fichier `plans/week1.txt` avec le contenu suivant :
     ```
     Semaine 1 : Introduction
     - Jour 1 : Présentation des objectifs
     - Jour 2 : Concepts de base
     ```
   - Enregistrez le fichier.

8. **Ignorer les fichiers inutiles** :
   - Créez un fichier `.gitignore` à la racine.
   - Ajoutez une ligne pour ignorer les fichiers de brouillon, par exemple :
     ```
     *.draft
     ```

9. **Enregistrer les modifications** :
   - Ajoutez `README.md` à l’index Git.
   - Validez avec un message Conventional Commits, par exemple : `docs: ajouter README initial`.
   - Ajoutez le dossier `plans` et `week1.txt` à l’index.
   - Validez avec un message, par exemple : `feat: ajouter plan de cours pour semaine 1`.

10. **Modifier le plan de cours** :
    - Ajoutez une ligne à `plans/week1.txt`, par exemple :
      ```
      - Jour 3 : Exercices pratiques
      ```
    - Ajoutez le fichier modifié à l’index.
    - Validez avec un message, par exemple : `feat: ajouter jour 3 au plan de semaine 1`.

11. **Pousser les modifications** :
    - Poussez la branche `feature/add-course-plan` vers GitHub.
    - Créez une PR de `feature/add-course-plan` vers `dev`.
    - Ajoutez une description, par exemple : "Ajout du README, du plan de cours pour semaine 1, et modification pour ajouter le jour 3, plus .gitignore."

12. **Vérifier les modifications** :
    - Consultez l’historique des commits sur `feature/add-course-plan`.
    - Visualisez les différences introduites par le commit modifiant `week1.txt`.

13. **Synchroniser la branche dev** :
    - Assurez-vous que la branche locale `dev` est à jour avec la branche distante `dev`.

14. **Supprimer la branche locale** :
    - Supprimez la branche locale `feature/add-course-plan` après avoir créé la PR.

15. **Soumettre le dépôt** :
    - Fournissez le lien du dépôt (ex. : `https://github.com/votre-utilisateur/course-plan`) à votre formateur.

## Arborescence attendue
```
course-plan/
├── README.md
├── plans/
│   └── week1.txt
└── .gitignore
```

## Critères d’évaluation
- Dépôt `course-plan` créé et accessible.
- Branches `main`, `dev`, et `feature/add-course-plan` correctement configurées.
- Commits respectant Conventional Commits (`docs`, `feat`, `chore`).
- PR créée vers `dev` avec description claire.
- Fichiers `README.md` et `week1.txt` contenant le contenu demandé, avec modification.
- Fichier `.gitignore` excluant `*.draft`.
- Historique des commits vérifiable.
- Branche locale `feature/add-course-plan` supprimée.