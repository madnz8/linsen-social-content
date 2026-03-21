## Files

- `system_prompt.md`: controls how the LinkedIn post is written.
- `config.json`: controls source filtering rules and active run days.
- `pillars.json`: controls the research pillars and keyword sets.

## JSON fields

### `config.json`
- `allowSocialSources`: if `true`, social domains are allowed; if `false`, social domains are excluded.
- `blockedDomains`: list of domains to always exclude from research results.
- `daysOfWeek`: controls which weekdays the automation is allowed to run.
- `monday` / `tuesday` / `wednesday` / `thursday` / `friday` / `saturday` / `sunday`: set `true` to allow runs on that day, `false` to skip.

### `pillars.json`
- `pillars`: list of research pillars.
- `name`: pillar label shown in the automation.
- `keywords`: search terms used to find article candidates for that pillar.

## Notes
- If `config.json` is invalid or unreachable, the automation falls back to local defaults.
- Default fallback schedule: run on Monday only.
- Manual test runs can still be forced from Trigger.dev with `forceRun: true`.
