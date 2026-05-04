# Domain Health Check

Monitor your domain registration, DNS configuration, and overall domain health directly from your Strapi admin panel.

## Overview
The UpSnap Domain Health Check ensures your domain is properly registered, resolves correctly across the internet, and alerts you well in advance of expiration. It also monitors for any unauthorized changes to your DNS records or WHOIS/RDAP status.

## Features

### Domain Registration & Lifecycle
*   **Expiration Tracking:** Get the exact date your domain expires and a countdown of how many days are remaining.
*   **Registration Status:** Monitor "Expired" and "Expiring Soon" flags to prevent accidental downtime and loss of your domain.
*   **History Tracking:** See when the domain was originally registered and when its record was last updated in the global registry database.

### DNS Record Monitoring
The plugin verifies and displays essential DNS records to ensure your site is reachable and your services are correctly configured:
*   **A/AAAA Records:** Monitor your site's IPv4 and IPv6 addresses.
*   **MX Records:** Verify that your email routing configuration is intact.
*   **NS Records:** Monitor your authoritative nameservers.
*   **TXT Records:** Keep track of verification and security records (e.g., SPF, DKIM, site verifications).
*   **CNAME/Host:** View canonical name and host mapping details.

### Domain Security
*   **Registry Status Codes:** View registry-level EPP status codes (e.g., `clientTransferProhibited`) to ensure your domain is locked and protected from unauthorized transfers.
*   **Change Detection:** Monitor "Last Changed" timestamps to quickly identify unexpected updates to your domain's configuration.

## Usage

### Accessing the Dashboard
1.  In your Strapi Admin Panel, navigate to **Upsnap → Domain Check**.
2.  The page will display several detailed cards summarizing your domain's current health and configuration.

### Understanding the Data

#### General Info
*   **CNAME/Host:** Shows the primary addressing details for your monitor.
*   **Supported:** Indicates if advanced domain health features are active for your specific domain TLD.

#### DNS Records
Displays the current values for IPv4, IPv6, MX, NS, and TXT records as seen by the UpSnap monitoring network.

#### Domain Lifecycle
*   **Registered On:** The date your domain was first created.
*   **Expiration Date:** The deadline for your domain renewal.
*   **Days Until Expiration:** A live countdown to your renewal deadline.
*   **Last Changed:** The last time a change was detected in your domain's registration or DNS.

#### Domain Status Codes
Lists all active EPP status codes from the registry. These indicate if your domain is locked, active, or in a specific lifecycle state (like redemption).

### Manual Refresh
Click the **Refresh** or **Check Now** button in the top right to force a fresh lookup of your domain's WHOIS and DNS data via the UpSnap API.

## Troubleshooting
*   **Incorrect DNS Records:** If the DNS records shown don't match your intended configuration, your changes may still be propagating, or there may be a configuration error at your DNS provider/registrar.
*   **Expiration Warnings:** If you see an "Expiring Soon" warning, log in to your domain registrar immediately to renew your domain and avoid service interruption.
