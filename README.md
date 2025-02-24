[suomeksi](LUEMINUT.md)

# Vision

We enable non-technical people to design an app on their phone so that they can also deploy it for free.

# Mission

We provide an [open source](https://opensource.org) development tool for phones using [Domain-driven design](https://en.wikipedia.org/wiki/Domain-driven_design), a [Unified Modeling Language](https://en.wikipedia.org/wiki/Unified_Modeling_Language), [Command-Query Responsibility Segregation](https://en.wikipedia.org/wiki/Command_Query_Responsibility_Segregation), and [Event Sourcing](https://learn.microsoft.com/en-us/azure/architecture/patterns/event-sourcing). We also provide easy deployment for simple applications. The tool can be used by all software engineers, regardless of programming language or technology, so that as many people as possible can build an application for their needs.

# Strategy

We focus on [Firebase](https://firebase.google.com)-based application development, where the technology choices for the design and target application are [TypeScript](https://www.typescriptlang.org), [React](https://react.dev), [MUI](https://mui.com), and [Mermaid](https://mermaid.js.org/).

The design application is internationalized and support is initially in English and Finnish.

# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type aware lint rules:

- Configure the top-level `parserOptions` property like this:

```js
export default tseslint.config({
  languageOptions: {
    // other options...
    parserOptions: {
      project: ['./tsconfig.node.json', './tsconfig.app.json'],
      tsconfigRootDir: import.meta.dirname,
    },
  },
})
```

- Replace `tseslint.configs.recommended` to `tseslint.configs.recommendedTypeChecked` or `tseslint.configs.strictTypeChecked`
- Optionally add `...tseslint.configs.stylisticTypeChecked`
- Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and update the config:

```js
// eslint.config.js
import react from 'eslint-plugin-react'

export default tseslint.config({
  // Set the react version
  settings: { react: { version: '18.3' } },
  plugins: {
    // Add the react plugin
    react,
  },
  rules: {
    // other rules...
    // Enable its recommended rules
    ...react.configs.recommended.rules,
    ...react.configs['jsx-runtime'].rules,
  },
})
```
