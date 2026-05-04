# Broken Links Detection

Monitor and identify broken links across your Strapi-powered website to maintain site integrity and ensure a smooth user experience.

## Overview
The UpSnap Broken Links dashboard provides a real-time report of any links on your site that are failing, blocked, or timing out. By resolving these issues, you can improve your site's SEO and prevent users from encountering frustrating 404 errors.

## Features

### Real-Time Link Monitoring
*   **Internal & External Scanning:** Automatically detects issues with links pointing to your own pages as well as outbound links to third-party websites.
*   **Detailed Issue Classification:** Identifies why a link is failing, whether it's a "404 Not Found" error, a server timeout, or a blocked request.
*   **Contextual Information:** For every broken link found, the plugin tells you exactly which page the link was found on, making it easy to locate and fix.

### Comprehensive Dashboard
*   **Pages Checked:** See the total number of unique pages scanned during the last audit.
*   **Link Type Filtering:** Quickly toggle between Internal and External links to prioritize your fixes.
*   **Status Filtering:** Drill down into specific issues like "Broken", "Blocked", or "Timeout".

## Usage

### Viewing the Report
1.  In your Strapi Admin Panel, navigate to **Upsnap → Broken Links**.
2.  The dashboard will display a summary card showing:
    *   **Pages Checked:** Total unique pages audited.
    *   **Total Links:** Every link found during the scan.
    *   **Broken Links:** Links that returned a non-200 status code.
    *   **Blocked Count:** Links that were blocked by the destination server or firewall.

### Understanding the Results
The **Broken Links Table** provides the following details for each issue:

| Column | Description |
| :--- | :--- |
| **URL** | The specific link that is failing. |
| **Found On Page** | The page on your website where this link exists. |
| **Status** | The current state (Broken, Blocked, or Timeout). |
| **Classification** | The specific HTTP error or category (e.g., 404, 503). |
| **Link Type** | Whether the link is Internal (within your domain) or External. |
| **Issue** | A human-readable description of the problem. |

### Running a Manual Scan
If you've recently updated your content and want to verify the fixes, click the **Check Now** or **Refresh** button in the header of the Broken Links page. This will trigger a fresh audit via the UpSnap API.

## Troubleshooting
*   **"No primary monitor configured":** This means you haven't yet selected a monitor for this Strapi instance. Go to **Upsnap → Settings** to configure your monitor.
*   **Timeouts:** If you see many timeout errors, the destination server may be slow or blocking automated scanning bots.
*   **Blocked:** Some servers block automated crawlers. If these are internal links, ensure your server's firewall allows requests from UpSnap's monitoring regions.
