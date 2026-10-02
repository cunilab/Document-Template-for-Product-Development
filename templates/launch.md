# Launch — <Release / Product>

| Field | Value |
| --- | --- |
| Release | <v1.0 / launch name> |
| Target | YYYY-MM-DD |
| Owner | <name/team> |
| Status | Planning / Ready / Launched |

<!-- Use this only when a release needs coordination or a launch mistake would matter. -->

## Launch Scope

### Shipping

- <Capability/release item>
- <Capability/release item>

### Not Shipping

- <Explicitly excluded item>
- <Deferred item>

## Go / No-Go

### Product

- [ ] Critical user flow works end-to-end
- [ ] Known launch-blocking bugs are resolved or explicitly accepted
- [ ] User-facing copy/content is ready

### Technical

- [ ] Required tests pass
- [ ] Production configuration is ready
- [ ] Data migrations or compatibility changes are verified
- [ ] Monitoring/health checks are available

### Recovery

- [ ] Rollback or recovery path is known
- [ ] Backup is available when release changes critical data

### Communication

<!-- Delete if no announcement/support coordination is needed. -->

- [ ] Release notes / announcement ready
- [ ] Support or affected teams know what is changing

## Release Steps

1. <Pre-release action>
2. <Deploy/publish/distribute>
3. <Verify critical flow>
4. <Enable/announce if applicable>

## Rollback

**Rollback if:** <clear condition that makes the launch unsafe>

1. <Disable/revert>
2. <Restore data/config if needed>
3. Verify <previous healthy state>.

## After Launch

- [ ] Check health/errors after release
- [ ] Verify critical user flow in production
- [ ] Collect important feedback/issues
- [ ] Review success signal(s)
- [ ] Move unfinished work back to roadmap/backlog

## Result

<!-- Fill this after launch. -->

**Launched:** <date / not launched>  
**Outcome:** <what happened>  
**Follow-up:** <issue/decision/next milestone>
