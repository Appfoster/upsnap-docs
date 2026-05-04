# Broken Links Detection

Monitor and identify broken links across your WordPress website to maintain site integrity and ensure a smooth user experience.

## Overview
The UpSnap Broken Links dashboard provides a real-time report of any links on your site that are failing, blocked, or timing out. By resolving these issues, you can improve your site's SEO and prevent users from encountering frustrating 404 errors.

## Features

### Real-Time Link Monitoring
*   **Internal & External Scanning:** Automatically detects issues with links pointing to your own pages as well as outbound links to third-party websites.
*   **Detailed Issue Classification:** Identifies why a link is failing, whether it's a "404 Not Found" error, a server timeout, or a blocked request.
*   **Contextual Information:** For every broken link found, the plugin tells you exactly which page the link was found on, making it easy to locate and fix.

### Comprehensive Dashboard
*   **Pages Checked:** See the total number of pages scanned during the last audit.
*   **Link Type Filtering:** Quickly toggle between Internal and External links.
*   **Status Filtering:** Drill down into specific issues like "Broken", "Blocked", or "Timeout".

## Usage

### Viewing the Report
1.  Navigate to **Upsnap → Broken Links** in your WordPress admin sidebar.
2.  The dashboard will display a summary card showing:
    *   **Pages Checked:** Total unique pages audited.
    *   **Total Links:** Every link found on your site.
    *   **Broken Links:** Links that returned a non-200 status code.
    *   **Blocked Count:** Links that were blocked by the destination server or firewall.

### Understanding the Results
The **Broken Links Table** provides the following details for each issue:

| Column | Description |
| :--- | :--- |
| **URL** | The specific link that is failing. |
| **Found On Page** | The page on your WordPress site where this link exists. |
| **Status** | The current state (Broken, Blocked, or Timeout). |
| **Classification** | The specific HTTP error or category (e.g., 404, 503). |
| **Link Type** | Whether the link is Internal (within your domain) or External. |
| **Issue** | A human-readable description of the problem. |

### Running a Manual Scan
If you've recently fixed links and want to see updated results, click the **Check Now** button in the top right corner of the Broken Links page. This will trigger a fresh audit via the UpSnap API.

## Troubleshooting
*   **"No primary monitor configured":** This means you haven't yet connected your site to an UpSnap monitor. Go to **Upsnap → Settings** to set up your account.
*   **Timeouts:** If you see many timeout errors, the destination server may be slow or blocking automated checks.
*   **Blocked:** Some servers block the UpSnap crawler. If these are internal links, ensure your firewall allows requests from UpSnap's monitoring regions.
