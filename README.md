# ZLive
**ZLive** is a comprehensive, event-management and live-broadcast control cog for **ZygnalBot**, created by **TheHolyOneZ (TheZ)**. It is designed specifically for **discord.py setups**, but can also be used in other compatible bot configurations. 
> 💡 **Built for the Zygnal Ecosystem — to download and use this extension, you must be part of the Zygnal Ecosystem.**  
> This extension (cog) is part of the **Zygnal Ecosystem** and is only available through its supported platforms.  
> You can use it with:  
> - The **[Discord Bot Framework](https://github.com/TheHolyOneZ/discord-bot-framework)** — ideal for developers who want full control and flexibility *(includes an integrated extension marketplace)*, or  
> - The **[ZygnalBot](https://zygnalbot.de)** — a prebuilt, plug-and-play Discord bot *(also includes an integrated extension marketplace)*.  
>
> Browse and install extensions at [zygnalbot.com/extension](https://zygnalbot.com/extension).  
> For help or community discussions, join us on Discord: [discord.gg/sgZnXca5ts](https://discord.gg/sgZnXca5ts)
# ZLive

**ZLive** is a comprehensive, event-management and live-broadcast control cog for **ZygnalBot**, created by **TheHolyOneZ (TheZ)**. It is designed specifically for **discord.py setups**, but can also be used in other compatible bot configurations.

It provides hosts, moderators, and administrators with powerful tools to **manage live events, speaker queues, and audience interaction**, all through a clean and intuitive in-Discord interface.

---

## 🧠 Overview

ZLive allows you to create interactive “live session” environments on your Discord server — perfect for podcasts, stage discussions, Q&A events, classrooms, and interviews.

Each session includes its own **speaker queue**, **raise-hand system**, **broadcast controls**, **waiting room**, and **customizable embeds**, making it easy to run professional-grade live events directly within Discord.

---

## ⚡ Hybrid Command System

ZLive is a **hybrid cog**, supporting both **prefix commands** (e.g., `!zlive`, `!zlivehelper`) and **slash commands** (`/zlive`, `/zlivehelper`).
This ensures compatibility with ZygnalBot setups as well as standalone discord.py bots.

---

## 📦 Features

### 🎙️ Live Session Management

* Create, monitor, and control **individual live sessions** per guild.
* Each session has a **unique 8-character session code**.
* Sessions automatically expire after a configurable duration.
* Full support for multiple active sessions per guild.

### ✋ Raise-Hand Queue System

* Attendees can **click a button to join a speaking queue**.
* Supports **waiting room voice channels** or direct event participation.
* Automatically tracks queue order, total count, and active speakers.
* Configurable **queue join limits**, **auto-mute/unmute**, and **re-entry rules**.

### 🎛️ Host Control Panel

* Interactive **control dashboard** with Discord buttons and modals.
* Manage every part of the event without typing commands:

  * Set event and waiting room channels.
  * Configure queue and display embeds.
  * Manage staff, rules, and participant permissions.
  * Invite next speaker, extend time, mute/unmute, and end sessions.
* Real-time updates and persistent configuration per guild.

### 🚪 Waiting Room Mode

* Enable a **dedicated waiting room voice channel** for audience members.
* Event channels are automatically hidden when waiting room mode is on.
* Bot automatically moves speakers between waiting and event channels.
* Ideal for high-traffic or moderated stage events.

### 🧩 Customizable Embeds

* Fully editable **embed templates** for:

  * Queue display
  * Raise-hand panel
  * Broadcast helper
* Use dynamic variables such as:

  ```
  {queue_list}, {queue_count}, {event_channel},
  {waiting_room}, {instructions}, {lock_status}
  ```

### 🧑‍💼 Admin & Global Host System

* Administrators can create sessions for others.
* Global host roles and users can manage or override any session.
* Built-in admin panel with modals for managing hosts, viewing sessions, and extending durations.

### 🕓 Automatic Expiration

* Sessions automatically deactivate after the set duration.
* Expired sessions are cleaned up automatically.

### 🔔 Optional DM Notifications

* Hosts and invited speakers receive DM notifications when sessions start or when it's their turn to speak.

---

## 🧭 Command Summary

| Command                                        | Description                                              |
| ---------------------------------------------- | -------------------------------------------------------- |
| `/zlive` or `!zlive`                           | Opens the main ZLive control panel.                      |
| `/zliveadmin` or `!zliveadmin`                 | Opens the admin management panel (requires admin).       |
| `/zlivehelper <code>` or `!zlivehelper <code>` | Opens a host’s control panel for their session.          |
| `/zlivecleanup`                                | Manually cleans expired sessions.                        |
| `/zlivehelp`                                   | Displays an overview of commands and setup instructions. |

> All commands can be used as either **slash commands** or **prefix commands** — ZLive automatically detects your bot’s configuration.

---

### Initial Setup

1. Run `/zliveadmin` (or `!zliveadmin`) as an admin.
2. Click **“Create Session”** to assign a session to a host.
3. The host receives a code via DM — they use:

   ```
   /zlivehelper <code>
   ```

   or

   ```
   !zlivehelper <code>
   ```

   to access their control panel.
4. Configure event, queue, and waiting room channels.
5. Send the **Raise-Hand** and **Broadcast Helper** panels to start the event.

---

## 📁 Configuration & Storage

Each guild has a configuration file at:

```
data/ZLive/zlive_sessions_<guild_id>.json
```

Contains:

* Active sessions
* Host, staff, and global host data
* Queue and event metadata
* Embed templates and display preferences

Data automatically persists across restarts.

---

## 🧩 Customization Options

* **Embed colors** (`hex`)
* **Session duration** (hours)
* **Queue limits** (number of re-entries per user)
* **Time limits** (per speaker)
* **End-of-time action** (mute or kick)
* **Global host users and roles**
* **DM notifications toggle**

All options are configurable via Discord UI modals — no manual JSON editing required.

---

## ⚙️ Auto-Maintenance

* Background cleanup automatically removes expired sessions.
* Active session data is validated and refreshed on cog load.
* Robust error logging for debugging and audit purposes.

---

## 🪪 License Agreement

This cog is protected under a **Custom License Agreement** by **TheHolyOneZ (TheZ)**.

### Key Restrictions

* **Do not modify** or redistribute the source code.
* **Do not remove or alter** author credits or branding.
* You may **read** the source for educational purposes only.

For complete terms, see the **CUSTOM LICENSE AGREEMENT** section at the top of the code.

---

## ⚠️ Disclaimer

The software is provided **“AS IS”**, without warranty of any kind.
Use at your own risk. The developer assumes no responsibility for damages caused by misuse or modification.

---

## 👤 Credits

**Developer:** [TheHolyOneZ (TheZ)]
**Website:** [https://zygnalbot.com/extension/](https://zygnalbot.com/extension/)
**Discord:** TheHolyOneZ
**Copyright © 2025**

All rights reserved.

---

*ZLive — “Bring structure and control to your live Discord events.”*
