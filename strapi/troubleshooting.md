# Troubleshooting Guide

This guide helps you resolve common issues with the UpSnap Monitoring plugin for Strapi.

---

## Common Issues

### Authentication & Connection

#### "Login Failed" or "Invalid Credentials"

- **Cause:** Incorrect email/password or your server cannot communicate with `api.upsnap.ai`.
- **Solution:**
  1. Verify your credentials at https://upsnap.ai
  2. Check firewall/security groups for outbound HTTPS blocks
  3. Ensure your Node.js environment has internet access

---

#### "No Primary Monitor Configured"

- **Cause:** Logged in successfully but no monitor selected.
- **Solution:** Go to **Upsnap → Settings → Monitors** and enable **Set as Primary**.

---

#### "API Unreachable" or Connection Timeouts

- **Cause:** Network issues between your server and UpSnap.
- **Solution:**
  1. Retry after a few minutes
  2. Check service status: https://status.upsnap.ai

---

### Data & Display Issues

#### Dashboard Shows "No Data" or is Empty

- **Cause:** Monitor is new, paused, or API returned empty data.
- **Solution:**
  1. Click **Refresh**
  2. Wait 5–10 minutes after creating monitor
  3. Verify URL is publicly accessible

---

#### "Mixed Content" or "Broken Links" Not Updating

- **Cause:** Cached responses (CDN or Strapi middleware)
- **Solution:**
  1. Clear CDN cache (Cloudflare, etc.)
  2. Clear/disable Strapi cache middleware
  3. Trigger a fresh scan

---

#### UI Components or Charts Not Loading

- **Cause:** JS conflicts or blocked resources
- **Solution:**
  1. Open browser console (F12)
  2. Disable ad blockers/extensions
  3. Ensure admin build is up to date:

```bash
npm run build
```

---

## Debugging

### Server-Side Logs

1. Run Strapi:
```bash
npm run develop
```

2. Check logs for:
   - `[upsnap]` prefixed errors
   - 4xx / 5xx responses
   - Failed requests to `https://api.upsnap.ai`

---

### Browser Console (Frontend)

1. Open Developer Tools (F12)
2. Go to **Network**
3. Perform failing action
4. Look for failed requests:

```
/upsnap/monitors
/upsnap/settings
```

5. Inspect **Response** tab

---

### Testing API Connectivity

```bash
curl -I https://api.upsnap.ai/v1/status
```

Expected:

```
HTTP/2 200
```

---

## Error Messages Explained

- **Authentication Error (401):** Session expired → log in again
- **Permission Denied (403):** Check Strapi Roles & Permissions
- **Not Found (404):** Monitor/resource no longer exists
- **Rate Limit Exceeded (429):** Too many requests → wait or upgrade

---

## Still Need Help?

Provide logs and environment details when contacting support:

- **Email:** support@appfoster.com  
- **GitHub Issues:** https://github.com/Appfoster/upsnap-strapi