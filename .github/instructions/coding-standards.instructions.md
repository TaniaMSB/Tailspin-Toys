---
description: 'Commenting, documentation, and TypeScript coding standards'
applyTo: '**/*.{ts,astro}'
---

# Coding Standards

## Comments

Comments should explain why code exists, including intent, trade-offs, and
non-obvious decisions. Do not restate what the code already says. Prefer clear
names and straightforward code over comments that narrate mechanics.

Keep comments current. When changing the code a comment describes, update or
remove that comment in the same change. Do not add comments only to satisfy a
minimum comment count.

## Data-Layer Documentation

Every exported function in `db/` and `src/lib/` must have a TSDoc/JSDoc comment
that describes:

- the function's purpose;
- each parameter, including the injectable `db` argument used by data-access
  helpers; and
- the return value.

Use `@param` and `@returns` tags when the signature or surrounding text does
not make those details unambiguous. Keep the documentation focused on the
public contract rather than implementation steps.

## Astro Component Contracts

Every reusable `.astro` component must define and document its `Props`
interface. The documentation should explain what each prop controls, including
optional values and defaults. Extend Astro's or the platform's attribute types
when forwarding HTML attributes instead of duplicating those attributes.

## TypeScript Formatting

Use the existing project style consistently:

- four-space indentation;
- single quotes for strings in TypeScript;
- semicolons at statement endings;
- trailing commas in multiline objects, arrays, and parameter lists; and
- explicit parameter and return types for exported data-layer functions.

Run ESLint after TypeScript or Astro changes. ESLint enforces the repository's
TypeScript safety rules, including unused-variable handling; formatting and
documentation conventions are reviewed alongside the lint result.
