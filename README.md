# Common components

## Components

- `Navbar`

```svelte
<script>
    import { Navbar } from '@minetower/ui-components'
</script>

<Navbar 
    title="Minecraft Tweaks"
    small_title="Tweaks"
    repo_url="/minecraft-tweaks"
    center_title />
```

## Tailwind css

You must tell tailwind to keep track of these components for the classes, so do something like this:

```js
// tailwind.config.js
const ui_components = ['Navbar']

module.exports = {
    content: [
        // other options
        ...ui_components.map((c) =>
            require.resolve(`@minetower/ui-components/src/${c}.svelte`)),
    ],
    // other options
}
```
