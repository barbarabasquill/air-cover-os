# Air Cover/OS: connectors

Add these from the Connectors area in Claude, then turn them on in the
Air Cover/OS Project. Company tools (CRM, Gong, email, Slack) connect once you
are inside a company's stack; Air Cover works from the brief alone until then.

## Already connected
| Connector | What it adds to Air Cover |
|---|---|
| Clay | Account and contact enrichment, intent and job-change signals for Accounts to Work |
| Crunchbase | Funding, leadership changes and growth signals for Accounts to Work |
| Firecrawl | Competitor newsrooms, pricing and launch pages for Competitive Quick Takes |
| Zapier | The weekly Monday trigger, plus any company tool without a native connector |

## Add when you join a company (highest value first)
| Connector | Section it powers |
|---|---|
| Salesforce or HubSpot | Pipeline Pulse, Speed-to-Lead, Win Story, account owners |
| Gmail or Outlook | Saving the draft, sending to the list, reading replies |
| Gong | Voice of the Customer: top objections and call themes |
| Slack | Reading replies, posting the Monday teaser in the sales channel |
| Google Drive or SharePoint | Asset links for What's Launching and Content Spotlight |
| Google Calendar or Outlook Calendar | Webinar and event dates for What's Launching |
| Intent data (6sense or Demandbase, if your company has it) | Intent surges for Accounts to Work |

## Autonomous weekly send
1. In the Project, set `send_mode` in `air-cover-context.md`.
2. Schedule the weekly run: a scheduled task in Claude, or a Zapier schedule
   that starts the run every Monday morning.
3. Start in `draft` mode. Claude builds Air Cover and saves it as a draft;
   you review and press send. Move to `approve-to-send` or `auto` once the
   numbers are flowing from connected sources and you trust them.
