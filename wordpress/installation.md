# Installation Guide

Follow these steps to install and set up the UpSnap Monitoring plugin on your WordPress site.

## Requirements

Before installing UpSnap, ensure your environment meets the following requirements:

- **WordPress**: 5.8 or later.
- **PHP**: 7.4 or later (8.1+ recommended).
- **SSL**: A valid SSL certificate is required for your site to use HTTPS, which is necessary for accurate monitoring.

## Installation Methods

### Method 1: WordPress Plugin Repository (Recommended)

1.  Log in to your WordPress Admin dashboard.
2.  Navigate to **Plugins → Add New**.
3.  In the search bar, type **"Upsnap"**.
4.  Locate the **UpSnap Website Monitoring & Uptime Dashboard** plugin.
5.  Click **Install Now** and then click **Activate**.

### Method 2: Manual Installation (ZIP Upload)

1.  Download the plugin ZIP file from the [WordPress.org Plugin Page](https://wordpress.org/plugins/upsnap-monitoring/) or GitHub releases.
2.  In your WordPress Admin, go to **Plugins → Add New**.
3.  Click the **Upload Plugin** button at the top of the page.
4.  Choose the `upsnap-monitoring.zip` file and click **Install Now**.
5.  Once the installation is complete, click **Activate Plugin**.

## Post-Installation Setup

After activating the plugin, follow these steps to connect your site to the UpSnap monitoring network:

### 1. Authentication
Navigate to the new **Upsnap** menu in your sidebar and select **Settings**.
*   **Existing Users:** Enter your email and password to log in.
*   **New Users:** Click the "Register" link to create a free account directly within the plugin.

### 2. Monitor Selection
Once logged in, go to the **Monitors** tab:
*   If you already have monitors in your UpSnap account, click **Set as Primary** next to the monitor for this site.
*   If you have no monitors, click **Create Monitor** and enter your site's URL.

### 3. Verification
Navigate to **Upsnap → Dashboard**. You should see a "Connecting to UpSnap..." message followed by your site's real-time health data.

## Troubleshooting Installation

### Plugin Not Appearing in Sidebar
*   Ensure the plugin is activated under **Plugins → Installed Plugins**.
*   Try clearing your WordPress object cache (if using a plugin like Redis Object Cache or W3 Total Cache).

### Login Connection Issues
*   Ensure your server can make outbound HTTPS requests to `https://api.upsnap.ai`.
*   Check for security plugins (like Wordfence or iThemes Security) that might be blocking the API connection.

### PHP Version Errors
If you see a "Parse Error" or "Syntax Error" during installation, your server may be running an outdated version of PHP (below 7.4). Please contact your hosting provider to upgrade to a modern version of PHP.

## Next Steps
*   [Configure Notification Integrations](configuration.md)
*   [Learn about Reachability Monitoring](features/reachability.md)
*   [Explore Security Certificates](features/security.md)
