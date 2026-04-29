# Nex's DCNET Buddy

**Binary releases for Nex's DCNET Buddy - the companion app for the Dreamcast online community.**

## Latest Release

### v0.2.0 - 2026-04-29

#### Added
- **Real-Time Chat System** - Global and game-specific chat rooms with message persistence via Firebase RTDB
- **Preset Message Buttons** - Quick communication with predefined messages
- **Hybrid Messages** - Customizable values in some preset messages (minutes, player count)
- **Presence Tracking** - Global app users and per-game chat presence with online status
- **Friends System** - Add and manage friends by display name, stored locally
- **Setup Guides** - In-game help with step-by-step instructions for each game
- **Live Stats** - Home/Games screens show Players, Lobbies, and App Users counts

#### Changed
- App user presence counting ignores stale entries for accurate counters
- Per-game app-user counts from one shared presence poll instead of per-room scans
- Presence refresh is event-driven: room entry, activity, 30s in-room poll
- Global app-users fetch preserves last known list on read failure
- Efficient server communication with best-effort presence writes

#### Fixed
- Chat and presence screens no longer freeze when presence writes fail
- Message streams initialize even if presence endpoints error
- Presence writes are best-effort and non-fatal

---

## What This App Does

Nex's DCNET Buddy makes it easy to see who's online, find games, chat with fellow Dreamcast players, and launch directly into Flycast emulator.

- **Who's Online** - See all Dreamcast players currently online with presence
- **Active Games** - Browse games with real-time player/lobby/app-user stats
- **Real-time Chat** - Global and game-specific chat rooms with preset messages
- **Pin Games** - Track your favorite games for quick access
- **Quick Launch** - Set up Flycast once, then launch games with one tap

## Downloads

Download the latest release from the [Releases page](https://github.com/nexus382/nexs-dcnet-buddy/releases).

## Source Code

The source code is available in the dcnet-app repository.
