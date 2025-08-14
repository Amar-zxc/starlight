---
title: Project APIs Overview
description: Public APIs, functions, and extension points exposed by this project.
---

This starter does not define any custom runtime APIs or exported functions beyond configuration. It is meant as a foundation for your docs site.

- Add your own libraries, utilities, and components under `src/`.
- Re-export or document them here under the Reference section as you build them.

## Current public surface

- **Astro config**: `astro.config.mjs` configures Starlight and the sidebar.
- **Content collections**: `src/content.config.ts` defines the `docs` collection via Starlight’s schema.
- **Starlight components**: You can import UI components like `Card` and `CardGrid` in MDX.

## How to add your own public API

1. Create modules under `src/` (e.g., `src/lib/formatters.ts`).
2. Export the functions or components you intend to reuse.
3. Document them by adding a new page to `src/content/docs/reference/`.

Example module:

```ts
// src/lib/formatters.ts
export function formatTitle(input: string): string {
  return input.trim().replaceAll('-', ' ').replace(/\s+/g, ' ');
}
```

Example reference doc skeleton for a new function:

```md
---
title: formatTitle()
description: Normalize and prettify a string for display.
---

## Signature

```ts
function formatTitle(input: string): string
```

## Parameters

- input: string — Raw string to normalize.

## Returns

- string — A human-readable title string.

## Examples

```ts
formatTitle('hello-world'); // "hello world"
formatTitle('  many   spaces   '); // "many spaces"
```
```