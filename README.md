# 🎙️ Bryan Voice

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:09090f,50:3730a3,100:7c3aed&height=220&section=header&text=BRYAN%20VOICE&fontSize=52&fontColor=ffffff&fontAlignY=38&desc=Your%20Voice.%20Your%20Rules.&descSize=18&descAlignY=58&animation=fadeIn" width="100%" alt="Bryan Voice animated header" />

<a href="https://discord.js.org/"><img src="https://img.shields.io/badge/Discord.js-v14-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Discord.js"></a>
<a href="https://www.typescriptlang.org/"><img src="https://img.shields.io/badge/TypeScript-5.7-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"></a>
<a href="https://nodejs.org/"><img src="https://img.shields.io/badge/Node.js-18%2B-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js"></a>
<a href="https://www.mongodb.com/"><img src="https://img.shields.io/badge/MongoDB-Atlas-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB"></a>
<a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-white?style=for-the-badge&logo=opensourceinitiative&logoColor=black" alt="MIT License"></a>

<br/>

**A modern Discord temporary voice channel management bot.**

Create rooms instantly, manage permissions, control access, and give your community a seamless voice experience.

[Features](#-features) · [Architecture](#-architecture) · [Installation](#-installation) · [Commands](#-commands) · [Configuration](#-configuration)

</div>

---

## ✨ Bryan Voice Features

- ⚡ **Fast Room Creation** — Automatically create temporary voice channels when members join a configured generator.
- 🎛️ **Interactive Controls** — Lock, unlock, hide, rename, and manage rooms.
- 🛡️ **Anti-Abuse Protection** — Help prevent unwanted access and repeated join attempts.
- 👑 **Smart Ownership** — Support ownership transfers and room claiming.
- 💾 **Persistent Storage** — Cache frequently accessed state and persist configuration using MongoDB.
- 🎨 **Dynamic Emojis** — Synchronize application emojis with fallback support.

---

## 🚀 Installation

```bash
git clone https://github.com/YOUR_USERNAME/bryan-voice.git
cd bryan-voice
npm install
cp .env.example .env
npm run build
npm start
```

Replace `YOUR_USERNAME` with your GitHub username and make sure the repository name and npm scripts match your actual project.

## 🎙️ Commands

| Command | Description |
|---|---|
| `.v setup` | Configure voice generators and panels |
| `.v panel` | Send the control panel |
| `.v lock` / `.v unlock` | Control room access |
| `.v hide` / `.v unhide` | Control room visibility |
| `.v name <name>` | Rename a room |
| `.v limit <0-99>` | Set the member limit |
| `.v permit <@user>` | Allow a user into the room |
| `.v reject <@user>` | Deny access to a user |
| `.v claim` | Claim an eligible abandoned room |
| `.v info` | View room information |
| `.v ab` | Toggle anti-abuse protection |

## 🔐 Configuration

```ini
DISCORD_TOKEN=your_bot_token_here
CLIENT_ID=your_client_id_here
MONGODB_URI=mongodb://localhost:27017/bryan_voice
DEFAULT_PREFIX=.v
AUTO_LOAD_EMOJIS=true
```

Never commit your bot token or database credentials to a public repository.

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:7c3aed,50:3730a3,100:09090f&height=120&section=footer" width="100%" alt="Bryan Voice purple footer"/>

**BRYAN VOICE**

<sub>Your Voice. Your Rules.</sub>

</div>
