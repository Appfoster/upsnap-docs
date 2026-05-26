# Changelog

All notable changes to the UpSnap Strapi plugin will be documented in this file.

## [1.0.14] - 2026-05-26
- **Installation Tracking** Implements critical security, reliability, and robustness improvements for installation telemetry and tracking endpoints.

## [1.0.11] - 2026-05-06
### Added
- **Telemetry Installation Tracking**: Implemented a one-time telemetry API call to record plugin installation data (Platform, Plugin Version, Site URL, and Strapi Version) to help gather telemetry.

## [1.0.10] - 2026-04-01
### Added
- Implemented **Port Monitoring** to track specific service availability.
- Implemented **Keyword Monitoring** to verify page content integrity.
### Fixed
- Addressed various PR feedback and code quality improvements.

## [1.0.9] - 2026-03-30
### Added
- Created the **Incidents Page** for historical downtime tracking.
- Added a **Back button** for easier navigation within internal plugin pages.
- Implemented dummy data handling for the dashboard before the user is signed in.
### Changed
- Improved variable naming consistency across the server-side logic.

## [1.0.8] - 2026-03-19
### Added
- Implemented full **Authentication Flow** including Sign-in and Sign-up directly within the plugin.
- Added **Logout functionality** in the Settings panel.
- Added **Verification Expired** handling for secure session management.
### Fixed
- Resolved build errors related to TypeScript types.

## [1.0.7] - 2026-03-05
### Fixed
- Resolved an issue where monitor data could sometimes return `null` during API synchronization.

## [1.0.6] - 2026-03-02
### Fixed
- Fixed the statistics page to correctly display regions with zero response time in the charts.
- Improved visibility of data series in performance graphs.

## [1.0.4] - 2026-02-27
### Fixed
- Fixed **Token Validation** failures when the API token was missing or incorrectly stored.
- Improved error messaging for invalid tokens.
- Fixed automatic redirection when a session becomes invalid.

## [1.0.3] - 2026-02-27
### Changed
- Improved **Version Compatibility** for lower versions of Strapi v5.
- Updated README and package metadata.
### Fixed
- Resolved various minor build issues in production environments.

## [1.0.2] - 2026-02-19
### Fixed
- Fixed **Lighthouse scores** rendering logic to ensure accuracy.
- Cleaned up unnecessary code and temporary files from the build process.
- Improved code formatting across the admin source directory.

## [1.0.1] - 2026-02-18
### Added
- Added **Bulk Delete** actions for monitors and status pages.
- Added a **Regions Dropdown** to filter monitoring data geographically.
- Implemented **Statistics Card UI** and improved loading skeletons.
### Fixed
- Fixed responsiveness issues for the dashboard and chart components across tablet and mobile views.

## [1.0.0] - 2026-02-13
### Added
- Initial release of the UpSnap Strapi plugin.
- Core Features:
  - **Monitors:** Real-time reachability, SSL, and uptime tracking.
  - **Notifications:** Integration with Slack, Discord, Email, and Webhooks.
  - **Status Pages:** Public status page management.
  - **Performance:** Google Lighthouse audits (Mobile & Desktop).
  - **Content Security:** Mixed content and Broken link detection.
  - **Domain Health:** DNS and registration monitoring.
