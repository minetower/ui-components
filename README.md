# Common components

[![GitLab Release (latest by SemVer)](https://img.shields.io/gitlab/v/release/minetower/ui-components)](https://gitlab.com/minetower/ui-components)

## Install

```bash
# add GitLab NPM registry to project scope
echo '@minetower:registry=https://gitlab.com/api/v4/packages/npm/' >> .npmrc

yarn add -D @minetower/ui-components
```

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
