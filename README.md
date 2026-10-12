# renovate-config

Shared [Renovate](https://docs.renovatebot.com/) preset for `bronweg` repositories.

Use it from a repo's `renovate.json`:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>bronweg/renovate-config"]
}
```

## Policy (`default.json`)

- Schedule: weekends (Asia/Jerusalem); security updates any time.
- Releases must be at least 3 days old before an update is proposed.
- Stable (>=1.0) minor/patch updates and digest/pin updates: one grouped "non-major dependencies" PR, automerged.
- Pre-1.0 minor/patch updates: separate "pre-1.0 dependencies" group, manual review.
- Major updates: one PR each, manual review.
