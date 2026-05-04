# Mixed Content Detection

Identify and resolve insecure HTTP resources being loaded on your HTTPS-enabled Strapi website to ensure full security and browser compliance.

## Overview
Mixed content occurs when a secure HTTPS page loads assets (like images, scripts, or stylesheets) over an insecure HTTP connection. This can compromise your users' security, trigger browser warnings, and even cause browsers to block essential functionality. The UpSnap Mixed Content dashboard provides a clear list of these insecure resources so you can quickly fix them.

## Features

### Insecure Asset Tracking
*   **Automatic Detection:** UpSnap identifies insecure resources during its regular site audits.
*   **Broad Resource Coverage:** Monitors various types of assets that commonly cause mixed content warnings, including:
    *   **Images:** Photos and graphics loaded via `http://`.
    *   **Scripts:** JavaScript files that could potentially be hijacked if not served over HTTPS.
    *   **Stylesheets:** CSS files that define your site's appearance.
    *   **Other Resources:** Fonts, iframes, and media files.

### Resource Attribution
*   **Affected URL:** View the exact URL of the insecure resource.
*   **Context:** See which specific page on your Strapi site is responsible for loading the insecure asset, allowing for rapid debugging and correction.

## Usage

### Viewing the Mixed Content Report
1.  In your Strapi Admin Panel, navigate to **Upsnap → Mixed Content**.
2.  The dashboard will display a summary card showing the total number of mixed content violations detected.

### The Insecure Resources Table
Review the table to identify the specific assets that need to be updated to HTTPS:

| Column | Description |
| :--- | :--- |
| **URL** | The full HTTP address of the insecure asset. |
| **Found On Page** | The page on your website where this asset was detected. |
| **Resource Type** | The category of the asset (e.g., Image, Script, CSS). |

### Running a Manual Scan
If you have updated your content or configuration to fix mixed content and want to verify the results immediately, click the **Check Now** or **Refresh** button in the header. This will trigger a fresh audit of your site's security state.

## Why Mixed Content Matters
*   **Security Risk:** Insecure scripts or stylesheets can be intercepted and modified by attackers ("Man-in-the-Middle" attacks) to inject malicious code into your site.
*   **Browser Warnings:** Most modern browsers (Chrome, Firefox, Safari) will show a "Not Secure" warning in the address bar if mixed content is detected, which can damage user trust.
*   **Blocked Content:** Browsers are increasingly blocking "Active" mixed content (like scripts and iframes) entirely to protect users, which can break your site's functionality.

## Troubleshooting
*   **"No mixed content detected":** This is the ideal state! It means your site is serving all its assets securely over HTTPS.
*   **Resources Not Updating:** If you've fixed a URL but it still shows as HTTP in the report, ensure you've cleared any site-side or CDN-side caching (like Cloudflare) before running a fresh check.
*   **Hardcoded URLs:** In many Strapi applications, mixed content is caused by hardcoded `http://` links in your frontend templates or within your CMS content (e.g., in a Markdown or Rich Text field).
