# Claude Skills

| Skill | Purpose |
| ----- | ------- |
| [`motion-doctrine`](skills/motion-doctrine/SKILL.md) | Gateway motion law for HyperFrames videos — vector law, the current, Seam Gate, no idle wobble. Load first. |
| [`cut-the-curve`](skills/cut-the-curve/SKILL.md) | Technique catalog: zoom-through, inverse zoom, cut-the-curve, waterfall cut/entry, rack-focus, nudge curve. |
| [`oversized-cursor`](skills/oversized-cursor/SKILL.md) | House-style oversized cursor as an eye-carrier and click-ignition device. |
| [`captions-overlay`](skills/captions-overlay/SKILL.md) | Caption model (drop / rail / embed) and the captions-as-overlay rule. |
| [`changelog-video`](skills/changelog-video/SKILL.md) | Pipeline turning a weekly changelog .md into a branded changelog video. |

## Install as a Claude Code plugin

```
/plugin marketplace add Alphajuliet85/Claude-skills
/plugin install claude-skills@claude-skills
```

## Hooks

`hooks/hooks.json` adds a pre-commit guard: before any `git commit` Claude runs, it
runs `bun run build`, `bun run lint`, and typecheck, and blocks the commit on failure.
It only activates inside a repo whose `package.json` name is `hyperframes-monorepo`;
everywhere else it exits silently.
