# Troubleshooting Guide

This guide helps you resolve common issues with the UpSnap Monitoring plugin for WordPress.

---

## Common Issues

### Authentication & Connection

#### "Login Failed" or "Invalid Credentials"

- **Cause:** Incorrect email/password or your server is unable to communicate with `api.upsnap.ai`.
- **Solution:**
  1. Verify your credentials at https://upsnap.ai
  2. Check if your server's firewall is blocking outbound HTTPS requests.
  3. Ensure your server has the `curl` PHP extension installed and enabled.

---

#### "No Primary Monitor Configured"

- **Cause:** You have authenticated but haven't selected which monitor data to show on the dashboard.
- **Solution:** Go to **Upsnap → Settings → Monitors** and click the **Set as Primary** button next to your site.

---

#### "API Unreachable" or Connection Timeouts

- **Cause:** Network issues between your host and the monitoring network.
- **Solution:**
  1. Wait a few minutes and try again (temporary network issue).
  2. Check service status: https://status.upsnap.ai

---

### Data & Display Issues

#### "No data in response" or Empty Dashboard

- **Cause:** The UpSnap API returned an empty result, often because the monitor is new or paused.
- **Solution:**
  1. Click the **Check Now** button to force a fresh scan.
  2. Wait 5–10 minutes for initial data after creating a new monitor.
  3. Ensure the monitored URL is correct and publicly accessible.

---

#### "Mixed Content" or "Broken Links" Not Updating

- **Cause:** WordPress or CDN caching is serving stale data.
- **Solution:**
  1. Clear your site cache (WP Rocket, W3 Total Cache, etc.).
  2. Purge your CDN cache (Cloudflare, Akamai, etc.).
  3. Run a fresh check in the plugin.

---

#### Charts Not Loading

- **Cause:** JavaScript conflict or blocked resource.
- **Solution:**
  1. Open browser console (F12) and check for errors.
  2. Temporarily disable "Minify JS" in optimization plugins.

---

## Debugging

### Enable WordPress Debugging

If you encounter a white screen or a "Critical Error," enable debugging:

1. Open `wp-config.php`
2. Update/add:

```php
define( 'WP_DEBUG', true );
define( 'WP_DEBUG_LOG', true );
define( 'WP_DEBUG_DISPLAY', false );
```

3. Check logs at: `wp-content/debug.log`  
   Look for entries prefixed with `Upsnap_`.

---

### Browser Console (Frontend)

Most dashboard data loads via REST API.

1. Open Developer Tools (F12)
2. Go to **Network** tab
3. Refresh page
4. Look for failed requests to:
   ```
   /wp-json/upsnap-monitoring/v1/...
   ```
5. Inspect **Response** tab for error details

---

### Testing API Connectivity

Run this command via SSH:

```bash
curl -I https://api.upsnap.ai/v1/status
```

Expected response:
```
HTTP/2 200
```

---

## Error Messages Explained

- **Authentication Error (401):** Session expired → log out and log back in.
- **Permission Denied (403):** Missing required capability (`manage_options`).
- **Not Found (404):** Monitor no longer exists in your account.
- **Rate Limit Exceeded (429):** Too many manual checks → wait or upgrade plan.

---

## Still Need Help?

If the issue persists, contact support with debug logs and environment details.

- **Email:** support@appfoster.com  
- **Forum:** WordPress.org Support