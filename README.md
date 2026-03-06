# Roblox Milestone & Update Announcer Bot

This bot announces Roblox game visit milestones and updates to Discord.

## Features
- **Visit Milestone Announcements**: Get notified every X visits (configurable).
- **Game Update Alerts**: Receive notifications when your game is updated.
- **Subplace Detection**: Notifies you when new subplaces/stages are added to the universe.
- **Multiple Game Support**: Track multiple Roblox games with a single bot instance.

---

## Setup & Configuration

### 1. Prerequisites
- [Node.js](https://nodejs.org/) (v16.11.0 or higher recommended)
- A Discord Bot Token (from the [Discord Developer Portal](https://discord.com/developers/applications))
- The Universe ID of your Roblox game.

### 2. Installation
Clone the repository and install dependencies:
```bash
git clone <repository-url>
cd <repository-folder>
npm install
```

### 3. Configuration
1. Rename `.env.example` to `.env`.
2. Open `.env` and fill in your details:

| Variable | Description |
| --- | --- |
| `TOKEN` | Your Discord bot token. |
| `FREQUENCY` | How often to announce visit milestones (e.g., `10000`). |
| `UNIVERSEID` | The Roblox Universe ID (NOT the Place ID). |
| `CHANNELID` | The Discord channel ID for announcements. |

#### How to find your Universe ID:
To get your Universe ID from a Place ID, visit:
`https://apis.roblox.com/universes/v1/places/{YOUR_PLACE_ID}/universe`

#### Tracking Multiple Games:
You can track additional games by adding numbered environment variables:
```env
UNIVERSEID_2=YOUR_SECOND_UNIVERSEID
CHANNELID_2=YOUR_SECOND_CHANNELID
```

### 4. Running the Bot
To start the bot, run:
```bash
node announcer.js
```

---

*The bot checks for updates and milestones every 3 minutes.*
