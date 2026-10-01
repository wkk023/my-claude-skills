---
name: design-md-library
description: Library of 74 DESIGN.md files describing the visual language of well-known sites (Stripe, Linear, Vercel, Apple, Notion, Figma, Supabase, Raycast and more). Use when the user asks for a page or component "like <brand>", "in the style of <site>", wants a ready-made design system to start from, or wants to add a DESIGN.md to their project.
---

# DESIGN.md Library

Each file in `references/` is a plain-text design system (colors, type, spacing, components, do's and don'ts) extracted from a real product's public site. Source: [VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md) (MIT).

## How to use

1. **Pick the reference.** Match the brand the user named to a file in `references/` (e.g. "Linear-style" → `references/linear.app.md`). If they named none, suggest 2-3 that fit the brief and ask them to choose.
2. **Read the whole file** before writing any UI. Treat it as the design spec: tokens, type scale, radius, shadow and component rules.
3. **Apply it.** Either:
   - build directly from it, or
   - if the user wants the project to keep that look, copy it to the project root as `DESIGN.md` and reference it from `CLAUDE.md`.
4. **Keep it inspired, not cloned.** Use the design language, never the brand's logo, name, or copy. Do not build pages that impersonate the brand.

## Available systems

airbnb, airtable, apple, binance, bmw, bmw-m, bugatti, cal, claude, clay, clickhouse, cohere, coinbase, composio, cursor, dell-1996, elevenlabs, expo, ferrari, figma, framer, hashicorp, hp, ibm, intercom, kraken, lamborghini, linear.app, lovable, mastercard, meta, minimax, mintlify, miro, mistral.ai, mongodb, nike, nintendo-2001, notion, nvidia, ollama, opencode.ai, pinterest, playstation, posthog, raycast, renault, replicate, resend, revolut, runwayml, sanity, sentry, shopify, slack, spacex, spotify, starbucks, stripe, supabase, superhuman, tesla, theverge, together.ai, uber, vercel, vodafone, voltagent, warp, webflow, wired, wise, x.ai, zapier

## Pairs well with

- `design-taste-frontend`: its section 2 says to use a real design system when the brief matches one; these files are that system for brand-flavored briefs.
- `web-design-guidelines`: run it on the result to catch accessibility and UX issues.
