# YourCompany: SubWF Check + Add Line Items (CAP to AP Upsell)

**Nodes:** 10  
**Tools:** Code, HTTP/API

## How to use

### Option 1: Import JSON
1. Open n8n
2. Create a new workflow
3. Click the three dots menu > Import from file
4. Select \`workflow.json\`
5. Update credentials and configuration values

### Option 2: Claude Code prompt
Use the prompt in \`prompt.md\` (coming soon) to rebuild this workflow with Claude Code for your specific stack.

## Configuration

After importing, update these placeholders:
- \`person1@company.com\` / \`person2@company.com\` -- your team emails
- \`team@company.com\` -- your shared inbox
- \`partner1.com\` through \`partner7.com\` -- your partner domains
- \`[slack-channel-id]\` -- your Slack channel ID
- \`[hubspot-portal-id]\` -- your HubSpot portal ID
- \`[your-n8n-domain]\` -- your n8n instance URL
- Reconnect all credentials (API keys, OAuth)
