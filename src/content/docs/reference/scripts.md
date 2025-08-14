---
title: Scripts and CLI
description: Commands to develop, build, and preview the site.
---

All commands are run from the project root.

## NPM scripts

| Command | Description |
| --- | --- |
| `npm install` | Install dependencies |
| `npm run dev` | Start the dev server at `http://localhost:4321` |
| `npm run build` | Build the production site into `./dist/` |
| `npm run preview` | Preview the built site locally |
| `npm run astro ...` | Run `astro` subcommands (e.g., `astro check`) |

## Examples

```bash
# Start local development
yarn dev
# or
npm run dev

# Build for production
npm run build

# Preview a local build
npm run preview

# Get help for the Astro CLI
npm run astro -- --help
```

## Common tasks

- To add an integration: `npm run astro add <integration>`
- To type-check content and MDX: `npm run astro check`
- To upgrade dependencies: `npm outdated && npm update`