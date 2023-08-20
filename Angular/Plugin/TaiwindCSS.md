# TaiwindCSS

##  1. Create new Project
Start by creating a new Angular project if you don’t have one set up already. The most common approach is to use Angular CLI.

```sh
> ng new my-project
> cd my-project
```

## 2. Install Tailwind CSS
Install tailwindcss via npm, and then run the init command to generate a tailwind.config.js file.

```sh
pnpm install -D tailwindcss postcss autoprefixer
npx tailwindcss init
```

## 3. Configure your template paths
Add the paths to all of your template files in your tailwind.config.js file.

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./src/**/*.{html,ts}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

## 4. Add the Tailwind directives to your CSS
Add the @tailwind directives for each of Tailwind’s layers to your ./src/styles.css file.

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

## 5. Automatic class sorting with [prettier-plugin-tailwindcss](https://github.com/tailwindlabs/prettier-plugin-tailwindcss)
To get started, install prettier-plugin-tailwindcss as a dev-dependency:

```sh
pnpm install -D prettier prettier-plugin-tailwindcss
```

Then add the plugin to your Prettier config:

```js
// prettier.config.js
module.exports = {
  plugins: ['prettier-plugin-tailwindcss'],
}
```
