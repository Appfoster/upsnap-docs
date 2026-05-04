# Usage Guide

Learn how to navigate and use the Upsnap Monitoring plugin to keep your WordPress site healthy and performant.

## Getting Started

### Accessing the Plugin
1.  Log into your WordPress Admin.
2.  In the sidebar, locate the **Upsnap Monitoring** menu.
3.  Click **Upsnap Monitoring** to open the main dashboard or select a specific feature from the submenus.

### Navigation Overview
*   **Dashboard:** Your site's health summary at a glance.
*   **Reachability:** Uptime and global response time performance.
*   **Security Certificates:** SSL/TLS certificate health and chain details.
*   **Broken Links:** Identification of dead internal and external links.
*   **Lighthouse:** Performance, SEO, and Accessibility scores.
*   **Domain Check:** DNS configuration and registration lifecycle.
*   **Mixed Content:** Tracking insecure HTTP resources.
*   **Incidents:** A history of downtime and performance events.
*   **Status Pages:** Manage public status pages for your users.
*   **Settings:** Manage monitors, account info, and alert integrations.

---

## Basic Usage

### Running On-Demand Checks
While UpSnap performs automated checks, you can trigger a manual update at any time:
1.  Navigate to any feature page (e.g., Reachability).
2.  Click the **Check Now** button in the top right.
3.  The plugin will request a fresh audit from the UpSnap API and update the UI in real-time.

### Understanding Status Icons
*   🟢 **Online / Success:** Everything is working correctly and meeting industry standards.
*   🟡 **Warning / Performance Issue:** The site is reachable, but we've detected slow response times or minor configuration issues.
*   🔴 **Offline / Error:** Critical issue detected (e.g., site is down, certificate is expired, or high mixed content count).

---

## Feature Deep Dives

### Reachability
Monitor your site's availability from 10+ global locations.
*   **Response Time Chart:** Filter by "Last 24 Hours", "Last 7 Days", etc., to identify performance trends.
*   **Regional Data:** See how fast your site loads for users in the US, Europe, and Asia.

### Incidents Dashboard
Keep a record of every time your site went down or slowed down.
*   **Outage Logs:** See exactly when a downtime started and ended.
*   **Root Cause:** Review the HTTP status code (e.g., 502 Bad Gateway) received during the incident.

### Status Pages
Keep your customers informed during maintenance or outages.
*   **Public Link:** Create a branded page that lists your site's current status and uptime history.
*   **Management:** Enable or disable status pages directly from the WordPress admin.

### Broken Links
Maintain your SEO and user experience by fixing dead links.
*   **Link Detail:** View the broken URL and the specific WordPress page where it was found.
*   **Filters:** Quickly filter by "Internal" or "External" links to prioritize fixes.

---

## Advanced Usage

### Dashboard Widget
UpSnap adds a health summary to your main WordPress **Dashboard** (the first page you see after logging in). You can drag and drop this widget to your preferred position for instant visibility.

### Primary Monitor Selection
If you monitor multiple sites with your UpSnap account, you can choose which one to display in this specific WordPress installation:
1.  Go to **Upsnap Monitoring → Settings → Monitors**.
2.  Click **Set as Primary** for the correct monitor.
3.  All dashboard metrics will now reflect that specific site.

### Testing Alerts
Ensure your notification system is working:
1.  Go to **Upsnap Monitoring → Settings → Notification Integrations**.
2.  Find your integration (e.g., Slack) and click the **Test** button.
3.  Check your target app to confirm receipt of the test notification.

---

## Best Practices
*   **Frequency:** Set reachability to 5 minutes for business-critical sites.
*   **SEO:** Fix "Mixed Content" and "Broken Links" promptly to avoid penalties in search rankings.
*   **Security:** Always investigate when you see a "Security Certificate" warning—expired SSLs are the #1 cause of lost traffic.
