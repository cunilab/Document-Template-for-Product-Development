# Security — <Product / System>

| Field | Value |
| --- | --- |
| Scope | <product/service/subsystem> |
| Last reviewed | YYYY-MM-DD |

<!-- Use this when the product handles accounts, permissions, sensitive data, payments, secrets, devices, or exposed interfaces. Focus on real risks. -->

## Security Goals

- Protect <data/resource> from <unauthorized action>.
- Ensure only <actor> can <sensitive action>.
- Preserve <availability/integrity/privacy requirement>.

## Sensitive Data

| Data | Sensitivity | Stored where | Retention |
| --- | --- | --- | --- |
| <e.g. account email> | Low / Medium / High | <location> | <duration> |
| <e.g. access token> | High | <location> | <duration> |

## Access Model

| Actor | Can access | Cannot access |
| --- | --- | --- |
| <User> | <own resources> | <other users' resources> |
| <Admin/service> | <required access> | <explicit boundary> |

## Risks & Controls

| Risk | Impact | Control | Status |
| --- | --- | --- | --- |
| <Unauthorized access> | <what could happen> | <auth/authorization/control> | Covered / Gap |
| <Data exposure> | <what could happen> | <encryption/redaction/control> | Covered / Gap |
| <Abuse or brute force> | <what could happen> | <rate limit/control> | Covered / Gap |

## Security Checklist

<!-- Keep only checks relevant to this product. -->

- [ ] Authentication is required where needed
- [ ] Authorization is checked server-side / at the trusted boundary
- [ ] Secrets are not stored in source code
- [ ] Sensitive input is validated
- [ ] Sensitive data is not unnecessarily logged
- [ ] Dependencies and exposed interfaces have an update/review path
- [ ] Recovery exists for compromised credentials or keys

## Known Gaps

- [ ] **<Gap>** — <risk and planned mitigation>
- [ ] **<Gap>** — <risk and planned mitigation>

<!-- An accepted gap should be explicit. Do not pretend every risk is solved. -->
