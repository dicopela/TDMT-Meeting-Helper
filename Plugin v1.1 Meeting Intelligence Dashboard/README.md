# Meeting Intelligence Dashboard

A local Codex/ChatGPT plugin that turns Outlook Webex meeting-summary emails into a standalone HTML dashboard.

## What it creates

- Weekly executive briefs
- Inferred cross-meeting work themes
- A searchable action register with source links
- A searchable meeting index with links to Outlook or Confluence details

## Requirements

The host must have Outlook email tools connected and available. The plugin packages the repeatable workflow and dashboard template; it does not include a separate Outlook API server.

## Use

After installing the plugin from the local marketplace, invoke `$meeting-intelligence-dashboard` or ask: “Create an HTML dashboard from my Outlook Webex meeting summaries for September 1 through today.”

The skill saves the standalone dashboard to the active workspace’s `outputs/` folder unless you specify another location.
