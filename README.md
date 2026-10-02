# Product Development Document Templates

A small, reusable set of templates for documenting products without turning documentation into a project of its own.

## Principle

**Create a document only when it prevents confusion, preserves an important decision, coordinates work, or reduces meaningful risk.**

Do not copy every template into every product. Start small. Add documentation when the product needs it.

## Start Here

For most new products, begin with:

- [Product](templates/product.md) — why the product should exist.
- [Roadmap](templates/roadmap.md) — what matters now and what may come next.

Then add other documents only when a real need appears.

## Which document do I need?

| Situation | Template | Need |
| --- | --- | --- |
| Starting or clarifying a product | [Product](templates/product.md) | Core |
| Need shared direction and priorities | [Roadmap](templates/roadmap.md) | Core |
| Feature is complex, ambiguous, risky, or needs alignment | [PRD](templates/prd.md) | As needed |
| Important decision and reasoning should survive | [Decision](templates/decision.md) | As needed |
| System structure is difficult to understand from code/product docs | [Architecture](templates/architecture.md) | Optional |
| Product has meaningful security risks | [Security](templates/security.md) | Optional |
| Product must keep running after release | [Operations](templates/operations.md) | Optional |
| Preparing a coordinated release | [Launch](templates/launch.md) | Optional |

## Documentation Test

Before creating a document, ask:

1. Will it clarify **why or what** we are building?
2. Will it help people **coordinate**?
3. Will it preserve information we are likely to need later?
4. Will it reduce meaningful product, technical, security, or operational risk?

If every answer is **no**, do not create the document.

## Recommended Flow

```text
Product
  |
  +--> Roadmap
        |
        +--> PRD (when a feature needs specification)
              |
              +--> Build

Important decision? --> Decision record

Add only when needed:
complex system     --> Architecture
security concerns  --> Security
running service    --> Operations
real release       --> Launch
```

A roadmap is not a task list. A PRD is not required for every change. A decision record is not meeting notes.

## How to Use a Template

1. Copy only the template you need.
2. Rename it for the product or feature.
3. Delete sections that do not help.
4. Keep answers short unless detail changes a decision.
5. Update the document when reality changes.
6. If a document becomes stale and no longer provides value, fix it or remove it.

## Core Rule for Every Template

Each template contains:

> **Use this when:** the document provides clear value.  
> **Skip this when:** a smaller artifact already communicates enough.  
> **Delete sections that do not help.**

The templates are starting points, not forms that must be completed.

## Suggested Product Repository

A small product might need only:

```text
docs/
├── product.md
└── roadmap.md
```

A product with more complexity might grow into:

```text
docs/
├── product.md
├── roadmap.md
├── specs/
│   └── feature-name.md
├── decisions/
│   └── 001-important-decision.md
├── architecture.md
├── security.md
└── operations.md
```

**Documentation should grow with product complexity, not ahead of it.**
