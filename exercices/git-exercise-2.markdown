# Exercice Git Débutant : Créer une liste de tâches organisée

## Objectif
Cet exercice vous apprend à initialiser un dépôt GitHub pour gérer une liste de tâches textuelle, à organiser des fichiers texte, et à soumettre vos modifications via une pull request (PR). Vous travaillerez seul, en utilisant des fichiers texte simples.

## Tâches spécifiques
1. **Créer un dépôt GitHub** :
   - Créez un dépôt nommé `task-list` sur GitHub dans votre espace personnel.
   - Ne cochez aucune option (README, `.gitignore`).
   - Notez l’URL du dépôt (ex. : `https://github.com/votre-utilisateur/task-list.git`).

2. **Initialiser le dépôt localement** :
   - Créez un dossier vide nommé `task-list`.
   - Initialisez un dépôt Git dans ce dossier.
   - Connectez-le au dépôt GitHub distant.

3. **Créer la branche principale** :
   - Créez une branche nommée `main`.
   - Poussez cette branche vers GitHub.

4. **Créer une branche de développement** :
   - À partir de `main`, créez une branche `dev`.
   - Poussez `dev` vers GitHub.

5. **Créer une branche pour la liste de tâches** :
   - À partir de `dev`, créez une branche nommée `feature/add-task-list`.

6. **Ajouter un fichier README** :
   - Créez un fichier `README.md` à la racine avec le contenu suivant :
     ```markdown
     # Liste de Tâches
     Ce dépôt organise les tâches d’un projet fictif dans des fichiers texte.
     ```
   - Enregistrez le fichier.

7. **Ajouter une liste de tâches** :
   - Créez un dossier `tasks` à la racine.
   - Créez un fichier `tasks/priorities.txt` avec le contenu suivant :
     ```
     - Tâche 1 : Planifier le projet
     - Tâche 2 : Rédiger la documentation
     - Tâche 3 : Tester les fonctionnalités
     ```
   - Enregistrez le fichier.

8. **Ignorer les fichiers inutiles** :
   - Créez un fichier `.gitignore` à la racine.
   - Ajoutez une ligne pour ignorer les fichiers de brouillon, par exemple :
     ```
     draft.txt
     ```

9. **Enregistrer les modifications** :
   - Ajoutez `README.md` à l’index Git.
   - Validez avec un message Conventional Commits, par exemple : `docs: ajouter README initial`.
   - Ajoutez le dossier `tasks` et `priorities.txt` à l’index.
   - Validez avec un message, par exemple : `feat: ajouter liste de tâches prioritaires`.
   - Ajoutez `.gitignore` à l’index.
   - Validez avec un message, par exemple : `chore: ajouter .gitignore pour brouillons`.

10. **Pousser les modifications** :
    - Poussez la branche `feature/add-task-list` vers GitHub.
    - Créez une PR de `feature/add-task-list` vers `dev`.
    - Ajoutez une description, par exemple : "Ajout du README et d’une liste de tâches dans tasks/priorities.txt, plus .gitignore."

11. **Vérifier les modifications** :
    - Consultez l’historique des commits sur `feature/add-task-list`.
    - Visualisez les différences introduites par le commit de `priorities.txt`.

12. **Synchroniser la branche dev** :
    - Assurez-vous que la branche locale `dev` est à jour avec la branche distante `dev`.

13. **Supprimer la branche locale** :
    - Supprimez la branche locale `feature/add-task-list` après avoir créé la PR.

14. **Soumettre le dépôt** :
    - Fournissez le lien du dépôt (ex. : `https://github.com/votre-utilisateur/task-list`) à votre formateur.

## Arborescence attendue
```
task-list/
├── README.md
├── tasks/
│   └── priorities.txt
└── .gitignore
```

## Critères d’évaluation
- Dépôt `task-list` créé et accessible.
- Branches `main`, `dev`, et `feature/add-task-list` correctement configurées.
- Commits respectant Conventional Commits (`docs`, `feat`, `chore`).
- PR créée vers `dev` avec description claire.
- Fichiers `README.md` et `priorities.txt` contenant le contenu demandé.
- Fichier `.gitignore` excluant `draft.txt`.
- Historique des commits vérifiable.
- Branche locale `feature/add-task-list` supprimée.