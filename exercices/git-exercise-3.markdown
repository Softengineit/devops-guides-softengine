# Exercice Git Débutant : Créer des notes de réunion organisées

## Objectif
Cet exercice vous apprend à initialiser un dépôt GitHub pour organiser des notes de réunion en fichiers texte, et à soumettre vos modifications via une pull request (PR). Vous travaillerez seul, en utilisant des fichiers texte simples.

## Tâches spécifiques
1. **Créer un dépôt GitHub** :
   - Créez un dépôt nommé `meeting-notes` sur GitHub.
   - Ne cochez aucune option (README, `.gitignore`).
   - Notez l’URL du dépôt (ex. : `https://github.com/votre-utilisateur/meeting-notes.git`).

2. **Initialiser le dépôt localement** :
   - Créez un dossier vide nommé `meeting-notes`.
   - Initialisez un dépôt Git dans ce dossier.
   - Connectez-le au dépôt GitHub distant.

3. **Créer la branche principale** :
   - Créez une branche nommée `main`.
   - Poussez cette branche vers GitHub.

4. **Créer une branche de développement** :
   - À partir de `main`, créez une branche `dev`.
   - Poussez `dev` vers GitHub.

5. **Créer une branche pour les notes** :
   - À partir de `dev`, créez une branche nommée `feature/add-meeting-notes`.

6. **Ajouter un fichier README** :
   - Créez un fichier `README.md` à la racine avec le contenu suivant :
     ```markdown
     # Notes de Réunion
     Ce dépôt contient les notes des réunions d’équipe fictives.
     ```
   - Enregistrez le fichier.

7. **Ajouter des notes de réunion** :
   - Créez un dossier `notes` à la racine.
   - Créez un fichier `notes/2025-07-10.txt` avec le contenu suivant :
     ```
     Réunion du 10 juillet 2025
     - Discussion sur les objectifs du projet.
     - Planification des prochaines étapes.
     ```
   - Enregistrez le fichier.

8. **Ignorer les fichiers inutiles** :
   - Créez un fichier `.gitignore` à la racine.
   - Ajoutez une ligne pour ignorer les fichiers personnels, par exemple :
     ```
     personal.txt
     ```

9. **Enregistrer les modifications** :
   - Ajoutez `README.md` à l’index Git.
   - Validez avec un message Conventional Commits, par exemple : `docs: ajouter README initial`.
   - Ajoutez le dossier `notes` et `2025-07-10.txt` à l’index.
   - Validez avec un message, par exemple : `feat: ajouter notes de réunion du 10 juillet`.
   - Ajoutez `.gitignore` à l’index.
   - Validez avec un message, par exemple : `chore: ajouter .gitignore pour fichiers personnels`.

10. **Pousser les modifications** :
    - Poussez la branche `feature/add-meeting-notes` vers GitHub.
    - Créez une PR de `feature/add-meeting-notes` vers `dev`.
    - Ajoutez une description, par exemple : "Ajout du README et des notes de réunion dans notes/2025-07-10.txt, plus .gitignore."

11. **Vérifier les modifications** :
    - Consultez l’historique des commits sur `feature/add-meeting-notes`.
    - Visualisez les différences introduites par le commit de `2025-07-10.txt`.

12. **Synchroniser la branche dev** :
    - Assurez-vous que la branche locale `dev` est à jour avec la branche distante `dev`.

13. **Supprimer la branche locale** :
    - Supprimez la branche locale `feature/add-meeting-notes` après avoir créé la PR.

14. **Soumettre le dépôt** :
    - Fournissez le lien du dépôt (ex. : `https://github.com/votre-utilisateur/meeting-notes`) à votre formateur.

## Arborescence attendue
```
meeting-notes/
├── README.md
├── notes/
│   └── 2025-07-10.txt
└── .gitignore
```

## Critères d’évaluation
- Dépôt `meeting-notes` créé et accessible.
- Branches `main`, `dev`, et `feature/add-meeting-notes` correctement configurées.
- Commits respectant Conventional Commits (`docs`, `feat`, `chore`).
- PR créée vers `dev` avec description claire.
- Fichiers `README.md` et `2025-07-10.txt` contenant le contenu demandé.
- Fichier `.gitignore` excluant `personal.txt`.
- Historique des commits vérifiable.
- Branche locale `feature/add-meeting-notes` supprimée.