## How Topic Selection Works

The automation uses `pillars.json` as a guide for what kind of content to look for. Each pillar represents a strategic theme, and its keywords help the system search for relevant articles and posts online.

Every day, the automation searches for recent content related to those pillars, removes sources that are blocked in `config.json`, and then asks AI to choose the best topics for LINSEN. The AI does not just pick random links: it tries to find strong, relevant, and varied ideas that fit the LINSEN positioning.

The automation also keeps a memory of topics that were already selected in previous runs. This helps reduce duplicates over time, so it is less likely to suggest the same angle again. The memory is not perfect, but it is designed to avoid obvious repetition while keeping the system simple and flexible.

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
