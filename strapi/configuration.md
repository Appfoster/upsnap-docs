# Configuration Guide

Configure the UpSnap monitoring plugin to track your Strapi site's health and receive real-time alerts.

## Authentication
The plugin integrates directly with the UpSnap API. You do not need to manually manage API tokens in your configuration files.

1.  Navigate to **Upsnap → Settings** in your Strapi Admin Panel.
2.  **Login:** If you already have an UpSnap account, enter your credentials.
3.  **Register:** If you are new to UpSnap, you can create a free account directly within the plugin.
4.  Once authenticated, your API session is securely managed, and you will gain access to your monitors and notification settings.

## Monitor Configuration
Monitors are the core of UpSnap. They define what URL or host is being checked and how often.

### Managing Monitors
Access the **Monitors** tab under **Upsnap → Settings**:
*   **Primary Monitor:** You must select one monitor as your "Primary". This monitor provides the data for your main Strapi dashboard overview.
*   **Create Monitor:** Click "Create Monitor" to add a new site or service to track.
*   **Edit Monitor:** Adjust the name, URL, or check interval for any existing monitor.

### Monitor Settings
When creating or editing a monitor, you can configure:
*   **Monitor Name:** A friendly name to identify the site (e.g., "Main API Server").
*   **Monitor URL:** The full HTTPS URL of your Strapi application or website.
*   **Check Interval:** How often UpSnap should audit your site (e.g., Every 1 minute, Every 5 minutes, Every hour).

## Notification Integrations
Stay informed about downtime or performance issues by connecting UpSnap to your favorite communication tools.

### Setting Up Notifications
Access the **Notification Channels** tab under **Upsnap → Settings**:
1.  **Add Integration:** Choose from supported channels like **Email, Slack, Discord, SMS, Telegram, PagerDuty, Webhooks**, and more.
2.  **Configuration:** Provide the required details (e.g., Webhook URL for Slack/Discord, Phone Number for SMS).
3.  **Test:** Use the "Test" button to ensure your integration is working correctly before saving.
4.  **Toggle:** You can easily enable or disable specific integrations without deleting them.

## Permissions & Access Control
In Strapi, access to the UpSnap plugin is managed through **Role Based Access Control (RBAC)**:

1.  Go to **Settings → Administration Panel → Roles**.
2.  Select a role and scroll down to the **Plugins** section.
3.  Find **Upsnap** and configure permissions for viewing the dashboard, managing settings, or performing specific monitoring actions.

## Troubleshooting Configuration
*   **"No primary monitor configured":** You must go to the Monitors tab in Settings and ensure one monitor is selected as the primary source for the dashboard.
*   **Login Issues:** Ensure your credentials are correct. If you've forgotten your password, please visit the [UpSnap website](https://upsnap.ai) to reset it.
*   **Integrations Not Sending:** Ensure the integration is enabled and that your test message was successful during setup.
