# 🎙️ Bryan Voice

<div align="center">

<a href="https://github.com/YOUR_USERNAME/bryan-voice">
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:05050A,25:17102D,60:5126B5,100:9B5CFF&height=260&section=header&text=BRYAN%20VOICE&fontSize=64&fontColor=FFFFFF&fontAlignY=38&desc=NEXT-GEN%20TEMPORARY%20VOICE%20MANAGEMENT&descSize=14&descAlignY=60&animation=fadeIn&stroke=9B5CFF&strokeWidth=1" width="100%" alt="Bryan Voice — premium animated purple header"/>
</a>

<br/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=17&duration=2500&pause=700&color=B99AFF&center=true&vCenter=true&width=650&lines=YOUR+VOICE.+YOUR+RULES.;INSTANT+TEMPORARY+VOICE+ROOMS.;BUILT+FOR+MODERN+DISCORD+COMMUNITIES." alt="Animated Bryan Voice tagline"/>

<br/><br/>

<a href="https://discord.js.org/"><img src="https://img.shields.io/badge/DISCORD.JS-v14-8B5CF6?style=for-the-badge&logo=discord&logoColor=white" alt="Discord.js"/></a>
<a href="https://www.typescriptlang.org/"><img src="https://img.shields.io/badge/TYPESCRIPT-5.7-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"/></a>
<a href="https://nodejs.org/"><img src="https://img.shields.io/badge/NODE.JS-18%2B-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js"/></a>
<a href="https://www.mongodb.com/"><img src="https://img.shields.io/badge/MONGODB-ATLAS-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB"/></a>
<a href="LICENSE"><img src="https://img.shields.io/badge/LICENSE-MIT-E9D5FF?style=for-the-badge&logo=opensourceinitiative&logoColor=black" alt="MIT License"/></a>

<br/><br/>

**Not just another voice bot. A better way to control your server's voice experience.**

Create temporary voice rooms, manage access, customize permissions, and keep your community organized through a streamlined Discord experience.

<br/>

<a href="#-experience"><img src="https://img.shields.io/badge/EXPLORE-FEATURES-7C3AED?style=for-the-badge" alt="Explore features"/></a>
<a href="#-quick-start"><img src="https://img.shields.io/badge/GET-STARTED-17102D?style=for-the-badge" alt="Get started"/></a>

<br/><br/>

<img src="https://user-images.githubusercontent.com/74038190/212284100-561aa473-3905-4a80-b561-0d28506553ee.gif" width="75%" alt="Animated divider"/>

</div>

---

<div align="center">

## ✦ THE BRYAN VOICE EXPERIENCE

<sub>PRECISION · CONTROL · SIMPLICITY</sub>

</div>

<table>
<tr>
<td width="50%" valign="top">

<h3>⚡ Instant Room Creation</h3>

Create temporary voice rooms when members join a configured generator. Automatically move members into their new rooms.

</td>
<td width="50%" valign="top">

<h3>🎛️ Total Room Control</h3>

Lock, unlock, hide, rename, limit, and manage room access through commands and interactive controls.

</td>
</tr>
<tr>
<td width="50%" valign="top">

<h3>🛡️ Intelligent Protection</h3>

Support room-level anti-abuse controls, access checks, and moderation actions for private voice spaces.

</td>
<td width="50%" valign="top">

<h3>👑 Ownership Management</h3>

Handle room ownership changes and allow eligible members to claim abandoned rooms.

</td>
</tr>
<tr>
<td width="50%" valign="top">

<h3>💾 Cache-First Architecture</h3>

Use in-memory state for frequent operations and MongoDB for persistent configuration and data.

</td>
<td width="50%" valign="top">

<h3>🎨 Custom Visual Identity</h3>

Synchronize custom application emojis where supported, with fallbacks when an emoji is unavailable.

</td>
</tr>
</table>

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:17102D,50:38206D,100:17102D&height=3&section=header" width="100%" alt="Purple separator"/>

</div>

## ◈ Architecture

Bryan Voice is designed around responsive Discord interactions, room ownership checks, temporary channel lifecycle management, and persistent configuration.

```mermaid
flowchart TB
    A(["MEMBER JOINS GENERATOR"]) --> B["CREATE TEMPORARY ROOM"]
    B --> C["MOVE MEMBER"]
    C --> D["APPLY ROOM PERMISSIONS"]
    D --> E[("UPDATE IN-MEMORY STATE")]
    E --> F[("PERSIST TO MONGODB")]

    G["INTERACTIVE CONTROL"] --> H["VALIDATE REQUEST"]
    H --> I{"AUTHORIZED?"}
    I -->|Yes| J["EXECUTE ROOM ACTION"]
    I -->|No| K["REJECT REQUEST"]
    J --> E

    style A fill:#241447,stroke:#9B5CFF,color:#FFFFFF
    style B fill:#241447,stroke:#9B5CFF,color:#FFFFFF
    style D fill:#241447,stroke:#9B5CFF,color:#FFFFFF
    style E fill:#31205B,stroke:#B99AFF,color:#FFFFFF
    style F fill:#102B24,stroke:#34D399,color:#FFFFFF
    style I fill:#38206D,stroke:#B99AFF,color:#FFFFFF
```

### Performance philosophy

| Component | Objective |
|---|---|
| Interaction handling | Respond promptly and acknowledge interactions appropriately |
| Channel lifecycle | Minimize unnecessary Discord API operations |
| Authorization | Validate ownership and permissions before changes |
| State management | Cache frequently accessed data |
| Persistence | Handle database failures without silently losing data |
| Reliability | Handle API errors, rate limits, and stale rooms |

> Actual latency, CPU consumption, and memory usage depend on the implementation and deployment environment. Add verified benchmark results here when available.

---

## ◈ Quick Start

<div align="center">

<sub>GET UP AND RUNNING IN FOUR STEPS</sub>

</div>

### 01 — Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/bryan-voice.git
cd bryan-voice
```

### 02 — Install dependencies

```bash
npm install
```

### 03 — Configure your environment

```bash
cp .env.example .env
```

Add your credentials to `.env`:

```ini
DISCORD_TOKEN=your_bot_token_here
CLIENT_ID=your_client_id_here
MONGODB_URI=mongodb://localhost:27017/bryan_voice
DEFAULT_PREFIX=.v
AUTO_LOAD_EMOJIS=true
```

### 04 — Build and launch

```bash
npm run build
npm start
```

These commands assume the repository has the listed files and npm scripts. Replace the repository URL and adjust the commands to match your actual project.

---

## ◈ Command Center

<details open>
<summary><strong>🎙️ Voice Room Controls</strong></summary>

| Command | Action |
|---|---|
| `.v setup` | Configure generators, categories, themes, and panels |
| `.v panel` | Send the voice management panel |
| `.v needhelp` | Move to the configured help voice room |
| `.v lock` | Restrict new connections |
| `.v unlock` | Reopen the room |
| `.v hide` | Hide the room from unauthorized members |
| `.v unhide` | Restore room visibility |
| `.v name <name>` | Rename the room |
| `.v limit <0-99>` | Change the member limit |
| `.v permit <@user>` | Grant a user access |
| `.v reject <@user>` | Deny access to a user |
| `.v claim` | Claim an eligible abandoned room |
| `.v info` | Display room details |
| `.v ab` | Toggle anti-abuse protection |

</details>

<details>
<summary><strong>🔐 Discord Application Requirements</strong></summary>

Configure your application in the [Discord Developer Portal](https://discord.com/developers/applications).

Enable only the privileged intents your implementation actually requires:

- **Message Content Intent** for ordinary prefix-command parsing.
- **Server Members Intent** for features that depend on privileged member data or events.
- **Presence Intent** for presence-dependent functionality.

Grant only the bot permissions needed for its configured features. Avoid granting Administrator by default.

</details>

<details>
<summary><strong>🧰 Production Checklist</strong></summary>

- [ ] Store secrets outside source control.
- [ ] Validate room ownership and permissions on every relevant action.
- [ ] Handle Discord rate limits and API failures.
- [ ] Clean up empty temporary channels.
- [ ] Recover gracefully from process restarts.
- [ ] Test ownership transfers and permission overwrites.
- [ ] Monitor errors and database connectivity.
- [ ] Measure real performance before publishing benchmarks.

</details>

---

## ◈ Project Configuration

| Setting | Description |
|---|---|
| `DISCORD_TOKEN` | Bot authentication token |
| `CLIENT_ID` | Discord application identifier |
| `MONGODB_URI` | MongoDB connection string |
| `DEFAULT_PREFIX` | Default text-command prefix |
| `AUTO_LOAD_EMOJIS` | Toggle automatic emoji synchronization |

**Security note:** Never commit `.env` files or publish bot tokens. If a token is exposed, reset it immediately.

---

## ◈ Contributing

Want to improve Bryan Voice?

1. Fork the repository.
2. Create a feature branch.
3. Implement and test your changes.
4. Open a pull request with a clear description.

Bug reports and practical improvements are welcome.

## ◈ License

Bryan Voice is distributed under the **MIT License**. See [`LICENSE`](LICENSE) for the full license text.

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:9B5CFF,35:5126B5,70:17102D,100:05050A&height=180&section=footer&animation=fadeIn" width="100%" alt="Bryan Voice animated purple footer"/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=18&duration=3000&pause=1000&color=B99AFF&center=true&vCenter=true&width=500&lines=BRYAN+VOICE;YOUR+VOICE.+YOUR+RULES." alt="Bryan Voice closing animation"/>

<br/>

<sub>CRAFTED FOR COMMUNITIES. BUILT FOR CONTROL.</sub>

</div>
