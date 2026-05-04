# Frequently Asked Questions

Common questions and answers about the UpSnap monitoring plugin for WordPress.

## General Questions

### What is UpSnap?
UpSnap is a comprehensive monitoring solution for WordPress that provides real-time insights into your website's health, performance, and security. It monitors uptime, SSL certificates, broken links, Lighthouse scores, and more, all from within your WordPress dashboard.

### What monitoring features are included?
*   **Reachability:** Global uptime and response time tracking.
*   **Security Certificates:** SSL/TLS certificate validation and expiry alerts.
*   **Broken Links:** Automated scanning for dead internal and external links.
*   **Lighthouse:** Performance, Accessibility, Best Practices, and SEO audits.
*   **Domain Health:** DNS record monitoring and registration tracking.
*   **Mixed Content:** Detection of insecure HTTP assets on HTTPS pages.

### Is it compatible with the latest version of WordPress?
Yes, UpSnap is fully compatible with WordPress 5.8 through the latest stable releases (6.x).

## Installation & Setup

### How do I install the plugin?
1.  **WordPress Repository:** Search for "Upsnap" in **Plugins → Add New**.
2.  **Manual Upload:** Download the plugin ZIP and upload it via **Plugins → Add New → Upload Plugin**.
3.  **Activation:** Once installed, click "Activate" to begin the setup process.

### What are the system requirements?
*   **WordPress:** 5.8 or later.
*   **PHP:** 7.4 or later (8.0+ recommended).
*   **HTTPS:** Your site must be accessible via HTTPS for many monitoring features to work optimally.

### Do I need to manually configure an API key?
No. Simply navigate to **Upsnap → Settings** and log in with your UpSnap account. The plugin will securely handle the API authentication for you automatically.

## Usage & Performance

### How often does it check my site?
The monitoring frequency depends on your configuration. By default, reachability is checked every 5 minutes, while more intensive scans like Lighthouse or Broken Links run on a scheduled daily or hourly basis.

### Does it affect my site's performance?
No. The audits are performed by UpSnap's global monitoring servers, not your WordPress server. This ensures your site's resources remain focused on serving your visitors.

### Can I get email notifications?
Yes. You can configure email alerts, as well as Slack, Discord, and Webhook integrations, in the **Settings → Notification Integrations** tab.

### How do I view historical data?
Detailed historical charts for response times and uptime are available on the **Upsnap → Reachability** page.

## Troubleshooting

### Why are my checks failing?
Common causes include:
*   **Firewall Blocking:** Your server or a security plugin (like Wordfence) might be blocking the UpSnap monitoring bots.
*   **Maintenance Mode:** If your site is in maintenance mode or behind a "Coming Soon" page, external monitors cannot reach it.
*   **Incorrect URL:** Ensure your "Primary Monitor" URL in settings matches your actual site address.

### "No primary monitor configured" — what does this mean?
You have successfully logged in, but you haven't told the plugin which monitor should be shown on the dashboard. Go to **Upsnap → Settings → Monitors** and click the **Set as Primary** button next to your site.

### How do I clear the plugin data?
The plugin respects standard WordPress data management. To reset your settings, you can "Log Out" from the Settings page. To remove all data entirely, simply deactivate and delete the plugin.

## Security & Billing

### Is my monitoring data secure?
Yes. All communication between your WordPress site and the UpSnap API is encrypted via HTTPS. Your API tokens are stored securely using WordPress best practices.

### How much does it cost?
UpSnap offers a generous **Free Plan** for personal sites and small blogs. For high-frequency monitoring and advanced features, various premium plans are available at [upsnap.ai](https://upsnap.ai).

### Can I monitor multiple sites?
Yes! You can manage multiple monitors from a single UpSnap account. In your WordPress site, you can choose which of those monitors to display in the local dashboard.

## Support

### Where can I get help?
*   **Documentation:** Browse the guides in this wiki for detailed walkthroughs.
*   **WP.org Forums:** For general questions and community support.
*   **Email Support:** Premium users can contact our dedicated support team via the UpSnap dashboard.
