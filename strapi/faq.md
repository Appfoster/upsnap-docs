# Frequently Asked Questions

Common questions and answers about the UpSnap monitoring plugin for Strapi.

## General Questions

### What is UpSnap?
UpSnap is a comprehensive monitoring solution for Strapi that provides real-time insights into your website's health, performance, and security. It monitors uptime, SSL certificates, broken links, Lighthouse scores, and more, all from within your Strapi admin panel.

### What monitoring features are included?
*   **Reachability:** Global uptime and response time tracking.
*   **SSL/TLS Security:** Certificate validation and expiry alerts.
*   **Broken Links:** Automated scanning for dead internal and external links.
*   **Lighthouse:** Performance, Accessibility, Best Practices, and SEO audits.
*   **Domain Health:** DNS record monitoring and registration tracking.
*   **Mixed Content:** Detection of insecure HTTP assets on HTTPS pages.

### Is it compatible with the latest version of Strapi?
Yes, UpSnap is built specifically for **Strapi v5.x**.

## Installation & Setup

### How do I install the plugin?
1.  **Install via NPM/Yarn:**
    ```bash
    npm install @upsnap/strapi
    # or
    yarn add @upsnap/strapi
    ```
2.  **Enable Plugin:** Add the configuration to your `config/plugins.js` or `config/plugins.ts` file.
3.  **Build & Restart:** Rebuild your admin panel and restart your Strapi server.

### What are the system requirements?
*   **Strapi:** v5.x or later.
*   **Node.js:** >= 18.0.0 (Supports up to 22.x).
*   **Database:** Any database supported by Strapi (PostgreSQL, MySQL, SQLite).

### Do I need to manually configure an API key?
No. Simply navigate to **Upsnap → Settings** in your Strapi admin panel and log in with your UpSnap account. The plugin will securely handle the authentication and session management for you.

## Usage & Performance

### How often does it check my site?
The monitoring frequency depends on your settings. Reachability can be checked as often as every 1 minute, while more intensive audits like Lighthouse or Broken Links are typically scheduled on a daily or hourly basis.

### Does it affect my Strapi server's performance?
No. The actual monitoring audits are performed by UpSnap's global infrastructure, not your Strapi server. This ensures your server resources remain dedicated to your API and content management.

### Can I get notifications in Slack or Discord?
Yes. You can configure multiple notification channels including Email, Slack, Discord, Telegram, and Webhooks in the **Upsnap → Settings → Notification Channels** tab.

### Where can I see historical uptime data?
Detailed historical trends, response time graphs, and uptime percentages are available on the **Upsnap → Reachability** page.

## Troubleshooting

### Why is my dashboard showing "No data"?
*   **Authentication:** Ensure you are logged in via the Settings page.
*   **Primary Monitor:** You must select a "Primary Monitor" in Settings to tell the plugin which site's data to display on the main dashboard.
*   **Firewall:** If your server is in a private environment, UpSnap's monitoring bots must be able to reach your public URL.

### I can't see the Upsnap menu in the sidebar.
Ensure the plugin is enabled in your `config/plugins` file and that you have rebuilt your admin panel (`npm run build`). Also, check your user's **Roles & Permissions** in Strapi to ensure you have access to the plugin.

### How do I reset the plugin?
You can log out from the Settings page to clear your session. To remove the plugin entirely, uninstall the package and remove the entry from your `config/plugins` file.

## Security & Billing

### Is my monitoring data secure?
Yes. All communication between Strapi and the UpSnap API is encrypted via HTTPS. Sessions are managed securely using Strapi's best practices.

### Is there a free version?
Yes! UpSnap offers a **Free Plan** suitable for personal projects and small sites. For professional features and higher frequency monitoring, several premium plans are available at [upsnap.ai](https://upsnap.ai).

### Can I monitor multiple Strapi instances?
Yes. You can use the same UpSnap account across multiple Strapi installations. Each instance can be configured to track its own monitor or multiple monitors.

## Support

### Where can I get help?
*   **Documentation:** Browse the guides in this documentation portal for detailed walkthroughs.
*   **GitHub Issues:** Report bugs or request features on our [official repository](https://github.com/Appfoster/upsnap-strapi/issues).
*   **Email Support:** Premium users can access priority support via the [UpSnap website](https://upsnap.ai).
