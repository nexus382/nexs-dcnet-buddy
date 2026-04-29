# Nex's DCNET Buddy

**The companion app for the Dreamcast online community.**

The Dreamcast was ahead of its time — the first console with true online multiplayer from your living room through your telephone line. It died before it should have, but the community kept it alive. Today, DCNET brings that original experience back, and **DCNET Buddy** makes finding players just as easy as the games themselves.

---

## The Dreamcast Story

The Dreamcast had it all: amazing games, many with built-in netplay. It was the first system to deliver real online multiplayer into living rooms nationwide. Then it was gone too soon.

Fortunately, the community never stopped playing. DCNET has revived the original online experience:

- **No setup required** — works with Flycast, the #1 rated and downloaded Dreamcast emulator
- **Real hardware support** — connect your actual Dreamcast via DreamPI with support for VMU, Rumble, and any controller through DreamPicoPort
- **Full VMU emulation** — DreamPotato integration brings complete VMU functionality to Flycast, in heavy active development
- **Minimal data usage** — online gameplay uses next to nothing (~0.5 Mbps), so 2 GB/day gives you a perfect experience all day long
- **Hybrid play** — connect your real Dreamcast OR emulator to DCNET and play with everyone

**The problem?** Finding other players was nearly impossible. DCNET Buddy solves that — see who's online, what they're playing, and get into the game in seconds.

---

## Features

### Core Functionality
- **Real-Time Player Discovery** — live player list across all 33 DCNET games with game-specific presence
- **Status Indicators** — quick visual badges showing who's in lobby, in-game, away, or offline
- **Friends System** — add players by display name, track online status, stored locally
- **Privacy Controls** — Public, Friends Only, or Private profile visibility

### Game Browsing & Launch
- **Complete Game Library** — all 33 DCNET games with live player and lobby counts
- **One-Tap JOIN** — launch directly into Flycast from the app
- **Auto-Detect ROMs** — app scans your game folder and finds matching ROMs automatically
- **ROM Binding** — bind ROM files to each game profile
- **Verify Before JOIN** — test that everything works before launching
- **Game Setup Guides** — step-by-step instructions for PSO, Quake III, SW Super Bombad Racing, and more
- **Pin Favorites** — track your go-to games at the top of the home screen

### Real-Time Chat
- **Global Chat** — message the whole DCNET community with timestamps
- **Game-Specific Rooms** — chat within a game's lobby context
- **Predefined Messages** — quick phrases like "LF 1 more player" for fast coordination
- **Hybrid Mode** — custom values in preset messages (player count, minutes remaining)
- **Chat History Persistence** — Firebase Realtime Database stores messages

### Notifications & Sounds
- **Toast Notifications** — on-screen alerts for messages, player joins, lobby changes, friend online
- **Custom Sound Effects** — distinct tones for boot, messages, success, and back navigation
- **Per-Type Toggle** — enable/disable notifications for each event type independently
- **Master Tones Toggle** — one switch to mute all sound effects
- **Windows Background Notifications** — WinToast alerts when app is not in foreground

### Presence & Activity
- **Global Presence** — show when you're actively using the app
- **Per-Game Presence** — join a game's "room" when you're playing
- **Activity Tracking** — app knows you're active even with passive use
- **Event-Driven Refresh** — presence updates on room entry, activity, and 30s in-room polls

### Quick Launch Integration
- **Flycast Path Configuration** — set your flycast.exe path once in Settings
- **Direct Launch** — boot straight into the game from the app
- **Setup Verification** — confirms your profile is configured correctly

---

## Getting Started

### 1. Download the Latest Release

1. Download the latest release from GitHub
2. Extract the zip file - leave the .exe in the extracted folder
3. Create a shortcut on your desktop if you want quick access

### 2. First-Time Setup

1. Launch the app
2. Go to **Settings** and set your **display name** - must match your DCNET username
3. Configure your **Flycast path** (location of flycast.exe)
4. Configure your **game library folder** (where your ROMs are stored)
5. For each game you want quick-launch access to, tap **Set up JOIN** - auto-detect will find your ROM, or browse manually
6. Tap **Save**, then tap **Verify** to confirm

**Recommended:** Spend 5 minutes setting up JOIN for all your games now, so they're ready when you need them.

### 3. Quick Launch Integration

With DCNET Buddy, you can go from cold start to netplay screen in about **3 seconds**:
- Traditional startup: 2-5 minutes of manual navigation
- With DCNET Buddy: Single click from this app → Flycast launches → Game loads → Netplay screen ready

Just tap **JOIN** on any configured game and Flycast opens directly to that game's netplay screen.

---

## App Screens

### Home
Online players, hot games with most players, recent chat preview, server status indicator.

### Games
All 33 DCNET games with live player/lobby counts, JOIN setup flow with ROM binding, verification system, and pin favorites.

### Chat
Real-time global chat room with message history, predefined message mode, and online player count header.

### Players
Tabbed view (Online / Looking / All), player cards with status and current game, friend management.

### Settings
Display name, Flycast/ROM paths, notification toggles, theme selection (Light / Dark / System), auto-refresh interval, privacy controls, update checker.

---

## Status Indicators

| Color | Meaning |
|-------|---------|
| 🟢 Green | Online, in lobby, or joinable |
| 🔵 Blue | Currently in a game |
| 🟠 Orange | Loading a game |
| 🟡 Yellow | Away or needs verification |
| ⚪ Grey | Offline |

---

## Privacy

| Level | What Others See |
|-------|-----------------|
| **Public** | Everyone can view your profile |
| **Friends Only** | Only your friends can see you |
| **Private** | No one can see your profile |

---

## Troubleshooting

**"Configure Flycast" shows instead of JOIN**
→ Go to **Settings → Flycast Path** and enter the full path to flycast.exe.

**No games showing**
→ The app connects to the live DCNET server. If no games appear, the server may be temporarily unavailable.

**Chat messages not sending**
→ Check your Firebase configuration. Chat requires Firebase Realtime Database for message sync.

**Can't verify JOIN profile**
→ 1. Confirm Flycast path is correct in Settings
→ 2. Verify ROM file exists at the specified path
→ 3. Try setting up JOIN again from the Games screen

---

## Technical Stack

- **Flutter** — cross-platform (Windows, Android)
- **WebSocket** — real-time presence and status updates
- **Firebase Realtime Database** — chat message persistence
- **audioplayers** — sound effect playback

### Architecture
- API-first design with in-memory caching
- Shared WebSocket connections per topic
- Debounced screen refreshes to prevent burst loops
- Best-effort presence writes (non-fatal)

---

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## License

MIT License — free to use, modify, and distribute.

---

## Acknowledgments

- The **Dreamcast community** — for keeping the online scene alive for 25+ years
- **Flycast emulator team** — for making Dreamcast accessible on modern hardware
- **DCNET project** — for bringing the original online experience back to life
- All contributors who help maintain this project

**Questions? Issues?**
Open an issue on GitHub or reach out to the DCNET community.

Happy gaming! 🎮
