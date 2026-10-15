---
id: <REPO>-STD-001
title: "<Repository> Documentation Standards"
status: draft
---

# <Repository> Documentation Standards

Applies to everything under `docs/`. The root `README.md` is a short entry point and has no header.

The goal is docs that stay correct with little effort. Git already records who changed what and when, so the docs do not duplicate that.

## Header

Every governed document starts with this YAML header and nothing before it:

```yaml
---
id: <REPO>-<AREA>-NNN
title: "<Matches the H1 heading>"
status: draft
---
```

| Field | Rule |
| --- | --- |
| `id` | Permanent and unique, `<REPO>-<AREA>-NNN`. Never reused, even if the file moves. |
| `title` | Matches the H1 heading. **Keep it quoted** — an unquoted `:` breaks the header. |
| `status` | `draft`, `proposed`, `accepted` or `superseded`. |

No other fields. When a document replaces another, say so in its first paragraph and set the old one to `superseded`.

Status describes the **text**, not the software. Whether something is implemented is recorded only as evidence against the checks. A document never claims a feature works.

## One source of truth per topic

Each rule lives in exactly one document; others link to it instead of restating it.

| Topic | Owner |
| --- | --- |
| Product purpose, users, goals, boundaries | `product.md` |
| Phase order and milestones | `roadmap.md` |
| Feature behavior and boundaries | `specs/` |
| System structure and flows | `architecture.md` |
| Pass/fail checks and recorded results | `evidence.md` |
| Rationale for a hard-to-reverse choice | `adr/` |
| End-user tasks | `user-guide.md` |

Adjust the table to the documents this repository actually has. If you find the same rule in two places, delete one and link to the other.

## Changing documents

- Status lifecycle: `draft` → `proposed` (open for review) → `accepted` (maintainer approved) → `superseded`. A substantive edit to an accepted doc puts it back to `proposed` until re-approved.
- Changes that alter a public contract (file format, API, save format, dependency direction, protocol) need an ADR or an ADR update in the same PR.
- New documents: copy a template from the org template repository, pick a new ID, add a line to the [index](./README.md).
- Write plain English: full sentences, defined terms, no unexplained abbreviations.

## Review checklist

- [ ] Header has `id`, `title`, `status`; ID is unique.
- [ ] Relative links resolve.
- [ ] No rule duplicated from its owning document.
- [ ] No claim that something is implemented or passing without linked evidence.
- [ ] Contract changes carry an ADR.
