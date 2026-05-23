# Ariel Sama

McCombs MBA (2026) · Austin, TX

I work where business judgment, operational discipline, and AI fluency meet — primarily on product and strategy problems with real operational depth.

## How I work with AI

I'm building out a deliberate dual-agent workflow on my project work:

- **Codex CLI (OpenAI)** for planning, review, and supervision
- **Claude Code (Anthropic)** for execution on the laptop and on production servers
- I broker between them — deciding what crosses, what gets revised, and what reaches the codebase

With real money on the line and AI-assisted code, having a second AI review changes feels like basic risk control. I'm still calibrating where it adds the most value.

## Trading bot

Multi-strategy live trading system running on a DigitalOcean droplet against modest real capital — equities through Alpaca, crypto through Coinbase. Built using the workflow above.

The paper-trading bot has a first operational layer in place:

- **Pushover** alerts on order failures and unexpected crashes (`notifier.py`)
- **Healthchecks.io** dead-man's-switch via a 1-minute heartbeat — 39,000+ pings since deployment
- A dedicated `HEARTBEAT` log line independent of market or position state, so silent stalls are caught the same way as crashes

Paper proves the pattern, then promotion goes to live, then crypto — not all at once.

On separating the heartbeat helper from the notifier:

> notifier.py is for user-facing alert events. A healthcheck ping is a machine-facing liveness signal that happens every minute whether anything interesting occurred or not. Different purpose, different cadence — keeping them separate ages better.

**Stack:** Python, pandas, Alpaca + Coinbase APIs, systemd on DigitalOcean, Pushover, Healthchecks.io.

## Other public work

- **[`fintech-shortcourse-harvard`](https://github.com/CodeSpaniard/fintech-shortcourse-harvard)** — Capstone and coursework from the FinTech short course (Harvard VPAL × GetSmarter): financial innovation, blockchain, digital payments, AI in finance.
- **[`postgrad-data-science-portfolio`](https://github.com/CodeSpaniard/postgrad-data-science-portfolio)** — Portfolio from my postgraduate program in data science and business analytics.

---

📍 Austin, TX · open to remote and relocation
Currently open to Strategy, Operations, and Product roles.

