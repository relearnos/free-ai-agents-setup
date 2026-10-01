a/D:\My Second Brain\free-ai-agents-setup\README.md → b/D:\My Second Brain\free-ai-agents-setup\README.md
@@ -0,0 +1,122 @@
+# Free AI Agents Setup Guide
+
+A beginner-friendly, step-by-step guide for running **Hermes Agent**, **Claude Code**, and **Codex CLI** on **free local AI models** — no API bill, no subscription, no credit card.
+
+Everything runs on your own machine through [OmniRoute](https://github.com/diegosouzapw/OmniRoute), a free MIT-licensed local gateway that rotates across hundreds of AI providers and auto-falls-back the moment one hits its limit.
+
+**Live site:** `https://YOURNAME.github.io/free-ai-agents-setup/`
+*(replace with your deployed URL — see Deploy below)*
+
+---
+
+## What's inside
+
+The whole guide is one self-contained HTML file. No build step, no dependencies, no bundler. Open `index.html` in any browser and it works.
+
+| Part | Covers |
+|---|---|
+| 1 | Install **Node.js** (22.22.2+ / 24.x) — Windows & macOS tabs |
+| 2 | Install & start **OmniRoute** — the keep-window-open warning |
+| 3 | Connect a **free provider** + create your API key |
+| 4 | Connect your agent — **Hermes** · **Claude Code** · **Codex**, each with Win/macOS steps |
+| 5 | **Troubleshooting** — 7 real failure modes with fixes |
+| 6 | **9Router** as the OmniRoute alternative + comparison table |
+
+Features:
+- 🌙 Dark/light theme toggle
+- 📋 Copy button on every code block
+- 🪟🍎 Windows / macOS tabs on every section
+- 🔴🟠🟢 Colour-coded per-agent panels (Hermes red, Claude orange, Codex green)
+
+---
+
+## The three gotchas this guide exists to solve
+
+1. **Hermes needs ≥64K context.** Leave the Context field at its 16000 default and Hermes refuses to start with *"context window below the minimum 64,000."* The guide sets it to `131072`.
+2. **Codex v0.137+ reads `config.toml` only.** The legacy `config.yaml` is **silently ignored** — no error, just nothing happening.
+3. **Claude Code uses the gateway *root*, not `/v1`.** Adding `/v1` breaks it. This is the exact opposite of the Hermes and Codex settings, which is why it trips people up.
+
+---
+
+## Quick start (copy-paste)
+
+```bash
+# 1. Install Node.js 22.22.2+ or 24.x from https://nodejs.org
+
+# 2. Install + start OmniRoute (keep this window open)
+npm install -g omniroute
+omniroute
+# dashboard → http://localhost:20128
+
+# 3. Connect a free provider in the dashboard, then create an API key
+#    → Endpoints → Create API Key
+
+# 4. Point your agent at it (see guide for per-agent config)
+```
+
+---
+
+## Deploy
+
+### GitHub Pages (free, permanent — recommended)
+
+```bash
+git init
+git add index.html README.md
+git commit -m "Add free AI agents setup guide"
+git branch -M main
+git remote add origin https://github.com/YOURNAME/free-ai-agents-setup.git
+git push -u origin main
+```
+
+Then in the repo: **Settings → Pages → Source: `main` / `root` → Save.**
+
+Live in ~1 minute at `https://YOURNAME.github.io/free-ai-agents-setup/`
+
+### Netlify Drop (fastest — 5 minutes, no repo)
+
+1. Go to [netlify.com/drop](https://netlify.com/drop)
… omitted 44 diff line(s) across 1 additional file(s)/section(s)
