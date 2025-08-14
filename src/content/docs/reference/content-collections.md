---
title: Content Collections
description: The `docs` collection and frontmatter used in this site.
---

This project defines a `docs` content collection using Starlight’s loader and schema.

## Definition

- File: `src/content.config.ts`
- Export: `collections.docs = defineCollection({ loader: docsLoader(), schema: docsSchema() })`

```ts
// src/content.config.ts (excerpt)
import { defineCollection } from 'astro:content';
import { docsLoader } from '@astrojs/starlight/loaders';
import { docsSchema } from '@astrojs/starlight/schema';

export const collections = {
  docs: defineCollection({ loader: docsLoader(), schema: docsSchema() }),
};
```

## File locations and routes

- Place `.md` or `.mdx` files under `src/content/docs/`.
- File paths map to routes. For example, `src/content/docs/guides/example.md` → `/guides/example/`.

## Common frontmatter fields

- **title**: Page title.
- **description**: Short description for listings and SEO.
- **template**: Optional page layout, e.g., `splash`.
- **hero**: Optional hero configuration for splash pages.

### Example (splash page)

```md
---
title: Welcome to Starlight
description: Get started building your docs site with Starlight.
template: splash
hero:
  tagline: Congrats on setting up a new Starlight project!
  image:
    file: ../../assets/houston.webp
  actions:
    - text: Example Guide
      link: /guides/example/
      icon: right-arrow
    - text: Read the Starlight docs
      link: https://starlight.astro.build
      icon: external
      variant: minimal
---
```

### Example (guide)

```md
---
title: Example Guide
description: A guide in my new Starlight docs site.
---
```

## Authoring tips

- Use `.mdx` when you need to import and use components.
- Keep frontmatter concise; detailed context belongs in the body content.