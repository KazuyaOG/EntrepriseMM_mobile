# Gestion MM — iOS

Application mobile iOS de gestion pour Entreprise Michel Maisonneuve. Elle reprend l’application web EntrepriseMM (gestion des clients, calendrier/rendez-vous, factures, rappels, dépenses, taxes et outils) et l’emballe comme une application iOS native avec Capacitor.

## Prérequis

- Node.js 20+
- macOS avec Xcode (pour compiler, lancer le simulateur ou signer l’application iOS)

## Développement web

```sh
npm install
npm run dev
```

## Créer et lancer l’application iOS

```sh
npm install
npm run build
npx cap add ios       # une seule fois
npx cap sync ios      # après chaque changement de l’application web
npx cap open ios      # ouvrir le projet dans Xcode
```

Dans Xcode, choisissez un simulateur iPhone ou un appareil connecté puis Run. Pour une distribution, configurez la signature dans Signing & Capabilities et archivez l’application depuis Xcode. La compilation iOS nécessite macOS/Xcode.

Les données actuelles sont conservées localement sur l’appareil via le stockage du navigateur; elles ne sont pas synchronisées entre appareils. Faites des sauvegardes régulières depuis l’application.
