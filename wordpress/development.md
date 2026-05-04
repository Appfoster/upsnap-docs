# Development Guide

This guide covers the architecture, project structure, and coding standards for the UpSnap WordPress plugin.

---

## Project Structure

```text
upsnap-monitoring/
├── admin/                  # Admin-specific logic and UI
│   ├── css/                # Feature-specific stylesheets
│   ├── js/                 # Feature-specific JavaScript (vanilla)
│   ├── partials/           # PHP template parts for admin pages
│   └── class-upsnap-admin.php # Admin menu and asset registration
├── assets/                 # Shared static assets
│   ├── css/                # Global admin styles
│   ├── images/             # Icons and placeholders
│   └── js/                 # Third-party libraries (e.g., ApexCharts)
├── includes/               # Core business logic and services
│   ├── class-upsnap-api.php                # External UpSnap.ai API client
│   ├── class-upsnap-rest-api.php           # WordPress REST API registration
│   ├── class-upsnap-health-check-builders.php # Data normalization
│   └── class-upsnap-token-storage.php      # Secure token management
└── upsnap-monitoring.php   # Main plugin entry point
```

---

## Architecture

### Main Plugin File

The `upsnap-monitoring.php` file initializes the plugin, defines constants, and bootstraps the core components using a hook-based architecture.

---

### Service Layer (`includes/`)

Business logic is decoupled into specialized classes:

- **API Client:** All communication with `api.upsnap.ai` is centralized in `class-upsnap-api.php`.
- **REST API:** The plugin exposes internal endpoints (e.g., `/wp-json/upsnap-monitoring/v1/health-check`) to allow the frontend JS to fetch data asynchronously without blocking page loads.
- **Builders:** The `Health_Check_Builders` class takes raw API data and transforms it into a standardized format for the UI.

---

### Admin Dashboard (`admin/`)

- **Modularity:** Each feature (Reachability, Lighthouse, etc.) has its own JS and CSS file, which are only loaded on their respective admin pages to maintain performance.
- **Partials:** UI components are broken down into small, reusable PHP files in the `partials/` directory.

---

## Development Workflow

### Prerequisites

- WordPress 5.8+ environment (e.g., LocalWP, DevKinsta, or a staging site)
- PHP 7.4 or higher

---

### Local Setup

1. Clone the repository into your `wp-content/plugins` folder.
2. Activate the plugin via the WordPress Dashboard or WP-CLI.
3. Go to **Upsnap → Settings** and log in with your developer account.

---

## Coding Standards

- **WordPress Coding Standards:** Follow WP Coding Standards for all PHP, JS, and CSS.
- **Prefixing:** Always prefix functions, classes, and global variables with `upsnap_` to avoid conflicts.

### Security

- Use `wp_nonce_field` and `check_ajax_referer` for all actions.
- Sanitize all input using `sanitize_text_field()` or similar.
- Escape all output using `esc_html()`, `esc_attr()`, or `wp_kses()`.

---

## API Integration

To add a new monitoring feature:

1. **Core Builder:** Add a new method to `Upsnap_Health_Check_Builders` to handle data normalization.
2. **REST Endpoint:** Register a new route in `class-upsnap-rest-endpoints.php`.
3. **Partial:** Create a new UI template in `admin/partials/`.
4. **Assets:** Create corresponding JS/CSS in `admin/js/` and `admin/css/`.
5. **Admin Class:** Register the new submenu and enqueue assets in `class-upsnap-admin.php`.

---

## Testing

- **Manual Testing:** Verify UI responsiveness and data accuracy across different screen sizes and browsers.
- **REST API Testing:** Use tools like Postman or curl to verify internal REST endpoints.
- **Security Audit:** Ensure nonces are validated and capabilities are checked (`current_user_can('manage_options')`).