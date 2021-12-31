# SvelteKit localStorage setup (with TypeScript and examples)

This repo presets a quick way to set up local storage functionality to your [SvelteKit](https://kit.svelte.dev/) stores.
Here is the list of files created and modified in this tutorial:
```
src/
  routes/
    __layout.svelte
    about.svelte
    contact.svelte
    index.svelte
  stores/
    index.ts
    store-localstorage.ts
```

## To the point: _SvelteKit_ + _localStorage_

**Note:** This tutorial assumes you installed SvelteKit scaffolding with _TypeScript_ support according to the instructions
on the [home page](https://kit.svelte.dev/)

The `/src/stores/store-localstorage.ts` contains a wrapper for `writable` found in `svelte/store`. Use it like this:
```ts
// In a file set for your stores, like stores/index.ts here
import { writableLocal } from "../stores/store-localstorage.ts"

const store = writableLocal<string>("yourStoreKey", "A default value")

// And now in .svelte files you can manipulate the store
// as you would normally do
// and it will be saved to the localStorage
$store = "New value"

// To reset the localStorage set it to undefined
$store = undefined
```

Check out the `.svelte` files in the `routes` directory for examples.

## License

[Svelte](https://svelte.dev/) itself is [MIT-licensed](https://mit-license.org/), thus all of my code inside is free to use as well. You can freely link here and tell all your friends about this repo.

Feel free to fork, clone, open issues and comment this repo.