# Templates de projets

Ce fichier répertorie les dépôts de templates préconfigurés avec des pipelines CI/CD pour différents types de projets.

## Liste des templates
1. **Node.js Starter**
   - Dépôt : [your-org/node-starter](https://github.com/your-org/node-starter)
   - Description : API REST avec Express, tests Jest, et pipeline CI/CD.
   - Utilisation :
     ```bash
     git clone https://github.com/your-org/node-starter.git
     npm ci
     npm start
     ```

2. **React-Vite Starter**
   - Dépôt : [your-org/react-vite-starter](https://github.com/your-org/react-vite-starter)
   - Description : Application React avec Vite, ESLint, et pipeline CI/CD.
   - Utilisation :
     ```bash
     git clone https://github.com/your-org/react-vite-starter.git
     npm ci
     npm run dev
     ```

3. **Next.js Starter**
   - Dépôt : [your-org/nextjs-starter](https://github.com/your-org/nextjs-starter)
   - Description : Application Next.js avec SSR, ESLint, et pipeline CI/CD.
   - Utilisation :
     ```bash
     git clone https://github.com/your-org/nextjs-starter.git
     npm ci
     npm run dev
     ```

4. **Android Starter**
   - Dépôt : [your-org/android-starter](https://github.com/your-org/android-starter)
   - Description : Application Android avec Gradle, tests unitaires, et Fastlane.
   - Utilisation :
     ```bash
     git clone https://github.com/your-org/android-starter.git
     ./gradlew build
     ```

5. **React Native Starter**
   - Dépôt : [your-org/react-native-starter](https://github.com/your-org/react-native-starter)
   - Description : Application React Native avec Metro, tests, et Fastlane.
   - Utilisation :
     ```bash
     git clone https://github.com/your-org/react-native-starter.git
     npm ci
     npx react-native run-android
     ```

## Structure des templates
Chaque template inclut :
- Un `README.md` avec des instructions d’installation et d’utilisation.
- Un pipeline CI/CD (`.github/workflows/ci.yml`) pour tests, linting, et déploiement.
- Un `Dockerfile` (si applicable) pour conteneurisation.
- Des configurations pour ESLint, Jest, ou Gradle selon le projet.

## Créer un nouveau projet
1. Cloner le template correspondant.
2. Suivre le README du dépôt pour les instructions spécifiques.
3. Créer une branche et suivre la [stratégie Git](../guides/git-strategy.md).