# Apostrophe 3 + Vue 3 widgets + Tailwind CSS

## Get started

Install dependencies: `npm install`

## Running the project

Run `npm run dev` to build the Apostrophe UI and start the site up. Remember, this is during alpha development, so we're all in "dev mode." The `dev` script will watch for saves in client-side CSS and Javascript and trigger a build and page refresh if they are detected. It will also restart the app when server-side code is saved.

## Integration details

- `modules/@apostrophe/home-page/views/page.html`: Replace the default home page
- `modules/asset/index.js`: Tailwind webpack configuration
- `modules/asset/ui/src/style.css`: Tailwind entrypoint
- `modules/asset/ui/src/index.js`: Bundle the Tailwind styles as a global include
- `modules/todo` - A piece that also mounts external Vue 3 app and builds it's own
- `modules/todo-widget` - A widget that mounts (offered in the `todo` piece) Apostrophe Vue app
- `index.d.ts` - To let TS know we have types, needed because our module is CJS.

## Dependencies

- `myovchev/todo-vue3` - a repository installed as npm package `@myovchev/todo-vue3`, contains simple Todo App, bundled with Vite.
- `@corllete/apos-vue3` - Apostrophe Webpack configuration for Vue 3. 
- `vue@^3` - Vue 3
- `vue-tsc` - Development only, alows CI type checking (`npm run test`)