# Good Dog! Meeting and Project Intelligence

A standalone meeting and project intelligence dashboard for delivery and project teams.

## Contents

- meeting-intelligence-dashboard.html — complete dashboard source, including its inline styles, application logic, embedded project workspace, and the current meeting snapshot.
- BUILD.md — local preview and hosted refresh instructions.
- ARCHITECTURE.md — page structure and data flow.

## Dashboard areas

- Executive overview
- Work themes
- Action register
- Meetings
- Detailed Meeting Prep
- PR workspace

The main page heading follows the selected tab.

## Requirements

The dashboard is a self-contained HTML file. It has no package manager, framework, separate JavaScript/CSS assets, or install step. A modern browser is enough to view the embedded snapshot.

The Refresh data control requests the latest content from Confluence page 2470707256. It uses the signed-in browser session; no API token is included in this package. Refresh requires access to that Confluence page and a browser-approved hosted origin. Browsers block the Confluence request when this file is opened directly through a file URL. See BUILD.md.

## Data handling

The HTML contains an embedded meeting snapshot and project information. Treat the file and any hosted copy as internal company material. Use an approved private hosting location and access controls.
