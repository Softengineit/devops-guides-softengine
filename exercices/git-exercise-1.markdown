# Exercice Git Débutant : Créer un journal de projet avec des entrées texte

## Objectif
Cet exercice vous apprend à créer un dépôt GitHub pour tenir un journal de projet fictif, à organiser des entrées texte, et à soumettre vos modifications via une pull request (PR). Vous travaillerez seul, en utilisant uniquement des fichiers texte simples, et en respectant la stratégie GitFlow et les conventions de commits.

## Tâches spécifiques
1. **Créer un dépôt GitHub** :
   - Connectez-vous à GitHub et créez un dépôt nommé `project-journal` dans votre espace personnel.
   - Ne cochez aucune option (README, `.gitignore`) lors de la création.
   - Notez l’URL du dépôt (ex. : `https://github.com/votre-utilisateur/project-journal.git`).

2. **Initialiser le dépôt localement** :
   - Créez un dossier vide nommé `project-journal` sur votre ordinateur.
   - Initialisez un dépôt Git dans ce dossier.
   - Connectez ce dépôt local au dépôt GitHub distant.

3. **Créer la branche principale** :
   - Créez une branche nommée `main` pour la base stable du projet.
   - Poussez cette branche vers GitHub.

4. **Créer une branche de développement** :
   - À partir de `main`, créez une branche nommée `dev` pour les modifications en cours.
   - Poussez `dev` vers GitHub.

5. **Créer une branche pour le journal** :
   - À partir de `dev`, créez une branche nommée `feature/add-journal-entry`.

6. **Ajouter un fichier README** :
   - Créez un fichier `README.md` à la racine avec le contenu suivant :
     ```markdown
     # Journal de Projet
     Ce dépôt contient un journal fictif pour suivre les progrès d’un projet.
     ```
   - Enregistrez le fichier.

7. **Ajouter une entrée de journal** :
   - Créez un dossier `journal` à la racine.
   - Créez un fichier `journal/2025-07-10.txt` avec le contenu suivant :
     ```
     Date: 10 juillet 2025
     Entrée: Démarrage du projet. Objectif défini : documenter les progrès quotidiens.
     ```
   - Enregistrez le fichier.

8. **Ignorer les fichiers inutiles** :
   - Créez un fichier `.gitignore` à la racine.
   - Ajoutez une ligne pour ignorer les fichiers temporaires, par exemple :
     ```
     *.bak
     ```

9. **Enregistrer les modifications** :
   - Ajoutez `README.md` à l’index Git.
   - Validez avec un message Conventional Commits, par exemple : `docs: ajouter README initial`.
   - Ajoutez le dossier `journal` et `2025-07-10.txt` à l’index.
   - Validez avec un message, par exemple : `feat: ajouter première entrée de journal`.
   - Ajoutez `.gitignore` à l’index.
   - Validez avec un message, par exemple : `chore: ajouter .gitignore pour fichiers de sauvegarde`.

10. **Pousser les modifications** :
    - Poussez la branche `feature/add-journal-entry` vers GitHub.
    - Créez une PR de `feature/add-journal-entry` vers `dev`.
    - Ajoutez une description, par exemple : "Ajout du README et de la première entrée de journal dans journal/2025-07-10.txt, plus .gitignore."

11. **Vérifier les modifications** :
    - Consultez l’historique des commits sur `feature/add-journal-entry` pour voir les trois commits.
    - Visualisez les différences introduites par le commit de `2025-07-10.txt`.

12. **Synchroniser la branche dev** :
    - Assurez-vous que la branche locale `dev` est à jour avec la branche distante `dev`.

13. **Supprimer la branche locale** :
    - Supprimez la branche locale `feature/add-journal-entry` après avoir créé la PR.

14. **Soumettre le dépôt** :
    - Fournissez le lien du dépôt (ex. : `https://github.com/votre-utilisateur/project-journal`) à votre formateur.

## Arborescence attendue
```
project-journal/
├── README.md
├── journal/
│   └── 2025-07-10.txt
└── .gitignore
```

## Critères d’évaluation
- Dépôt `project-journal` créé et accessible.
- Branches `main`, `dev`, et `feature/add-journal-entry` correctement configurées.
- Commits respectant Conventional Commits (`docs`, `feat`, `chore`).
- PR créée vers `dev` avec description claire.
- Fichiers `README.md` et `2025-07-10.txt` contenant le contenu demandé.
- Fichier `.gitignore` excluant `*.bak`.
- Historique des commits vérifiable.
- Branche locale `feature/add-journal-entry` supprimée.