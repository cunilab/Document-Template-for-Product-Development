# Product Development Document Templates

Reusable Markdown templates for product documentation without turning documentation into another product.

## Principle

**Create a document only when it makes the product easier to understand, decide, build, release, or operate.**

A tiny product may need only a README. Add documents as complexity appears.

## How These Templates Work

The templates are designed to be **copied and filled in**, not used as question lists.

- Visible Markdown shows the final document structure.
- `<placeholders>` show what to replace.
- `<!-- comments -->` give guidance but disappear when rendered.
- Checklists show progress or verifiable requirements.
- Tables are used where comparison or structured facts are clearer than prose.
- Delete any section that adds no value.

## Which Template Do I Need?

| Situation | Template |
| --- | --- |
| People need to understand or run the project | [README](templates/readme.md) |
| Product purpose, users, goals, or boundaries are becoming unclear | [Product](templates/product.md) |
| Product has multiple releases, phases, or meaningful milestones | [Roadmap](templates/roadmap.md) |
| A feature is too complex or ambiguous for a normal issue | [PRD](templates/prd.md) |
| An important choice and its reasoning should survive | [Decision](templates/decision.md) |
| System structure is difficult to understand from code alone | [Architecture](templates/architecture.md) |
| Product has meaningful security risks | [Security](templates/security.md) |
| Someone must deploy, monitor, recover, or troubleshoot it | [Operations](templates/operations.md) |
| A release needs coordinated readiness and recovery | [Launch](templates/launch.md) |

## Documentation Test

Before creating a document, ask:

1. Will it clarify an important product or technical decision?
2. Will someone use it to build, operate, review, or coordinate work?
3. Will the information still matter after the current conversation or issue is gone?
4. Would losing this information create confusion, repeated work, or meaningful risk?

If every answer is **no**, do not create the document.

## Typical Growth

### Small project

```text
README.md
```

### Product with direction

```text
README.md

docs/
├── product.md
└── roadmap.md
```

### Product with more complexity

```text
README.md

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

Add `launch.md` when a release needs explicit launch coordination.

## Recommended Flow

```text
README
  |
  +--> Product (when purpose/scope needs to be explicit)
         |
         +--> Roadmap (when there are multiple milestones)
                |
                +--> PRD (when a feature needs deeper specification)
                       |
                       +--> Build

Important choice?     --> Decision
Complex system?       --> Architecture
Meaningful risk?      --> Security
Running service?      --> Operations
Coordinated release?  --> Launch
```

## Rules

- **Do not create every template.**
- **Do not duplicate the same information across documents.**
- **Roadmap = milestones and outcomes, not every task.**
- **PRD = feature behavior and boundaries, not implementation diary.**
- **Decision = why a choice was made, not meeting notes.**
- **Architecture = important structure and flows, not every class/module.**
- **Security = real risks and controls, not a generic compliance dump.**
- **Operations = actions someone may actually need during production.**
- **Delete stale documentation or update it.**

**Documentation should grow with product complexity, not ahead of it.**
