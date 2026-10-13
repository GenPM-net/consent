# @core/consent

[![genpm](https://api.genpm.net/v1/badge/@core/consent.svg)](https://genpm.net/p/@core/consent) ![license](https://img.shields.io/badge/license-MIT-blue)

> GDPR cookie consent: banner with equal reject/accept, categories, proof records, ConsentGate and Google Consent Mode v2

A [GenPM](https://genpm.net) module: **source code + AI rules + MCP config**, injected into your project instead of hidden in `node_modules`. The code lands in `src/lib/consent`, pinned to a verified commit, and you own it.

## Install

```bash
genpm add @core/consent
```

No genpm yet? `curl -fsSL https://genpm.net/install.sh | sh` (macOS/Linux), `irm https://genpm.net/install.ps1 | iex` (Windows), or one-off with `npx @genpm-net/cli add @core/consent`.

Or let your AI agent do it: run `genpm mcp setup` once, then ask *"add @core/consent with genpm"* in Claude Code, Cursor, VS Code, Windsurf, Codex or Gemini CLI. It shows you a dry-run plan before writing anything.

## What it does

Cookie consent that meets GDPR/ePrivacy: categories (necessary always on; analytics, marketing, preferences off by
default), a banner where "Reject all" is as prominent as "Accept all", a preferences center, proof of each decision
(`consent_records`: choices, policy version, date; no IP), server checks (`hasConsent`), a client `ConsentGate` and
Google Consent Mode v2 values. Changing `CONSENT_POLICY_VERSION` asks everyone again.

## At a glance

- **GenPM dependencies** (installed with it): [@core/db](https://genpm.net/p/@core/db)
- **npm dependencies** (proposed, never installed without asking): `zod`, `react`
- **Environment variables** (added to `.env.example`): `CONSENT_POLICY_VERSION`, `SITE_URL`, `CONSENT_COOKIE_DOMAIN`
- **AI rules**: [`AGENTS.md`](AGENTS.md), loaded by your agent only when it works in `src/lib/consent`

## Security

GenPM installs a 40-character commit SHA (never a branch), verifies an Ed25519-signed manifest, never runs install scripts and scans AI rules for prompt injection. Details: [genpm.net/docs/security](https://genpm.net/docs/security).

## License

MIT — see [LICENSE](LICENSE). Browse the full catalog at [genpm.net](https://genpm.net).
