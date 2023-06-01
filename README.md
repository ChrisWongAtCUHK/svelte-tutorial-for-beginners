# Svelte + Vite

This template should help get you started developing with Svelte in Vite.

## Recommended IDE Setup

[VS Code](https://code.visualstudio.com/) + [Svelte](https://marketplace.visualstudio.com/items?itemName=svelte.svelte-vscode).

## Need an official Svelte framework?

Check out [SvelteKit](https://github.com/sveltejs/kit#readme), which is also powered by Vite. Deploy anywhere with its serverless-first approach and adapt to various platforms, with out of the box support for TypeScript, SCSS, and Less, and easily-added support for mdsvex, GraphQL, PostCSS, Tailwind CSS, and more.

## Technical considerations

**Why use this over SvelteKit?**

- It brings its own routing solution which might not be preferable for some users.
- It is first and foremost a framework that just happens to use Vite under the hood, not a Vite app.

This template contains as little as possible to get started with Vite + Svelte, while taking into account the developer experience with regards to HMR and intellisense. It demonstrates capabilities on par with the other `create-vite` templates and is a good starting point for beginners dipping their toes into a Vite + Svelte project.

Should you later need the extended capabilities and extensibility provided by SvelteKit, the template has been structured similarly to SvelteKit so that it is easy to migrate.

**Why `global.d.ts` instead of `compilerOptions.types` inside `jsconfig.json` or `tsconfig.json`?**

Setting `compilerOptions.types` shuts out all other types not explicitly listed in the configuration. Using triple-slash references keeps the default TypeScript setting of accepting type information from the entire workspace, while also adding `svelte` and `vite/client` type information.

**Why include `.vscode/extensions.json`?**

Other templates indirectly recommend extensions via the README, but this file allows VS Code to prompt the user to install the recommended extension upon opening the project.

**Why enable `checkJs` in the JS template?**

It is likely that most cases of changing variable types in runtime are likely to be accidental, rather than deliberate. This provides advanced typechecking out of the box. Should you like to take advantage of the dynamically-typed nature of JavaScript, it is trivial to change the configuration.

**Why is HMR not preserving my local component state?**

HMR state preservation comes with a number of gotchas! It has been disabled by default in both `svelte-hmr` and `@sveltejs/vite-plugin-svelte` due to its often surprising behavior. You can read the details [here](https://github.com/sveltejs/svelte-hmr/tree/master/packages/svelte-hmr#preservation-of-local-state).

If you have state that's important to retain within a component, consider creating an external store which would not be replaced by HMR.

```js
// store.js
// An extremely simple external store
import { writable } from 'svelte/store'
export default writable(0)
```

# [Svelte Tutorial for Beginners](https://www.youtube.com/playlist?list=PL4cUxeGkcC9hlbrVO_2QFVqVPhlZmz7tO)
* [Svelte Tutorial for Beginners #19 - Header & Footer Components](https://www.youtube.com/watch?v=xwiER0u9YS0)
* [Svelte Tutorial for Beginners #20 - Reusable Tabs Component](https://www.youtube.com/watch?v=U8cM_jhmDxA)
* [Svelte Tutorial for Beginners #21 - Poll Form Component](https://www.youtube.com/watch?v=Cv8vo4ZBy2E)
* [Svelte Tutorial for Beginners #22 - Custom Button Component](https://www.youtube.com/watch?v=3-DO-9fUKo0)
* [Svelte Tutorial for Beginners #23 - Custom Form Validation](https://www.youtube.com/watch?v=lx71zJldzEs)
* [Svelte Tutorial for Beginners #24 - Adding New Polls](https://www.youtube.com/watch?v=lCiyWC8cqDg)
* [Svelte Tutorial for Beginners #25 - Poll Details Component](https://www.youtube.com/watch?v=OC_WmW3nZCs)
* [Svelte Tutorial for Beginners #26 - Card Component](https://www.youtube.com/watch?v=2z4z7zgyT9g)
* [Svelte Tutorial for Beginners #27 - Casting Votes](https://www.youtube.com/watch?v=eqmxFAxBwBo)
* [Svelte Tutorial for Beginners #28 - Vote Bars](https://www.youtube.com/watch?v=05lrYOs6GTM)
* [Svelte Tutorial for Beginners #29 - Introduction to Stores](https://www.youtube.com/watch?v=rszZ7TYTbR0)
* [Svelte Tutorial for Beginners #30 - Lifecycle Hooks](https://www.youtube.com/watch?v=pza7POTt9Yo)
* [Svelte Tutorial for Beginners #31 - Updating Store Data](https://www.youtube.com/watch?v=dD7uF_CgN_8)
* [Svelte Tutorial for Beginners #32 - Deleting Polls](https://www.youtube.com/watch?v=izXFqVTUfXU)