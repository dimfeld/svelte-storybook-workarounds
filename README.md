# svelte-storybook-workarounds

**Update for 2023: Don't use this anymore. Storybook 7 is in beta and works great with SvelteKit 1.0 out of the box!**




This is an example repository showing the workarounds needed to get Storybook working well with SvelteKit as of July 2021.

SvelteKit is still changing as of this writing and Storybook is constantly releasing new versions,
so I do not recommend forking this code as it may be out of date by the time you see it.

Instead, I recommend these steps:

1. Create your Sveltekit project: `npm init svelte@next my-app`
2. Install Storybook: `cd my-app && npx sb init`
3. Install Webpack 5 Storybook builder dependencies: `npm install --save-dev @storybook/builder-webpack5 @storybook/manager-webpack5`
4. Copy the following files from this repository:
    - [`.storybook/main.cjs`](./.storybook/main.cjs) -- and delete `.storybook/main.js` in your project
    - [`.storybook/package.json`](./storybook/package.json) -- yes, it's just an empty object
5. Make sure that the Svelte preprocessor configuration in `.storybook/main.cjs` matches the one you want in `svelte.config.js`.

I've detailed the full process [on my website](https://imfeld.dev/writing/sveltekit_with_storybook).
