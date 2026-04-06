# GHL: WhatsApp Lead Nurture + Qualifier (Manual Review)

**Nodes:** 20
**Tools:** Code, HTTP/API, Google Sheets

## What it does

Same as the automated version, but instead of sending replies immediately, it saves AI-generated messages to a Google Sheet for your review. Change status to "Approved" and a second workflow sends the message automatically every 5 minutes.

Perfect if you want AI to draft, but a human to approve before anything goes out.

## How to use

### Option 1: Import JSON
1. Open n8n
2. Create a new workflow
3. Click the three dots menu > Import from file
4. Select `workflow.json`
5. Update credentials and configuration values

## Configuration

After importing, update:
- GoHighLevel API key (in all globe/HTTP nodes under Authorization header)
- Location ID (from your GHL account URL: `/v2/location/YOUR_ID`)
- Google Sheets ID (from your sheet URL)
- Sheet tab name (default: `tracker`)
- Column names in Sheets nodes (must match your sheet headers)
- OpenAI API key credential
- Customize the AI prompt in the Edit Fields node

## Google Sheet setup

Create a sheet with these column headers (exact match):
- `contact_id`
- `contact_name`
- `message`
- `status` (values: `review`, `approved`, `sent`, `needs template`)

## Notes
- Publish the second workflow (the scheduler) or it won't auto-send approved messages
- WhatsApp has a 24h window for free-form replies — approve messages promptly
- The scheduler checks every 5 minutes for approved rows
