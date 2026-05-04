# Google Lighthouse Audits

Monitor your website's performance, accessibility, SEO, and adherence to modern best practices directly from your WordPress admin.

## Overview
The UpSnap Lighthouse integration runs automated audits against your website using Google's Lighthouse engine. This allows you to track key quality metrics and ensure your site provides a high-quality experience for both users and search engines.

## Features

### Multi-Strategy Auditing
*   **Desktop & Mobile:** Toggle between Desktop and Mobile strategies to see how your site performs across different devices and network conditions.
*   **Automated Updates:** Audits are performed automatically according to your UpSnap account configuration.

### Core Scoring Categories
The plugin provides visual scores (0-100) for five key categories:
*   **Performance:** Measures how quickly your content loads and how soon users can interact with it.
*   **Accessibility:** Checks for common accessibility issues to ensure your site is usable for everyone.
*   **Best Practices:** Audits for modern web development standards and security best practices.
*   **SEO:** Ensures your page is optimized for search engine results rankings.
*   **PWA (Progressive Web App):** Checks if your site meets the technical requirements for Progressive Web Apps.

### Key Performance Metrics
Get detailed insights into your site's loading performance with specific metrics:
*   **FCP (First Contentful Paint):** When the first text or image is painted.
*   **LCP (Largest Contentful Paint):** When the main content of the page has likely loaded.
*   **Speed Index:** How quickly the contents of a page are visibly populated.
*   **TBT (Total Blocking Time):** Sum of all time periods between FCP and Time to Interactive where task length exceeded 50ms.
*   **Time to Interactive:** When the page is fully interactive.
*   **CLS (Cumulative Layout Shift):** Measures visual stability by quantifying how much elements move around during loading.

## Usage

### Accessing Lighthouse Reports
1.  Navigate to **Upsnap → Lighthouse** in your WordPress Admin sidebar.
2.  Use the **Strategy** dropdown to switch between "Desktop" and "Mobile" views.

### Understanding Your Scores
The scores are color-coded based on industry standards:
*   🟢 **90-100 (Excellent):** Your site is well-optimized in this category.
*   🟠 **50-89 (Needs Improvement):** There are opportunities to improve this metric.
*   🔴 **0-49 (Poor):** This category needs immediate attention.

### Manual Audit Refresh
If you've made optimizations and want to see the immediate impact, click the **Check Now** button in the top right. This triggers a fresh Lighthouse audit via the UpSnap API.

## Troubleshooting
*   **"No data in response":** If you see this after a fresh audit, the Lighthouse service may be busy or your site may be blocking the audit crawler. Ensure your site is publicly accessible and not blocked by security plugins or firewalls.
*   **Low Performance Scores:** Common causes in WordPress include unoptimized images, too many plugins (large JS/CSS files), or a slow hosting environment.
