# [Bun](https://bun.sh)

Yet another Javascript runtime

## Useful commands

```shell
bun upgrade # Upgrade bun binary to the latest version
bun init # Start new project

bun add packageName # Install package
```

## packaje.json

> Run with `bun run scriptName`

```json
{
    "scripts": {
        "start": "bun run index.ts",
        "dev": "bun --watch index.ts"
    }
}
```
