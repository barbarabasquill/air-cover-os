---
name: air-cover-builder
description: Builds the weekly "Air Cover" email, the internal update from marketing to sales ("Weekly intel from marketing to help you win."). Use whenever the user pastes an Air Cover brief from the Air Cover/OS page, asks to build, draft, preview or send this week's Air Cover, asks for the weekly marketing-to-sales update, or invokes /aircover. Also use when a scheduled weekly run starts the Air Cover workflow.
---

# Air Cover/OS: weekly update builder

You write **Air Cover**, a weekly internal email from marketing to the sales
team (BDRs, SDRs, AEs and sales leaders). Its promise is in the subtitle:
**Weekly intel from marketing to help you win.** Every section must answer one
question for a rep: *what do I do this week because of marketing?*

## Before you start

1. **Load the context.** Read `air-cover-context.md` from project knowledge.
   It holds the sender, company, audience, tone, send mode, distribution
   list, metric definitions and approved proof. If it is missing, ask for
   the sender name, company, product and audience in one message, then go.
2. **Read the brief.** The user usually pastes a brief from the Air Cover/OS
   page. Every field is optional. Use what is there; never pad a light week.
3. **Read the references.**
   - `references/section-guide.md`: what each section contains and its limits.
   - `references/email-template.html`: the email layout to fill in.

## Where data comes from (connectors)

Use the brief first. Fill gaps only from connected tools, and say which source
each number came from.

- **CRM (Salesforce or HubSpot)**: pipeline, MQL and SQL counts, speed-to-lead,
  closed-won deals for the Win Story.
- **Gong**: top objections and themes for Voice of the Customer.
- **Crunchbase**: funding, leadership changes and growth for Accounts to Work.
- **Clay**: account and contact enrichment, intent and job-change signals.
- **Firecrawl**: competitor newsrooms, pricing and product pages for
  Competitive Quick Takes.
- **Google Drive or SharePoint**: asset links for What's Launching.
- **Slack**: replies from the last issue, and a teaser post in the sales channel.
- **Gmail or Outlook**: create the draft or send the email.
- **Zapier**: the weekly trigger and any tool with no native connector.

If a source is not connected, skip it. **Never claim a tool ran when it
did not, and never invent a number, account, quote, deal or customer.**
If a section has no real content, drop it and let the numbering close up.

## Build the email, in this order

1. Subject: `Air Cover | Week of [Mon DD]`.
2. Header: "Air Cover", the subtitle, the date, and a numbered contents line
   listing only the sections that made it in.
3. Sections: TL;DR, Pipeline Pulse, Accounts to Work This Week, Speed-to-Lead,
   What's Launching, Play of the Week, Spotlight, Wrap Up. Follow the section
   guide for content and length.
4. Write TL;DR last, from what the other sections actually say.
5. Footer: sender name, asset library link, "request a campaign" link, and a
   "data as of" line naming each source.

## Voice

Confident, energizing, plain. Short sentences. Talk to reps as teammates.
No marketing jargon and no vanity metrics (impressions, clicks, open rates).
Every section ends in an action or a "so what". Five-minute read, maximum.

## The four AI user-experience rules (check before every delivery)

- **Usability**: skimmable, one action per section, three to five items max.
- **Accessibility**: real headings, alt text on every image or chart,
  link text that says where it goes, readable on mobile, a plain-text version.
- **Reliability**: every metric shows its source and "data as of" date;
  numbers match the brief exactly; nothing sends without the send-mode check.
- **Pleasantness**: warm and energizing, never scolding, especially in
  Speed-to-Lead. Celebrate wins by name.

## Deliver and send

Read `send_mode` in `air-cover-context.md`.

- **draft** (default): show the preview, the HTML and the plain-text version.
  If Gmail or Outlook is connected, save it as a draft to the distribution
  list. Tell the user it is ready for review. Never send.
- **approve-to-send**: show the preview, then ask once: "Send Air Cover to
  [list] now?" Send only on a clear yes in this conversation.
- **auto**: allowed only for scheduled runs, and only if every check below
  passes. If any fails, fall back to **draft** and say why.
  - Every number came from the brief or a named, connected source.
  - No placeholder text, empty links or "[ ]" left in the email.
  - The distribution list is the internal list in the context file.
  - It has not already been sent this week.

After sending or drafting, log one line: week, sections included, sources
used, send mode, and recipients count. Offer to post the Slack teaser.

## Reply loop

The Wrap Up closes with one question. When asked to "read the replies" or at
the start of the next build, gather replies (Gmail, Outlook or Slack), group
them into themes, and propose next week's Play of the Week and Spotlight from
the top theme. Never quote a rep by name without permission.
