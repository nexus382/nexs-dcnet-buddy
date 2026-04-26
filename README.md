# Nex's DCNET Buddy

**Binary releases for Nex's DCNET Buddy - the companion app for the Dreamcast online community.**

## Latest Release

### v0.1.3 - 2026-04-26

#### Added
- Websocket-based live updates for DCNET status topics to reduce repeated REST polling
- ETag-aware API cache handling for lighter network use on unchanged data
- Persistent `COMING SOON` chat banner in global chat, game companion chat, and home chat preview

#### Changed
- Refresh flows now update more smoothly across Home, Games, People, and Game Detail screens
- Chat send/post actions continue to show explicit “coming soon” feedback while backend chat is still gated
- Game/presence rendering now favors live state updates and safer fallback behavior

#### Fixed
- Removed broken fallback references to missing mock members (`MockDataService.games` and `MockDataService.players`) that caused Windows build failures
- Included related model/widget/service hardening needed for current production behavior

---

## What This App Does

Nex's DCNET Buddy makes it easy to see who's online, find games, chat with fellow Dreamcast players, and launch directly into Flycast emulator.

- **Who's Online** - See all Dreamcast players currently online
- **Active Games** - Browse games with players right now
- **Pin Games** - Track your favorite games for quick access
- **Quick Launch** - Set up Flycast once, then launch games with one tap

## Downloads

Download the latest release from the [Releases page](https://github.com/nexus382/nexs-dcnet-buddy/releases).

## Source Code

The source code is available in the [dcnet-app](https://github.com/nexus382/dcnet-app) repository.
