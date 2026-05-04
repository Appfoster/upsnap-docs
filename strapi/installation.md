# Installation Guide

Follow these steps to install and set up the UpSnap Monitoring plugin for Strapi.

---

## Requirements

Before installing UpSnap, ensure your environment meets the following requirements:

- **Strapi:** v5.x or later
- **Node.js:** >= 18.0.0 (supports up to 22.x)
- **Package Manager:** npm or yarn
- **SSL:** Not required for local development, but a valid SSL certificate is recommended for production monitoring

---

## Installation Steps

### 1. Install the Package

Run the following command in your Strapi project root:

#### Using npm
```bash
npm install @upsnap/strapi
```

#### Using yarn
```bash
yarn add @upsnap/strapi
```

---

### 2. Enable the Plugin

Enable the plugin in your Strapi configuration.

**File:** `config/plugins.js` (or `config/plugins.ts`)

```javascript
module.exports = {
  // ...
  upsnap: {
    enabled: true,
  },
};
```

---

### 3. Build and Restart

Rebuild your Strapi admin panel and restart the server:

```bash
# Rebuild the admin panel
npm run build

# Start Strapi in development mode
npm run develop
```

---

## Post-Installation Setup

After Strapi restarts, connect your instance to UpSnap:

### 1. Authentication

- Go to **Upsnap → Settings**
- **Existing Users:** Log in with your account
- **New Users:** Register directly from the plugin

---

### 2. Monitor Selection

- Go to the **Monitors** tab
- If monitors exist:
  - Click **Set as Primary** for your site
- If no monitors exist:
  - Click **Create Monitor** and enter your site URL

---

### 3. Verification

- Navigate to **Upsnap → Dashboard**
- You should see:
  - “Connecting...” → followed by real-time data (uptime, response time, security)

---

## Troubleshooting Installation

### Plugin Not Appearing in Sidebar

- Ensure plugin is enabled in `config/plugins.js`
- Run `npm run build` after installation
- Check server logs for initialization errors

---

### Login Connection Issues

- Ensure your server can access:
  ```
  https://api.upsnap.ai
  ```
- If behind a proxy, configure Node.js for outbound requests

---

### Build Failures

- Ensure Node.js version >= 18
- Ensure sufficient memory during build
- Clear node modules if needed:

```bash
rm -rf node_modules package-lock.json
npm install
```

---

## Next Steps
*   [Configure Notification Integrations](configuration.md)
*   [Learn about Reachability Monitoring](features/reachability.md)
*   [Explore Security Certificates](features/security.md)