# Ashen

> Private Discord bot for the DIYD server.

Ashen is a custom-built Discord bot handling moderation, partner management, scheduled announcements, and server utilities for DIYD. It is not a public bot and is not available for invite.

---

## Features

**Moderation**
- Invite link scanning and audit across any channel
- Purge invite messages from a specific user
- Ban + purge in one command
- Configurable mod log channel
- Safeword system — pings a designated role and logs the trigger silently to mods

**Partner Management**
- Add, edit, deactivate, and reactivate partner entries
- Store partner invite links and descriptions
- Rep system — automatically pings a designated rep user after every ad post
- Per-partner rep channel overrides
- Ad preview without triggering pings
- Quick ping — instantly post a partner's stored ad on demand

**Scheduling**
- Schedule recurring partner posts by day and time or cron expression
- Dual timezone support — America/New York (ET) and Europe/Dublin (IST)
- View all active schedules with next run times in both timezones
- Reschedule or cancel individual jobs without restarting the bot

**Server Utilities**
- Uptime display
- Customisable streaming status with purple activity icon
- Guild whitelist system — bot auto-leaves any server it hasn't been authorised for

**Developer Tools**
- Live service log viewer via Discord (`!journal`)
- Slash command guild sync (`!sync`)
- Job debug output for scheduled tasks
- Whitelist management with expiry and auto-pruning

---

## Stack

- Python 3.10+
- [discord.py](https://github.com/Rapptz/discord.py)
- [APScheduler](https://apscheduler.readthedocs.io/) — recurring job scheduling
- [aiosqlite](https://aiosqlite.omnilib.dev/) — async SQLite for partner/schedule data
- [openai](https://github.com/openai/openai-python) — used for select features
- [python-dotenv](https://github.com/theskumar/python-dotenv) — environment variable management

---

## Project Structure

```
ashen/
├── ashen.py              # Main bot file — core commands and events
├── cogs/
│   ├── partner.py        # Partner management and ad commands
│   ├── scheduler.py      # Cron-based scheduling for partner posts
│   └── whitelist.py      # Guild whitelist and auto-leave system
├── data/
│   ├── partners.db       # SQLite database (auto-created)
│   └── guild_whitelist.json
├── bot_config.json       # Runtime config (auto-created)
├── .env                  # Environment variables (not committed)
└── .env.example
```

---

## Environment Variables

```env
BOT_TOKEN=
OPENAI_API_KEY=
DEV_LOG_CHANNEL_ID=
CONFIG_FILE=bot_config.json
LOG_FILE=invite_check_log.txt
SUMMARY_CHANNEL_ID=
FETCH_LIMIT=
```

---

## Running

```bash
python3.10 -m venv venv
source venv/bin/activate
pip install discord.py openai aiosqlite apscheduler cron-descriptor python-dotenv
python ashen.py
```

For persistent deployment, a systemd service is recommended.

---

## Legal

- [Terms of Service](./terms-of-service.md)
- [Privacy Policy](./privacy-policy.md)

---

*Ashen is a private project. Not open for contributions or public use.*
