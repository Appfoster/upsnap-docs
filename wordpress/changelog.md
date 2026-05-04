# Changelog

All notable changes to the **UpSnap Website Monitoring & Uptime Dashboard** plugin for WordPress will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.1] - 2026-05-04

- Updated documentation links and readme formatting.
- Standardized versioning across plugin files.

## [1.0.0] - 2026-05-01

### Added
- **Initial release** of the UpSnap monitoring integration for WordPress.
- **Reachability Monitoring:** Real-time uptime tracking and global response time analysis.
- **Security Certificates:** SSL/TLS certificate validation, expiry countdowns, and chain monitoring.
- **Broken Links Detection:** Identification of broken internal/external links with source page tracking.
- **Lighthouse Performance:** Google Lighthouse scoring for Performance, Accessibility, SEO, and Best Practices.
- **Domain Health Check:** DNS record validation, domain registration tracking, and EPP status monitoring.
- **Mixed Content Detection:** Identification of insecure HTTP resources on secure HTTPS pages.
- **Incidents Dashboard:** Centralized view of all monitoring incidents and historical outages.
- **Status Pages:** Management of public-facing status pages directly from the WordPress admin.
- **Admin Dashboard Widget:** A quick-glance health summary on the main WordPress Dashboard.

### Technical Features
- **WordPress Compatibility:** Full support for WordPress 5.8 through 6.x.
- **PHP Support:** Compatible with PHP 7.4 and higher.
- **Service Architecture:** Clean separation between WordPress admin logic and core API services.
- **Secure Authentication:** Encrypted storage for UpSnap API tokens.
- **Native UI:** Built using standard WordPress admin patterns and Dashicons for a seamless experience.

## Version Policy
This plugin follows Semantic Versioning:
*   **MAJOR** version for incompatible changes or significant rebrandings.
*   **MINOR** version for backwards-compatible functionality additions.
*   **PATCH** version for backwards-compatible bug fixes and security updates.

## Support Policy
*   **Current Version:** Full support, feature updates, and security patches.
*   **Previous Versions:** Critical security updates only (for up to 6 months).
