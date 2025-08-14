---
title: Components
description: UI components used in MDX pages and how to use them.
---

This starter uses Starlight-provided components. Below are commonly used components with examples.

## Card and CardGrid

- Import from `@astrojs/starlight/components` in `.mdx` files.
- Use `CardGrid` to layout multiple `Card` items.

### Example

```mdx
---
title: Cards Example
---

import { Card, CardGrid } from '@astrojs/starlight/components';

<CardGrid stagger>
  <Card title="Update content" icon="pencil">
    Edit `src/content/docs/index.mdx` to see this page change.
  </Card>
  <Card title="Add new content" icon="add-document">
    Add Markdown or MDX files to `src/content/docs` to create new pages.
  </Card>
  <Card title="Configure your site" icon="setting">
    Edit your `sidebar` and other config in `astro.config.mjs`.
  </Card>
  <Card title="Read the docs" icon="open-book">
    Learn more in the Starlight documentation.
  </Card>
</CardGrid>
```

### Props

- **Card**: `title` (string), `icon` (string), `href` (optional), `children` (content)
- **CardGrid**: `stagger` (optional boolean)

## Adding your own components

- Create components under `src/components/` (e.g., Astro, React, or preact components).
- Import and use them directly in `.mdx` pages.
- Document them by adding a new page to this Reference section with examples and props tables.