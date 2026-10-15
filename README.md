# Product Development Document Templates

The org-wide documentation standard for cunilab. Reusable Markdown templates for product documentation without turning documentation into another product.

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

## Document Header

Every governed document — everything under `docs/` — starts with this YAML header and nothing before it:

```yaml
---
id: <REPO>-<AREA>-NNN
title: "<Matches the H1 heading>"
status: draft
---
```

| Field | Rule |
| --- | --- |
| `id` | Permanent and unique: `WFT-ARCH-001`, `KVR-ADR-003`. Never reused, even if the file moves. |
| `title` | Matches the H1 heading. **Keep it quoted** — an unquoted `:` breaks the header. |
| `status` | `draft`, `proposed`, `accepted`, or `superseded`. No other fields. |

- The root `README.md` is a short entry point and **has no header**. Governance starts when `docs/` exists.
- Status describes the **text**, not the software. Whether something works is recorded only as evidence; a document never claims a feature works.
- Lifecycle: `draft` → `proposed` (open for review) → `accepted` (maintainer approved) → `superseded`. A substantive edit to an accepted document puts it back to `proposed` until re-approved.

Copy [templates/document.md](templates/document.md) to start a governed document. Copy [templates/standards.md](templates/standards.md) into `docs/standards.md` to install the full governance rules in a repository.

## Which Template Do I Need?

| Situation | Template |
| --- | --- |
| A new document with no better-fitting template | [Document](templates/document.md) |
| People need to understand or run the project | [README](templates/readme.md) |
| Documents exist but have no index | [Docs index](templates/index.md) |
| A repository needs rules for writing and changing documents | [Standards](templates/standards.md) |
| Product purpose, users, goals, or boundaries are becoming unclear | [Product](templates/product.md) |
| Product has multiple releases, phases, or meaningful milestones | [Roadmap](templates/roadmap.md) |
| A feature is too complex or ambiguous for a normal issue | [PRD](templates/prd.md) |
| An important choice and its reasoning should survive | [ADR](templates/adr.md) |
| System structure is difficult to understand from code alone | [Architecture](templates/architecture.md) |
| A claim must be proven before release | [Evidence](templates/evidence.md) |
| End users must install, use, or troubleshoot the product | [User guide](templates/user-guide.md) |
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
├── README.md          # docs index
├── product.md
└── roadmap.md
```

### Product with more complexity

```text
README.md

docs/
├── README.md
├── standards.md
├── product.md
├── roadmap.md
├── specs/
│   └── feature-name.md
├── adr/
│   └── 0001-important-decision.md
├── evidence.md
├── architecture.md
├── security.md
└── operations.md
```

Add `launch.md` when a release needs explicit launch coordination, and `user-guide.md` when end users install or operate the product themselves.

## Recommended Flow

```text
README
  |
  +--> Docs index + Standards (once docs/ exists)
         |
         +--> Product (when purpose/scope needs to be explicit)
                |
                +--> Roadmap (when there are multiple milestones)
                       |
                       +--> PRD (when a feature needs deeper specification)
                              |
                              +--> Build

Important choice?     --> ADR (docs/adr/NNNN-slug.md)
Claims need proof?    --> Evidence
Complex system?       --> Architecture
Meaningful risk?      --> Security
End users involved?   --> User guide
Running service?      --> Operations
Coordinated release?  --> Launch
```

## Rules

- **Do not create every template.**
- **Do not duplicate the same information across documents. One source of truth per topic: link, don't restate.**
- **Roadmap = milestones and outcomes, not every task.**
- **PRD = feature behavior and boundaries, not implementation diary.**
- **ADR = why a choice was made, not meeting notes.**
- **Evidence = what was proven and how, not plans or aspirations.**
- **Architecture = important structure and flows, not every class/module.**
- **Security = real risks and controls, not a generic compliance dump.**
- **Operations = actions someone may actually need during production.**
- **A document never claims a feature works without linked evidence.**
- **Delete stale documentation or update it.**

**Documentation should grow with product complexity, not ahead of it.**
