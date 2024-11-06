# glowskin-mobile-app

This template should help get you started developing with Vue 3 in Vite.

## Project structure

glowskin-mobile-app/
├── public/
│   └── index.html               # Main HTML file, where the Vue app is mounted
├── src/
│   ├── assets/                  # Static assets (images, fonts, etc.)
│   │   ├── images/              # Image assets for the project
│   │   └── fonts/               # Font files if custom fonts are used in the project
│   ├── components/              # Reusable Vue components
│   │   ├── Header.vue           # Header component containing navigation links
│   │   ├── HeroSection.vue      # Introducing the GlowSkin Project
│   │   ├── SystemDescription.vue # Description of GlowSkin’s system capabilities
│   │   ├── SuggestionSection.vue # Describing what system could suggest you after the analysis
│   │   ├── WhyChooseUs.vue      # Section outlining reasons to choose GlowSkin
│   │   ├── AnalysisSteps.vue    # Link to skin analysis
│   │   ├── CommunitySection.vue # Contains subscription form and privacy notice
│   │   ├── Footer.vue           # Footer component with links and social media icons
│   └── router/                  # Router configuration for page navigation
│   |    └── index.js             # Defines routes
│   ├── stores/                   # Vuex store for global state management
│   │   ├── index.js             # Main store setup file
│   │   ├── modules/             # Modular Vuex store organization
│   ├── App.vue                  # Root Vue component that hosts the main layout
│   └──  main.js                  # Main entry file where the Vue app is initialized
├── package.json                 # Project configuration, scripts, and dependencies
└── README.md                    # Documentation file outlining project setup, usage, and structure



## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur).

## Customize configuration

See [Vite Configuration Reference](https://vite.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```
