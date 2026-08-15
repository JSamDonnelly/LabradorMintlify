# Source: https://www.testwithlabrador.com/trust

Trust & Security

# How Labrador protects your audit data

We build accessibility auditing software, and we hold ourselves to the same standard of honesty we ask of the teams we audit. This page describes how your data is handled in plain language, including the things we haven’t built yet.

## Security practices

Encrypted in transit

Every connection uses TLS, with HSTS preloading and automatic upgrades of insecure requests.

Encrypted at rest

Our database and file storage providers encrypt all stored data with AES-256.

Passwords never stored

Passwords are hashed with bcrypt. We cannot see, recover, or tell you your password.

Card data never touches us

Stripe, a PCI DSS Level 1 provider, handles payments. Card numbers never reach our servers.

Two-factor authentication

Optional authenticator-app codes, with single-use recovery codes if you lose your device. You control this yourself.[Manage Account → Two-factor authentication](https://www.testwithlabrador.com/account)

Session control

Changing your password signs out your other devices, and you can end every other session yourself at any time.[Manage Account → Signed-in devices](https://www.testwithlabrador.com/account)

## Your security controls

Everything below is in your account settings. To get there, select the account icon at the top right of any page and choose **Manage Account**, or go straight to [your account page](https://www.testwithlabrador.com/account).

### Turn on two-factor authentication

Under **Two-factor authentication**, choose **Set up**. Then:

1. Add Labrador to an authenticator app — scan the QR code, or choose “enter a setup key” in your app and type the key we show. Scanning is never required.
2. Enter the 6-digit code your app displays and confirm.
3. Save the recovery codes we give you. They are shown once, each works once, and they are how you get in if you lose your phone.

From then on, signing in asks for a code after your password. To turn it off, use **Turn off** in the same place — it asks for your password and a current code, so a stranger at your unlocked laptop can’t simply switch it off.

### Sign out your other devices

Left yourself signed in on a shared or lost computer? Under **Signed-in devices**, choose **Sign out other devices**. Every other session ends immediately; the device you are using stays signed in.

### Change your password

Under **Password**, enter your current and new password. Changing it also signs out your other devices automatically, so a password you think was exposed stops being useful everywhere at once.

## Where your data lives

Your audit records — projects, pages, criterion results, and issues — are stored in a managed PostgreSQL database on Microsoft Azure. Screenshots and file attachments are stored in Microsoft Azure Blob Storage and are reachable only through short-lived signed links scoped to each request, never through public URLs.

All stored data is encrypted at rest, and every connection between your browser, our servers, and our providers is encrypted in transit.

Your data is stored in the United States — both the database and files in Azure East US 2 (Virginia).

## Backups and retention

The database is backed up automatically every night, with point-in-time recovery covering the previous 35 days. A separate daily backup is written to an independent system (GitHub, listed under third-party services below) and kept for 30 days, so no single provider or account ever holds the only copy of your data. Access to backups is limited to Labrador's engineering team.

When you delete something — an issue, a page, or a whole project — it is removed from the live database immediately; we use hard deletes, not hidden flags. Deleted data then ages out of every backup within 35 days.

## Access to your audits

Every request for project data is checked on the server against project ownership, team membership, and per-project roles before any data is returned. Plan limits are enforced server-side as well, not merely hidden in the interface.

All database access runs through a single layer using parameterized queries, so audit content you enter is never interpreted as a database command.

## Signing in

You can sign in with an email and password or with Google. Sign-in tokens are held in cookies that page scripts cannot read, and repeated failed attempts temporarily lock an account to slow down guessing.

Two-factor authentication is available on any password account, and off until you switch it on — see [Your security controls](https://www.testwithlabrador.com/trust#security-controls) above for how. Accounts that sign in with Google use whatever two-step verification is set on the Google account itself.

## Subprocessors

These third-party services may process your data. We update this list before adding a new one. Nothing is sent to our AI provider unless you ask for a remediation suggestion on a specific issue.

Third-party services Labrador uses and the data each one handles
| Provider | Purpose | Data involved |
| --- | --- | --- |
| Microsoft Azure | Primary database and file storage | Audit records, account data, screenshots, attachments |
| GitHub | Independent daily database backups; source code hosting | Encrypted backup copies of audit and account records, kept 30 days |
| Stripe | Billing and payments | Billing details; card data stays with Stripe |
| Anthropic | AI remediation suggestions, when you ask for one | The issue description and the page markup for that issue |
| Google | Optional sign-in, site analytics | Email and name at sign-in; usage events |
| Intercom | Support chat | Name, email, support conversations |
| Mailmodo | Account and marketing email | Name and email address |
| Mixpanel | Product analytics | Feature-usage events |
| LinkedIn | Advertising analytics on public marketing pages | Visits to public pages; never audit data |
| Sentry | Error monitoring | Technical error reports |
| Wistia | Video hosting on marketing pages | Viewing analytics on public pages |

## Deleting your data

Email [security@testwithlabrador.com](mailto:security@testwithlabrador.com) from your account address and we will delete your account and its audit data within 30 days. There is no button for this yet — a person handles the request, and we will confirm when it is done. Self-service deletion is on our roadmap.

## What we haven’t built yet

Trust pages usually stop at the good news. Here is the rest, so you can make an informed decision:

- **Single sign-on (SAML)** is not yet available.
- **Organisation-wide enforcement of two-factor authentication** is not yet available; individuals can enable it for themselves today.
- **SOC 2 certification** is planned for when our enterprise customers need it. Our practices are built so that the audit is a formality rather than a scramble.

## Security questionnaires

Evaluating Labrador for your organisation? We are glad to complete standard security questionnaires, including CAIQ-Lite and HECVAT for higher-education procurement. Email [security@testwithlabrador.com](mailto:security@testwithlabrador.com) and we will normally return them within a few business days.

## Reporting a vulnerability

If you believe you have found a security issue in Labrador, email [security@testwithlabrador.com](mailto:security@testwithlabrador.com). We will acknowledge your report within two business days, keep you informed as we investigate, and credit you if you would like. Please give us reasonable time to fix an issue before disclosing it publicly.