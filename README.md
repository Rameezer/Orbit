# ORBIT — Intelligence Companion

An ambient intelligence companion that's already working when you arrive. No prompts. No waiting. ORBIT scans the live web, finds the most interesting signal in the world today, and presents a fully researched episode — before you've typed a single word.

## What it does

- **Boots itself** — live web search runs on open, episode ready within seconds
- **One voice** — clear, sharp, plain-English intelligence on finance, geopolitics, tech, culture
- **Ambient conversation** — react, question, redirect, go deeper. No command interface.
- **Redirect** — say "take me to climate" or "explore AI regulation" and ORBIT rebuilds
- **Publishes everywhere** — Blog, Long Post, Email, X Thread, Instagram. One click.

## Stack

- Pure HTML/CSS/JS — zero dependencies, zero build step
- Anthropic Claude API (`claude-sonnet-4-20250514`) with web search tool
- Vercel static hosting

## Setup

1. Clone this repo
2. Open `index.html` in VS Code
3. The Anthropic API key is handled by Claude.ai's artifact environment
4. Push to GitHub → Vercel auto-deploys

## For standalone deployment

If deploying outside Claude.ai artifacts, you'll need to proxy the Anthropic API call
through a serverless function (since API keys can't live in client-side JS).

See `/api/chat.js` for a ready-made Vercel serverless proxy.

## Project structure

```
orbit/
├── index.html        # The entire app — self-contained
├── vercel.json       # Vercel deployment config
├── api/
│   └── chat.js       # Serverless proxy for Anthropic API (for standalone deploy)
└── README.md
```

## Roadmap

- [ ] User accounts + episode history
- [ ] Personalisation layer (interests, domains)
- [ ] Public episode feed (the daily intelligence layer)
- [ ] Multi-user access (ORBIT for everyone)
- [ ] Mobile app
