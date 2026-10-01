# Free AI Agents Setup Guide

A beginner-friendly, step-by-step guide for running **Hermes Agent**, **Claude Code**, and **Codex CLI** on free local AI models. No API bill, no subscription, no credit card.

Everything runs on your own machine through [OmniRoute](https://github.com/diegosouzapw/OmniRoute), a free MIT-licensed local gateway that rotates across hundreds of AI providers and falls back automatically the moment one hits its limit.

Live site: https://YOURNAME.github.io/free-ai-agents-setup/

Replace that URL with your deployed link. See the Deploy section below.

---

## What is inside

The whole guide is one self-contained HTML file. No build step, no dependencies, no bundler. Open index.html in any browser and it works.

| Part | Covers |
| --- | --- |
| 1 | Install Node.js 22.22.2+ or 24.x, with Windows and macOS tabs |
| 2 | Install and start OmniRoute, including the keep-window-open warning |
| 3 | Connect a free provider and create your API key |
| 4 | Connect your agent: Hermes, Claude Code, or Codex, each with Win and macOS steps |
| 5 | Troubleshooting, covering 7 real failure modes with fixes |
| 6 | 9Router as the OmniRoute alternative, plus a comparison table |

Features:

- Dark and light theme toggle
- Copy button on every code block
- Windows and macOS tabs on every section
- Colour-coded per-agent panels: Hermes red, Claude orange, Codex green

---

## The three gotchas this guide exists to solve

**1. Hermes needs 64K context or more.**

Leave the Context field at its 16000 default and Hermes refuses to start, showing "context window below the minimum 64,000". The guide sets it to 131072.

**2. Codex v0.137 and newer reads config.toml only.**

The legacy config.yaml file is silently ignored. No error, just nothing happening.

**3. Claude Code uses the gateway root, not /v1.**

Adding /v1 breaks it. This is the exact opposite of the Hermes and Codex settings, which is why it trips people up.

---

## Quick start

Install Node.js 22.22.2+ or 24.x from https://nodejs.org first.

Then install and start OmniRoute. Keep that window open:

```
npm install -g omniroute
omniroute
```

The dashboard is at http://localhost:20128

Next, connect a free provider in the dashboard, then create an API key under Endpoints, then Create API Key.

Finally, point your agent at it. The guide has the per-agent config for Hermes, Claude Code, and Codex.

---

## Deploy

### GitHub Pages (free and permanent, recommended)

Run these commands in the project folder:

```
git init
git add index.html README.md
git commit -m "Add free AI agents setup guide"
git branch -M main
git remote add origin https://github.com/YOURNAME/free-ai-agents-setup.git
git push -u origin main
```

Then in the repo: Settings, then Pages, then set Source to main and root, then Save.

Live in about a minute at https://YOURNAME.github.io/free-ai-agents-setup/

### Netlify Drop (fastest, about 5 minutes, no repo)

1. Go to https://app.netlify.com/drop
2. Drag the folder onto the page
3. Get your netlify.app link immediately

---

## Before you publish

Two edits worth making:

1. **Subscribe button.** In index.html the CTA button is a placeholder. Point it at your YouTube channel.
2. **Channel name.** The CTA card says "my channel" as generic copy. Put your real name in.

---

## Share it

Drop the live link in your YouTube comments:

> Full setup guide (free, step by step): [LINK]
>
> Runs Hermes Agent, Claude Code and Codex on free local models.
> No API bill, no subscription.
>
> Windows + macOS tabs. Covers the 64K context trap that breaks
> most Hermes setups, the Codex config.toml thing that fails silently,
> and the Claude Code /v1 gotcha.
>
> Stuck anywhere? Drop the error in the replies, I'll help.

Pin that comment so the link stays above the replies permanently.

---

## Credits and license

- [OmniRoute](https://github.com/diegosouzapw/OmniRoute), the local AI gateway, MIT licensed
- [9Router](https://github.com/decolua/9router), OmniRoute's parent project, covered as an alternative, MIT licensed
- [Hermes Agent](https://github.com/NousResearch/hermes-agent), by Nous Research

Guide content is free to share and remix. Tools mentioned are MIT licensed. **You are welcome to fork, translate, or republish this with attribution.**

Built for beginners. Everything runs locally on your own computer.
