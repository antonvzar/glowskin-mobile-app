# glowskin-mobile-app

This template should help get you started developing with Vue 3 in Vite.

## Project structure


---

## Directory Details

- **`src/`**: Contains the core application files.
  - **`assets/`**: Static assets such as images and fonts.
    - `images/`: Contains images for various sections and icons.
    - `fonts/`: Holds font files used across the application.
  - **`components/`**: Contains reusable Vue components.
    - `Header.vue`: Header component containing navigation links.
    - `HeroSection.vue`: Introduces the GlowSkin Project with a brief overview.
    - `SystemDescription.vue`: Describes the capabilities of the GlowSkin system.
    - `SuggestionSection.vue`: Outlines system recommendations based on user analysis.
    - `WhyChooseUs.vue`: Highlights reasons to choose the GlowSkin system.
    - `AnalysisSteps.vue`: Guides users to start a skin analysis.
    - `CommunitySection.vue`: Provides contact and subscription options.
    - `Footer.vue`: Contains footer links and social media icons.
  - **`router/`**: Sets up routing for different pages within the application.
    - `index.js`: Defines and configures routes.
  - **`store/`**: Vuex store configuration for state management.
    - `index.js`: Sets up the main Vuex store.
    - `modules/`: Contains modular Vuex store configurations for different sections.
  - **`App.vue`**: The root Vue component, hosting the main layout.
  - **`main.js`**: Entry file that initializes the Vue app, configuring the store and router.
- **`package.json`**: Lists dependencies, scripts, and project metadata.
- **`README.md`**: Documentation for project setup, usage, and structure.
- **`index.html`**: Serves as the main HTML file where the Vue application is mounted



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
