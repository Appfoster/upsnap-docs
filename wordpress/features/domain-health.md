# Domain Health Check

Monitor your domain registration, DNS configuration, and overall domain health directly from your WordPress dashboard.

## Overview
The UpSnap Domain Health Check ensures your domain is properly registered, resolves correctly across the internet, and alerts you well in advance of expiration. It also monitors for any unauthorized changes to your DNS records or WHOIS status.

## Features

### Domain Registration & Lifecycle
*   **Expiration Tracking:** Get the exact date your domain expires and how many days are remaining.
*   **Registration Status:** Monitor "Expired" and "Expiring Soon" flags to prevent accidental downtime.
*   **History:** Track when the domain was originally registered and when its record was last updated in the RDAP/WHOIS database.

### DNS Record Monitoring
The plugin verifies and displays essential DNS records to ensure your site is reachable:
*   **A/AAAA Records:** Monitor your site's IPv4 and IPv6 addresses.
*   **MX Records:** Verify that your email routing configuration is intact.
*   **NS Records:** Monitor your authoritative nameservers.
*   **TXT Records:** Keep track of verification and security records (SPF, DKIM, etc.).
*   **CNAME/Host:** View canonical name and host mapping details.

### Domain Security
*   **Registry Status Codes:** View registry-level status codes (e.g., `clientTransferProhibited`) to ensure your domain is locked and protected from unauthorized transfers.
*   **Change Detection:** Monitor "Last Changed" timestamps to identify unexpected updates to your domain's configuration.

## Usage

### Accessing the Dashboard
1.  In your WordPress Admin, go to **Upsnap → Domain Check**.
2.  The page will display several detail cards summarizing your domain's health.

### Understanding the Data

#### General Info
*   **CNAME/Host:** Shows the primary addressing details for your monitor.
*   **Supported:** Indicates if advanced domain health features are active for this domain.

#### DNS Records
Displays the current values for IPv4, IPv6, MX, NS, and TXT records as seen by the global monitoring network.

#### Domain Lifecycle
*   **Registered On:** The date your domain was first created.
*   **Expiration Date:** When you need to renew your domain.
*   **Days Until Expiration:** A countdown to your renewal deadline.
*   **Last Changed:** The last time any significant change was detected in your domain's registration or DNS.

#### Domain Status Codes
Lists all active EPP status codes from the registry. These tell you if your domain is locked, active, or in a pending state.

### Manual Refresh
Click the **Check Now** button in the top right to force a fresh lookup of your domain's WHOIS and DNS data via the UpSnap API.

## Troubleshooting
*   **Incorrect DNS Records:** If the DNS records shown don't match your intended configuration, your changes may still be propagating, or there may be a configuration error at your DNS provider.
*   **Expiration Warnings:** If you see an "Expiring Soon" warning, log in to your domain registrar (e.g., Namecheap, GoDaddy) immediately to renew.
