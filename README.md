# n8n Workflow Templates

Production-tested n8n workflows from real client work. Each template includes the workflow JSON and instructions to adapt it for your stack.

## Templates

| Template | Nodes | Tools | Description |
|----------|-------|-------|-------------|
| [Auto-Create CRM Deals from Partner Intros](microsoft-outlook-integration-2-create-hubspot-deal-from-dra/) | 43 | n8n, HubSpot, Outlook, Slack, AI | Email lands, AI classifies + extracts, creates CRM deal, drafts reply, Slack approval |
| [AI Post-Call Notes + CRM Updates](teams-recordings-sharepoint/) | 57 | n8n, HubSpot, Teams, Slack, AI | Call ends, transcript processed, CRM updates automatically, summary to Slack |
| [Auto Emailer with Slack Approval](auto-emailer/) | 22 | n8n, HubSpot, Outlook, Slack | AI drafts follow-up emails, posts to Slack for one-click approval |
| [Proposal Signed: Invoice Generation](proposal-signed-send-invoices/) | 41 | n8n, HubSpot, Microsoft 365, Slack | Proposal gets signed, workflow creates and sends invoices automatically |
| [Proposal Signed: CRM + Slack Update](proposal-signed-update-hubspot-slack-notification/) | 9 | n8n, HubSpot, Slack | Proposal signature triggers CRM update and Slack notification |
| [Proposal Sequence Increment](proposal-sequence-increment/) | 11 | n8n, HubSpot | Auto-increments proposal numbers |
| [Sub-Workflow: Line Item Upsell](subwf-check-add-line-items-cap-to-ap-upsell/) | 10 | n8n, HubSpot | Checks deals and adds line items for upsell paths |
| [HubSpot Line Item Description Updater](hubspot-line-item-description-updater/) | 16 | n8n, HubSpot, Slack | Bulk updates line item descriptions |
| [Calendar Integration: Auto-Add Invitees](microsoft-calendar-integration-2-add-invitees/) | 25 | n8n, Microsoft 365 | Auto-adds invitees to calendar events |
| [Telegram Claude Bot](telegram-claude-bot-text-image-voice/) | 53 | n8n, Telegram, AI | Full Telegram bot: text, image, and voice messages with Claude |
| [Daily News Digest](daily-news-digest/) | 15 | n8n, Telegram | Automated daily news digest sent via Telegram |
| [Fireflies Transcript to Git](fireflies-transcript-to-git/) | 8 | n8n, Git | Auto-saves Fireflies call transcripts to a git repo |
| [Kanban Board Automation](kanban-move/) | 6 | n8n, Git | Moves tasks between kanban columns via automation |
| [n8n Auto-Update Notification](n8n-auto-update-notification/) | 7 | n8n, Microsoft 365 | Notifies when n8n updates are available |

## How to use

### Option 1: Import the JSON
1. Open n8n and create a new workflow
2. Click the three dots menu > **Import from file**
3. Select the `workflow.json` from the template folder
4. Update credentials and placeholder values (see each template's README)

### Option 2: Rebuild with Claude Code
Each template will include a `prompt.md` file you can use with Claude Code to recreate the workflow for your specific stack. For example: swap Outlook for Gmail, HubSpot for Pipedrive, same logic.

## Video walkthroughs

Each template has a companion YouTube video: [youtube.com/@vanessababicz](https://youtube.com/@vanessababicz)

## Placeholder values

After importing any template, search and replace these placeholders:

| Placeholder | Replace with |
|------------|--------------|
| `person1@company.com` | Your primary email |
| `person2@company.com` | Second team member's email |
| `team@company.com` | Your shared/team inbox |
| `partner1.com` - `partner7.com` | Your partner domains |
| `[slack-channel-id]` | Your Slack channel ID |
| `[hubspot-portal-id]` | Your HubSpot portal ID |
| `[your-n8n-domain]` | Your n8n instance URL |
| `[your-booking-link]` | Your booking page URL |

## License

MIT. Use these however you want.
