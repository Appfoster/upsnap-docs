# Usage Guide

Learn how to navigate and use the UpSnap Monitoring plugin to keep your Strapi site healthy and performant.

## Getting Started

### Accessing the Plugin
1.  Log into your **Strapi Admin Panel**.
2.  In the sidebar, locate the **Upsnap** menu item.
3.  Click **Upsnap** to open the main dashboard. You can navigate to specific features using the internal sidebar within the plugin.

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
*   **Settings:** Manage monitors, account info, and notification channels.

---

## Basic Usage

### Running On-Demand Checks
While UpSnap performs automated background checks, you can trigger a manual update at any time:
1.  Navigate to any feature page (e.g., **Reachability**).
2.  Click the **Refresh** or **Check Now** button in the header.
3.  The plugin will request a fresh audit from the UpSnap API and update the UI in real-time.

### Understanding Status Icons
*   🟢 **Online / Success:** Everything is working correctly and meeting industry standards.
*   🟡 **Warning / Issue:** The site is reachable, but we've detected slow response times or minor configuration issues.
*   🔴 **Offline / Critical Error:** Critical issue detected (e.g., site is down, certificate is expired, or high mixed content count).

---

## Feature Deep Dives

### Reachability
Monitor your site's availability from multiple global locations.
*   **Response Time Chart:** Filter by different time ranges to identify performance trends and latency spikes.
*   **Regional Data:** See how fast your site loads for users in different global regions.

### Incidents Dashboard
Keep a record of every time your site went down or experienced performance degradation.
*   **Outage Logs:** See exactly when a downtime started and ended.
*   **Root Cause:** Review the HTTP status codes and error details received during the incident.

### Status Pages
Keep your customers informed during maintenance or outages.
*   **Public Link:** Create a branded page that lists your site's current status and uptime history.
*   **Management:** Create, edit, or disable status pages directly from the Strapi admin panel.

### Broken Links
Maintain your SEO and user experience by fixing dead links.
*   **Link Detail:** View the broken URL and the specific page where it was found.
*   **Filters:** Quickly filter by link type to prioritize your fixes.

---

## Advanced Usage

### Primary Monitor Selection
If you monitor multiple sites with your UpSnap account, you can choose which one to display in this specific Strapi installation:
1.  Go to **Upsnap → Settings → Monitors**.
2.  Toggle the **Set as Primary** switch for the correct monitor.
3.  All dashboard metrics will now reflect that specific site.

### Testing Notification Channels
Ensure your alert system is working correctly:
1.  Go to **Upsnap → Settings → Notification Channels**.
2.  Find your configured integration (e.g., Slack) and click the **Test** button.
3.  Check your target application to confirm receipt of the test notification.

---

## Best Practices
*   **Monitoring Frequency:** Set reachability to 1 or 5 minutes for business-critical production environments.
*   **SEO & UX:** Fix "Mixed Content" and "Broken Links" promptly to avoid search engine penalties and improve user trust.
*   **SSL Security:** Pay close attention to "Security Certificate" warnings. Expired certificates are a leading cause of traffic loss and security warnings.
