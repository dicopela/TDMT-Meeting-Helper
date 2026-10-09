# Architecture

## Single-file layout

The dashboard is implemented in meeting-intelligence-dashboard.html:

- HTML defines the sidebar navigation, page panels, summary cards, tables, and embedded workspaces.
- CSS is inline in the document.
- JavaScript is inline and handles panel navigation, dynamic page titles, filters, tables, and refresh behavior.
- The PR workspace is embedded in the document as base64 data.
- The initial meeting/project snapshot is embedded in the document.

No external JavaScript or stylesheet assets were found in the HTML.

## Data flow

1. The embedded snapshot populates the dashboard when the page loads.
2. Navigation switches among the six panels; the large page heading is set from the active tab.
3. Refresh data requests Confluence page 2470707256 using the current browser session and no-store caching.
4. The refresh depends on browser CORS approval for the hosting origin and the signed-in user's Confluence access.

The Confluence source is the data refresh input. The local snapshot keeps the dashboard viewable when the refresh endpoint cannot be reached.
