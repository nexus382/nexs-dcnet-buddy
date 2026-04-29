# Nex's DCNET Buddy

**Binary releases for Nex's DCNET Buddy - the companion app for the Dreamcast online community.**

## Latest Release

### v0.1.4 - 2026-04-29

#### Added
- **Firebase RTDB-backed preset chat** - predefined message buttons, minutes/game picker, real send/read flow
- Game detail top stats now includes an **App Users** count alongside Players and Lobbies
- Home screen now shows a top stats row for **Players**, **Lobbies**, and **App Users**
- Games screen top stats shows **Players**, **Lobbies**, and **App Users**
- Game cards now show per-game **App Users** counts from `presence/game_chats`
- Firebase RTDB rules document and allow `presence/app_users` and `presence/game_chats` paths

#### Changed
- Global app-user parsing now tolerates missing `userId`/`lastSeenAt` fields for mixed-client compatibility
- Per-game app-user counts fetched via one shared `presence/game_chats` poll (10s interval) instead of per-room scans
- Presence refresh logic is leaner: game-chat users refresh on room entry, activity, and 30-second in-room poll
- Global app-users fetch preserves last known list on read failure instead of forcing synthetic entries

#### Fixed
- Chat and presence screens no longer freeze when presence writes fail
- Chat message streams initialize and update even if presence endpoints error
- Game chat/app presence heartbeat writes are now best-effort and non-fatal
- App user presence counting now ignores stale entries for accurate counters

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

The source code is available in the [dcnet-app](https://github.com/nexus382/dcnet-app) repository.