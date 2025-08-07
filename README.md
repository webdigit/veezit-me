# Veezit Admin

Application d'administration Veezit construite avec Vue 3, TypeScript, Vuetify 3 et Vite.

## 🚀 Technologies

- **Vue 3** - Framework JavaScript progressif
- **TypeScript** - Typage statique strict
- **Vuetify 3** - Framework UI Material Design
- **Vite** - Build tool moderne
- **Vue Router** - Routing côté client
- **Pinia** - Gestion d'état
- **ESLint + Prettier** - Linting et formatage

## 📋 Prérequis

- Node.js 18+ 
- npm ou yarn

## 🛠️ Installation

1. Cloner le projet
```bash
git clone <repository-url>
cd veezit-app
```

2. Installer les dépendances
```bash
npm install
```

3. Copier le fichier d'environnement
```bash
cp .env.example .env
```

4. Démarrer le serveur de développement
```bash
npm run dev
```

## 📁 Structure du projet

```
src/
├── components/     # Composants réutilisables
├── views/         # Pages de l'application
│   ├── HomeView.vue      # Dashboard
│   └── LoginView.vue     # Page de connexion
├── router/        # Configuration des routes
├── stores/        # Stores Pinia
├── plugins/       # Plugins (Vuetify)
└── assets/        # Ressources statiques
```

## 🎯 Fonctionnalités

- ✅ Layout responsive avec AppBar et navigation latérale
- ✅ Page Dashboard placeholder
- ✅ Page de connexion placeholder
- ✅ Navigation entre les pages
- ✅ Thème Vuetify clair
- ✅ Configuration TypeScript strict
- ✅ ESLint + Prettier configurés

## 🔧 Scripts disponibles

```bash
npm run dev          # Démarrer le serveur de développement
npm run build        # Build pour la production
npm run preview      # Prévisualiser le build
npm run lint         # Linter le code
npm run format       # Formater le code
```

## 🌍 Variables d'environnement

Copiez `.env.example` vers `.env` et configurez :

```env
VITE_API_BASE_URL=https://api.veezit.local
VITE_APP_NAME=Veezit Admin
```

## 📱 Pages disponibles

- **/** - Dashboard principal
- **/login** - Page de connexion

## 🔒 Sécurité

⚠️ **Note** : Cette version est un placeholder sans authentification réelle. L'authentification sera implémentée dans les prochaines versions.

## 🤝 Contribution

1. Fork le projet
2. Créer une branche feature (`git checkout -b feature/AmazingFeature`)
3. Commit les changements (`git commit -m 'Add some AmazingFeature'`)
4. Push vers la branche (`git push origin feature/AmazingFeature`)
5. Ouvrir une Pull Request

## 📄 Licence

Ce projet est sous licence MIT.
