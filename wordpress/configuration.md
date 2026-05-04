# Configuration Guide

Configure the UpSnap monitoring plugin to track your WordPress site's health and receive real-time alerts.

## Authentication
The plugin integrates directly with the UpSnap API. Unlike other CMS integrations, you do not need to manually manage API tokens in your configuration files.

1.  Navigate to **Upsnap → Settings** in your WordPress Admin.
2.  **Login:** If you already have an UpSnap account, enter your credentials.
3.  **Register:** If you are new to UpSnap, you can create a free account directly within the plugin.
4.  Once authenticated, your API token is securely stored in your WordPress database.

## Monitor Configuration
Monitors are the core of UpSnap. They define what URL or host is being checked and how often.

### Managing Monitors
Access the **Monitors** tab under **Upsnap → Settings**:
*   **Primary Monitor:** You must select one monitor as your "Primary". This monitor provides the data for your main WordPress dashboard widget and health check pages.
*   **Create Monitor:** Click "Create Monitor" to add a new site or service to track.
*   **Edit Monitor:** Adjust the name, URL, or check interval for any existing monitor.

### Monitor Settings
When creating or editing a monitor, you can configure:
*   **Monitor Name:** A friendly name to identify the site (e.g., "My Portfolio").
*   **Monitor URL:** The full HTTPS URL of your website.
*   **Check Interval:** How often UpSnap should audit your site (e.g., Every 5 minutes, Every hour).

## Notification Integrations
Stay informed about downtime or performance issues by connecting UpSnap to your favorite communication tools.

### Setting Up Notifications
Access the **Notification Integrations** tab under **Upsnap → Settings**:
1.  **Add Integration:** Choose from supported channels like **Email, Slack, Discord, SMS, Telegram, PagerDuty, Webhooks**, and more.
2.  **Configuration:** Provide the required details (e.g., Webhook URL for Slack, Phone Number for SMS).
3.  **Test:** Use the "Test" button to ensure your integration is working correctly before saving.
4.  **Toggle:** You can easily enable or disable specific integrations without deleting them.

## Advanced Configuration
For most users, the default settings are optimal. However, the following technical details are available for advanced setups:

### API Endpoints
The plugin communicates with `https://api.upsnap.ai/v1`. If you are behind a strict firewall, ensure your server can make outbound requests to this domain.

### Permissions
By default, only users with the `manage_options` capability (Administrators) can access the Upsnap menu and settings.

## Troubleshooting Configuration
*   **"No primary monitor configured":** You must go to the Monitors tab in Settings and click "Set as Primary" for one of your monitors.
*   **Integrations Not Sending:** Ensure the "Enabled" toggle is active for your integration and that your test message was successful.
