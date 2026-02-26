# Privacy Policy — Ashen

**Last updated:** February 2026

## 1. Overview

This Privacy Policy explains what data Ashen collects, how it is used, and how it is stored. Ashen is a private Discord bot operating exclusively within the DIYD server.

## 2. Data We Collect

Ashen collects and stores only the data required for its features to function:

**Server configuration data:**
- Mod log channel IDs
- Safeword role and channel settings
- Partner ad channel, rep channel, and preview channel settings
- Streaming status settings

**Partner data:**
- Partner names, invite links, and descriptions
- Scheduled post times and target channels
- Rep user IDs and notification channel IDs

**Moderation data:**
- Discord invite links scanned during audit commands
- Results of invite validity checks (stored in a local log file)

**Whitelist data:**
- Guild IDs and their whitelist expiry dates

## 3. Data We Do Not Collect

Ashen does not collect, store, or process:

- Message content beyond what is necessary to detect safeword role mentions
- Personal information such as usernames, email addresses, or profile data
- Direct messages
- Voice activity or media

## 4. How Data Is Used

All data collected by Ashen is used solely to provide its features within the DIYD server. Data is never sold, shared with third parties, or used for advertising or analytics purposes.

## 5. Data Storage

Data is stored locally on the server hosting Ashen. This includes:

- `bot_config.json` — server settings and configuration
- `data/partners.db` — partner and schedule data (SQLite database)
- `data/guild_whitelist.json` — whitelist entries
- `invite_check_log.txt` — audit scan results

Data is not transmitted to any external service except Discord's own API for normal bot operation.

## 6. OpenAI

Ashen uses the OpenAI API for certain features. When these features are used, relevant content may be sent to OpenAI for processing in accordance with [OpenAI's Privacy Policy](https://openai.com/privacy). No personally identifiable information is intentionally included in these requests.

## 7. Data Retention

Configuration and partner data is retained for as long as the bot is in operation. You may request deletion of specific data by contacting a server administrator through the DIYD server.

## 8. Your Rights

As a DIYD server member you may request:

- Information about what data Ashen holds related to your user ID
- Deletion of your user ID from Ashen's stored data (where applicable)

To make a request, contact a server administrator through the DIYD server.

## 9. Changes to This Policy

This Privacy Policy may be updated at any time. Continued use of the DIYD server following any changes constitutes acceptance of the updated Policy.

## 10. Contact

For questions about this Privacy Policy, reach out through the DIYD server.
