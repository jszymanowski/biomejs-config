**Key features:**
- Uses your `.gitignore` to avoid formatting unuseful files and directories.
- Up to 100 chars per line for modern monitors.
- Single quotes, no trailing commas, semicolons and spaces instead of tabs.

### Usage
Firstly, install [biome](https://biomejs.dev) and this [configuration](https://www.npmjs.com/package/@jszymanowski/biomejs-config):

```sh
pnpm i -D @jszymanowski/biomejs-config @biomejs/biome
```

Then add the following to your `biome.json`:

```jsonc
{
  "$schema": "https://biomejs.dev/schemas/latest/schema.json",
  "extends": ["@jszymanowski/biomejs-config"]
}
```

And finally, add the following scripts to your `package.json` to easily format and lint your code:

```jsonc
{
  "scripts": {
    "format": "biome format --write .",
    "lint": "biome check .",
    "lint:ci": "biome ci .",
    "lint:fix": "biome check --write --unsafe ."
  }
}
```