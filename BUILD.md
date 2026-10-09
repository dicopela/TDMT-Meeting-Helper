# Build and run

## Build

There is no compilation or dependency installation step. The dashboard is a single HTML file with inline CSS and JavaScript. Keep meeting-intelligence-dashboard.html together with this documentation when distributing the source package.

## Preview locally

Extract the package and open meeting-intelligence-dashboard.html in a browser to view the embedded snapshot.

For an HTTP preview on Windows, open PowerShell in the extracted folder and run:

    py -m http.server 8000

Then open:

    http://localhost:8000/meeting-intelligence-dashboard.html

This local preview serves the page, but it does not guarantee that data refresh will work.

## Refresh and hosting

The refresh function makes an authenticated request to:

    https://iot-controlcenter.atlassian.net/wiki/api/v2/pages/2470707256?body-format=storage

The browser sends the current Atlassian session. The user must be signed in and have permission to view the source page. The dashboard must also be served from an origin approved by the browser and Confluence CORS policy. Opening the file with a file URL is blocked; localhost may also be blocked unless it is explicitly allowed. Use the organization's approved private hosting origin for refresh testing.

Do not add passwords, API tokens, or other credentials to the HTML. If refresh fails on a hosted copy, check the signed-in account, Confluence page permissions, and the hosting origin's CORS approval.
