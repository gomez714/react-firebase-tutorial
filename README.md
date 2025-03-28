# ⚡ react-ts-firebase-tutorial

Starter using Vite + React + TypeScript + Tailwind with Firebase.

## Motivation

To provide an efficient and a quick way to understand how to implement CRUD functionality in the new version of Firebase (v9). Paired with ReactJs and TS, Firebase is a great tool for a quick prototyping or for someone learning full stack development.

This starter uses following libraries:

- Vite
- React
  - React Router
- TypeScript
- Tailwind CSS
  - daisyUI
- Firebase(v9, modular)
- ESLint
- Prettier

## Project Description

This is an AI tool directory, where tools can be listed, added and edited to cover CRUD functions in Firebase, but really concepts could be applied to other setup whether it's a simple todo app or a first version of a more compilcated app, for example inventory management.


## Set up

```shell
mv .env.local.example .env.local
yarn
yarn dev
```

### Firebase

If you **DO NOT** use Firebase, you should do:

- Delete the Firebase-related code: you check Main.tsx, SignInButton.tsx, SignOutButton.tsx.
- And then delete `src/lib/firebase.ts`
- Run `yarn remove firebase`
- Remove `VITE_FIREBASE_*` env values from `.env.local`

If you want to use Firebase, you should do:

- copy Firebase env values from Firebase Console, and paste them to `.env.local`.
- enable Google Auth in Firebase Console. ref: https://firebase.google.com/docs/auth/web/google-signin#before_you_begin

## Vite

[Vite](https://github.com/vitejs/vite) is a fast frontend build tool. According to the [README](https://github.com/vitejs/vite/blob/main/README.md), it consists of two major parts:

- A dev server that serves your source files over native ES modules, with rich built-in features and astonishingly fast Hot Module Replacement (HMR).
- A build command that bundles your code with Rollup, pre-configured to output highly optimized static assets for production.

## React

[React](https://github.com/facebook/react) is a JavaScript library for building user interfaces.

Due to its awesome renderer system, there are many [React Renderor](https://github.com/chentsulin/awesome-react-renderer). So React can be not used only Web, for example, used by [React Native](https://reactnative.dev/).

Let's dive into React and Vite can use with React.

## TypeScript

[TypeScript](https://github.com/microsoft/TypeScript) is a superset of JavaScript. It is just one of NPM library, but it provides an original compiler.

When you use TypeScript with React, you can write JSX with TypeScript, called TSX. Then you can develop views written by  **Type-Safe** template.

## Tailwind CSS

[Tailwind CSS](https://tailwindcss.com/) is modern utility-first CSS framework. It provides many CSS rules, but these are purged when production builds. So developers do not worry about CSS asset size for performance optimization.

In VSCode, I recommend to use [intellisense extension](https://tailwindcss.com/docs/intellisense).

Frequently, React developers are worried about how to write CSS in TSX(JSX) template. You must choose from CSS Modules, [styled-components](https://styled-components.com/), [linaria](https://github.com/callstack/linaria), and so on.
Additionally, CSS architecture is difficult about scoping, e.g. BEM, FLOCSS.

When you decide to use Tailwind, you only write utility-first CSS classes, you don't have to worry about them!

### daisyUI

[daisyUI](https://daisyui.com/) is Tailwind CSS Components library.

It prepares components CSS classes such as 'btn'. If you provide 'btn' class to `<button>` element, then there should be placed completely designed button.

If you don't want to use it, just remove the package and remove config in `tailwind.config.js`.

### Heroicons
Collection of SVG icons, by the makers of Tailwind CSS. You can browse icons in their (directory)
[https://heroicons.com/]

## Firebase

[Firebase](https://firebase.google.com/) is a PaaS that makes us create hi-quality apps so easy and so fast.

This library is not suitable for everyone, but I think it is one of the best libraries for prototyping. Therefore, I have added it to this repository.

The Firebase js SDK has become very useful in version 9, with [optimizations that greatly reduce bundle size](https://firebase.google.com/docs/web/modular-upgrade).

### How to Use

Please look at [firebase.ts](https://github.com/TeXmeijin/vite-react-ts-tailwind-starter/blob/main/src/lib/firebase.ts).

There you will find a set of utility functions to manipulate Firebase for the environment in which the Emulator is used.

## Formatter and Linter

Already set up [ESLint](https://eslint.org/) and [Prettier](https://prettier.io/). You can customize the rules.

NOTICE: The template does not use [eslint-plugin-prettier](https://github.com/prettier/eslint-plugin-prettier) and [prettier-eslint](https://github.com/prettier/prettier-eslint). So I recommend that running commands individually. e.g. `prettier && eslint`.

Please read: https://prettier.io/docs/en/integrating-with-linters.html.

