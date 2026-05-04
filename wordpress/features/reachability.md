# Reachability Monitoring

Monitor your website's availability, response times, and global performance directly from your WordPress admin dashboard.

## Overview
The Reachability monitoring feature provides real-time insights into your site's uptime. It continuously tests your website from multiple global locations to ensure your users can reach your content without delays or errors.

## Features

### Real-Time Global Monitoring
*   **Status Indicators:** Instantly see if your site is Online (Green), experiencing issues (Yellow), or Offline (Red).
*   **Multi-Region Performance:** View specific response times from different geographic monitoring points (e.g., US East, Europe West, Asia Pacific).
*   **HTTP Details:** Access technical details such as HTTP status codes (200, 404, 500) and server response headers.

### Security & TLS
*   **TLS Validation:** Monitor the security of your connection, including SSL version and cipher suites.
*   **Certificate Health:** Get immediate visibility into your security certificate's status.

### Performance Analytics & History
*   **Interactive Charts:** Visualize your site's response time over various periods:
    *   Last Hour
    *   Last 24 Hours
    *   Last 7 Days
    *   Last 30 Days
    *   Last Year
*   **Performance Stats:** Track your Average, Maximum, and Minimum response times to identify performance bottlenecks.

## Usage

### Viewing Your Site's Reachability
1.  In your WordPress Admin, go to **Upsnap → Reachability**.
2.  The **Status Banner** at the top provides an immediate health check.
3.  The **HTTP Details** and **TLS / Security** cards provide technical diagnostics for developers.
4.  **Region Cards:** Check the right-hand column to see how your site performs in different parts of the world.

### Analyzing Trends
Use the **Response Time** chart to identify patterns in your site's performance. For example, if you notice spikes at the same time every day, it may indicate a scheduled server task or backup that is slowing down your site.

### Manual Connection Check
To perform an on-demand reachability test, click the **Check Now** button in the top right. This will trigger a fresh check across all monitoring regions via the UpSnap API.

## Troubleshooting
*   **"Partial Reachability":** Your site may be reachable from some regions but blocked or slow in others. This often points to CDN configuration issues or regional network problems.
*   **"Unreachable":** This means the UpSnap monitoring network cannot connect to your site. Check your server status and firewall settings.
*   **"No data in response":** Ensure your primary monitor is correctly configured in **Upsnap → Settings**.
