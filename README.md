# Air Cover/OS

**Weekly intel from marketing to help you win.**

Air Cover/OS builds **Air Cover**, a weekly internal email from marketing to the
sales team (BDRs, SDRs, AEs and sales leaders). Fill in simple fields for each
section, copy the brief into Claude, and the Air Cover/OS Claude Project writes
the email, fills gaps from connected tools and delivers it on your send mode.

Part of a portfolio of GTM agents: GTM/OS, ABM-ABX/OS, Sales Momentum/OS and Air Cover/OS.

## What's in each issue

| # | Section | What reps get |
|---|---|---|
| 1 | TL;DR | What moved, what's hot, what to do this week |
| 2 | Pipeline Pulse | Marketing-sourced pipeline vs. target, MQL and SQL trend |
| 3 | Accounts to Work This Week | Accounts with a signal, plus a suggested opener |
| 4 | Speed-to-Lead | Response time, untouched MQLs, next week's goal |
| 5 | What's Launching | Campaigns and content going live, with talk tracks |
| 6 | Play of the Week | One ready-to-use email, call opener or LinkedIn message |
| 7 | Spotlight | Rotating: Win Story, Competitive Quick Take, Voice of the Customer, Content Spotlight |
| 8 | Wrap Up | The week's story and one question back to sales |

## Repository

```
air-cover-os/
├── index.html                      Command Center page (fields, brief, email preview)
├── air-cover-context.md            Your setup: sender, list, send mode, metrics, proof
├── claude-project/
│   ├── PROJECT_INSTRUCTIONS.md     Paste into the Claude Project instructions
│   └── CONNECTORS.md               Which connectors to add and why
├── plugin/
│   ├── .claude-plugin/plugin.json  Plugin manifest
│   ├── .mcp.json                   Clay, Crunchbase, Firecrawl, Zapier
│   └── skills/air-cover-builder/
│       ├── SKILL.md                The Air Cover build and send workflow
│       └── references/
│           ├── section-guide.md    Content and limits for every section
│           └── email-template.html Email-safe layout Claude fills in
├── LICENSE
└── README.md
```

## Set up (about 15 minutes)

1. **Repo.** Create the private repo `air-cover-os` and upload these files.
2. **Page.** Deploy to Netlify (drag the folder in, or connect the repo).
   No build step: it's a single `index.html`.
3. **Claude Project.** Create a Project named "Air Cover/OS".
   - Paste `claude-project/PROJECT_INSTRUCTIONS.md` into its instructions.
   - Add `air-cover-context.md`, `section-guide.md` and `email-template.html`
     to its knowledge.
4. **Connectors.** Turn on the connectors in `claude-project/CONNECTORS.md`.
5. **Each week.** Open the page, fill in what you have, select **Copy brief**,
   paste it into the Project and say "Build this week's Air Cover."
6. **Autonomous.** Schedule the Monday run (a scheduled task in Claude, or a
   Zapier schedule), then move `send_mode` from `draft` to
   `approve-to-send` or `auto` when you trust the data.

## Built on four AI user-experience rules

- **Usability.** Every field is optional, one action per section, five-minute read.
- **Accessibility.** Labeled fields, keyboard focus, mobile layout; emails ship
  with real headings, alt text and a plain-text version.
- **Reliability.** No invented numbers, a source and "data as of" date on every
  metric, and a send-mode gate before anything leaves.
- **Pleasantness.** Energizing, teammate tone; Speed-to-Lead encourages, never scolds.

## License

Copyright © 2026 Barbara Basquill. All rights reserved.
