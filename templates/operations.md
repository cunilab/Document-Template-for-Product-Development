# Operations — <Product / Service>

| Field | Value |
| --- | --- |
| Environment | Production / Staging / Local |
| Service | <name> |
| Owner | <person/team> |
| Production URL | <URL or N/A> |

<!-- Use this when someone may need to deploy, monitor, recover, or troubleshoot the product. Do not put secrets in this file. -->

## Run / Deploy

### Start

```sh
<command to start or deploy>
```

### Verify

```sh
<command or URL used to verify success>
```

**Expected:** <healthy result>

## Configuration

| Setting | Required | Source | Purpose |
| --- | --- | --- | --- |
| `<VARIABLE>` | Yes | Secret/env/config | <what it controls> |
| `<VARIABLE>` | No | Env/config | <what it controls> |

## Health & Monitoring

| Signal | Healthy | Where to check |
| --- | --- | --- |
| <Health endpoint> | <expected status> | <URL/tool> |
| <Error rate/logs> | <expected condition> | <tool/location> |
| <Critical dependency> | <expected condition> | <tool/location> |

## Backup & Recovery

<!-- Delete if the product has no persistent state. -->

| Item | Backup | Restore |
| --- | --- | --- |
| <Database/data> | <frequency/location> | <short restore method> |
| <Files/config> | <frequency/location> | <short restore method> |

### Recovery Check

- [ ] Restore process is documented
- [ ] A restore has been tested
- [ ] Critical data loss window is understood

## Common Problems

### <Problem / symptom>

**Symptoms**
- <what someone sees>

**Check**
```sh
<diagnostic command or check>
```

**Fix**
1. <action>
2. <action>
3. Verify <healthy condition>.

## Incident Quick Steps

1. Confirm user impact.
2. Check recent deploys and critical dependencies.
3. Stop or roll back the harmful change if needed.
4. Restore service/data if needed.
5. Record the cause and follow-up work.

<!-- Add product-specific steps when generic ones are insufficient. -->
