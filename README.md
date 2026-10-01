# my-claude-skills

My Claude Code plugin marketplace. Each skill is its own plugin, so install only the ones you need.

## Setup (once per computer)

In Claude Code:

```
/plugin marketplace add wkk023/my-claude-skills
```

Then install what you want:

```
/plugin install design-taste-frontend@my-claude-skills
/plugin install web-design-guidelines@my-claude-skills
/plugin install image-to-code@my-claude-skills
/plugin install design-md-library@my-claude-skills
/plugin install playwright-cli@my-claude-skills
```

Run `/plugin` to browse what's available. To get updates: `/plugin marketplace update my-claude-skills`.

### Claude Code on the web (cloud sessions)

Cloud sessions start fresh each time. Add these lines to the environment's **Setup script** (environment menu in the session title bar → Edit) and every new session gets the skills, whatever repo it works on:

```bash
claude plugin marketplace add wkk023/my-claude-skills || true
claude plugin install design-taste-frontend@my-claude-skills || true
claude plugin install web-design-guidelines@my-claude-skills || true
# add one line per plugin you want
```

## Plugins

| Plugin | What it does | Source |
|---|---|---|
| `design-taste-frontend` | Anti-slop rules for landing pages and portfolios: design read, dials, layout/typography/color bans, pre-flight checklist | [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) @ `ce26fc2` (MIT) |
| `web-design-guidelines` | Audits UI code against Vercel's Web Interface Guidelines, output as `file:line` findings. Includes an offline copy of the rules | [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills) @ `063bee9` (MIT) |
| `image-to-code` | Image-first workflow: generate section mockups, analyze them, then build to match. Written for tools with image generation | [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) @ `ce26fc2` (MIT) |
| `design-md-library` | 74 DESIGN.md design systems (Stripe, Linear, Vercel, Apple, Notion...) to build "in the style of" | [VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md) @ `f696123` (MIT) |
| `playwright-cli` | Drive a real browser: screenshots, dark mode, reduced motion, mobile, console errors, tests | [microsoft/playwright-cli](https://github.com/microsoft/playwright-cli) @ `b85c7a7` (Apache-2.0) |

Each skill folder keeps its upstream license.

## Adding a skill

1. Create `plugins/<name>/.claude-plugin/plugin.json` and `plugins/<name>/skills/<name>/SKILL.md`.
2. Add an entry to `.claude-plugin/marketplace.json`.
3. Check it with `claude plugin validate .`
