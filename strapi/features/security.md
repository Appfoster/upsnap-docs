# Security Certificates (SSL/TLS)

Monitor your website's SSL/TLS certificate validity, expiry dates, and security configuration directly from your Strapi admin panel.

## Overview
Ensuring your site's security certificate is valid and up-to-date is critical for maintaining user trust and SEO rankings. The UpSnap Security Certificates dashboard provides a detailed breakdown of your SSL status, including automated expiry tracking and certificate chain validation.

## Features

### Real-Time Validation
*   **Health Status:** Instantly see if your certificate is valid, expiring soon, or already expired.
*   **Expiry Countdown:** A clear, color-coded countdown tells you exactly how many days are left before renewal is required.
    *   🟢 **Green:** More than 30 days remaining.
    *   🟡 **Yellow:** 7 to 30 days remaining (Consider renewing soon).
    *   🔴 **Red:** Less than 7 days remaining (Urgent renewal required).

### Detailed Certificate Information
*   **Issuer Details:** Identify the Certificate Authority (CA) that issued your SSL (e.g., Let's Encrypt, Cloudflare, DigiCert).
*   **Validity Period:** View the "Not Before" and "Not After" dates to track your certificate's lifecycle.
*   **Technical Specs:** Monitor the Serial Number, Signature Algorithm, and Public Key Algorithm used for your encryption.

### Domain Coverage & SANs
*   **Wildcard Verification:** Confirms if your certificate covers all subdomains (e.g., `*.yourdomain.com`).
*   **Subject Alternative Names (SANs):** Lists all specific domains and subdomains covered by the current active certificate.

### Certificate Chain Monitoring
The plugin verifies the full chain of trust from your site to the root authority:
*   **End Entity Certificate:** Your specific domain certificate.
*   **Intermediate Certificates:** The links that bridge your certificate to the trusted root.
*   **Root Certificates:** The ultimate source of trust in the certificate chain.

## Usage

### Accessing the Security Dashboard
1.  Navigate to **Upsnap → Security Certificates** in your Strapi Admin Panel.
2.  The **Status Card** will show your overall certificate health and days until expiration.
3.  The **Certificate Details** card provides deep technical information about the active certificate.
4.  **Domain Coverage:** Scroll down to see which specific domains and subdomains are protected by this certificate.
5.  **Chain Validation:** Inspect the full certificate chain to ensure a complete path of trust.

### Manual Refresh
If you have just installed a new certificate and want to verify it immediately, click the **Refresh** or **Check Now** button in the header. This triggers a fresh SSL/TLS audit via the UpSnap API.

## Troubleshooting
*   **"Certificate has expired!":** Your site is now showing security warnings to users. Log in to your hosting provider or certificate authority immediately to renew and reinstall your certificate.
*   **"Chain Issues":** If your certificate is valid but the chain is incomplete, some browsers (especially on mobile) may show "Insecure" warnings. Ensure you have correctly installed the Intermediate/CA Bundle provided by your issuer.
*   **Domain Mismatch:** Ensure the "Subject Alternative Names" list includes the specific URL you are using for your Strapi application.
