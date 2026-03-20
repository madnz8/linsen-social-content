## Files

- `system_prompt.md`: controls how the LinkedIn post is written.
- `config.json`: controls source filtering rules.
- `pillars.json`: controls the research pillars and keyword sets.

## JSON fields

### `config.json`
- `allowSocialSources`: if `true`, social domains are allowed; if `false`, social domains are excluded.
- `blockedDomains`: list of domains to always exclude from research results.

### `pillars.json`
- `pillars`: list of research pillars.
- `name`: pillar label shown in the automation.
- `keywords`: search terms used to find article candidates for that pillar.
