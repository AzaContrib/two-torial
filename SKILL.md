# TWO-TORIAL Arcade Knowledge Skill

## Overview

**Skill Name:** `two-torial-arcade`  
**Version:** 1.0.0  
**Description:** An AI agent skill powered by TWO-TORIAL — the community-maintained compendium for arcade rhythm game setup, configuration, troubleshooting, and error code lookup.  
**Source:** [https://two-torial.xyz/](https://two-torial.xyz/) | [GitHub Repository](https://github.com/two-torial/two-torial)

---

## Purpose

This skill enables AI agents to answer common questions about:
- Setting up and configuring arcade rhythm games on PC
- Diagnosing and resolving errors and crashes
- Configuring controllers and hardware
- Patching and modding game data
- Networking arcade cabinets (cab-to-cab / LAN play)
- Understanding BEMANI, SEGA, and NAMCO arcade game ecosystems

---

## Capabilities

| Capability | Description |
|---|---|
| **Game Setup** | Step-by-step guidance for first-time setup of supported games |
| **Troubleshooting** | Diagnose crashes, boot failures, audio issues, and more |
| **Error Code Lookup** | Decode error messages from BEMANI and SEGA games |
| **Controller Configuration** | Configure arcade and PC controllers for each game |
| **Game Patching** | Guide through Spice2x, web-based, or manual hex patching |
| **Audio Setup** | Configure WASAPI/ASIO audio to minimize latency and crashes |
| **Networking** | Set up local network servers (Asphyxia Core, SoftEther VPN) |
| **Data Mods** | Install Omnimix or other data modifications |
| **Hardware Guidance** | Identify ASC vendors, arcade parts, and touch monitor requirements |

---

## Knowledge Domains

### Supported Games

#### BEMANI (Konami)
| Game | Versions |
|---|---|
| beatmania IIDX | 9th, 10th, 11 RED, 12 HAPPY SKY, 13 DistorteD, 14 GOLD, 24 SINOBUZ, 25 CANNON BALLERS, 26 Rootage, 27 HEROIC VERSE, 30 RESIDENT, 31 EPOLIS, 32 Pinky Crush |
| Sound Voltex (SDVX) | IV HEAVENLY HAVEN, V VIVID WAVE, VI EXCEED GEAR |
| Pop'n Music | Usaneko, Peace, HELLO Pop'n |
| Dance Dance Revolution | DDR Ace |
| Jubeat | Clan |
| GITADORA | Matixx, EXCHAIN, FUZZ-UP |
| Reflec Beat | Reflesia |
| NOSTALGIA | FORTE, Op.2 |
| BeatStream | アニムトライヴ (final) |
| MÚSECA | 1+1/2 |

#### SEGA
| Game | Versions |
|---|---|
| CHUNITHM | NEW, NEW PLUS, SUN, SUN PLUS, LUMINOUS, LUMINOUS PLUS, VERSE |
| maimai DX | BUDDiES |
| O.N.G.E.K.I. | bright MEMORY |

#### NAMCO
| Game | Versions |
|---|---|
| Taiko no Tatsujin | Nijiiro |

### Cross-Game Topics
- BEMANI error codes (comprehensive database)
- SEGA error codes (comprehensive database)
- SpiceTools / Spice2x patching
- Web-based game patching
- Manual hex patching
- WASAPI & ASIO audio configuration
- Exclusive audio stream workarounds
- Asphyxia Core local server setup
- SoftEther VPN for cab-to-cab networking
- Arcade System Controllers (ASCs) and vendor information
- Arcade parts and hardware catalog
- Touch monitor polling rates
- Data mods and Omnimix installation
- Unity-based arcade game modding

---

## How to Use This Skill

### For AI Agents

1. **Retrieve the knowledge index** from [`skill/knowledge-index.md`](skill/knowledge-index.md) to find which source file to consult for a given question.
2. **Read the relevant source documentation** from the `docs/` directory.
3. **Synthesize an answer** based on the documentation, preserving step-by-step order and any warnings.
4. **Cite sources** using the pattern: `Source: two-torial.xyz/<path>` or `docs/<path>.md` within this repo.

### Query Routing

Use the following heuristics to route queries to the correct source documents:

| Query Type | Primary Source |
|---|---|
| "How do I set up [game]?" | `docs/games/<game-dir>/setup.md` |
| "I'm getting error [code]" | `docs/errorcodes/bemani.md` or `docs/errorcodes/sega.md` |
| "Game is crashing / won't start" | `docs/games/<game-dir>/troubleshooting.md` or `problems.md` |
| "How do I configure a controller?" | `docs/games/<game-dir>/controllers.md` |
| "How do I patch [game]?" | `docs/extras/patchsp2x.md`, `docs/extras/patchweb.md`, or `docs/extras/hexguide.md` |
| "How do I set up audio?" | `docs/extras/audio.md` or `docs/extras/streamaudio.md` |
| "How do I connect two cabinets?" | `docs/games/<game-dir>/c2c.md` or `docs/extras/softether.md` |
| "How do I install data mods?" | `docs/extras/datamods.md` |
| "What hardware do I need?" | `docs/extras/ascs.md`, `docs/extras/parts.md`, or `docs/extras/pollingrates.md` |
| "How do I set up a local server?" | `docs/extras/asphyxia.md` |

### Response Format Guidelines

When answering with content from this skill:

1. **Start with prerequisites** — mention any requirements upfront (OS version, audio settings, tools needed).
2. **Follow the documented step order** — the guides are designed to be sequential; do not reorder steps.
3. **Include warnings verbatim** — `!!! warning` and `!!! danger` blocks in source docs contain critical cautions that should always be surfaced.
4. **Distinguish game versions** — many settings differ between game versions; always confirm which version the user has.
5. **Recommend backups** — the site recommends making backups before manipulating game files; include this reminder.
6. **Link to source** — when possible, direct users to the full guide for their specific version.

---

## Example Interactions

See [`skill/example-prompts.md`](skill/example-prompts.md) for a collection of example user queries and the expected agent response pattern.

---

## Limitations

- This skill covers **setup and configuration** of existing game data only. It does **not** help obtain, distribute, or circumvent copy protection for game data.
- Guides reflect community knowledge and **may not cover all edge cases** or the latest game patches.
- Some game versions are experimental or unlisted (CHUSAN, MU3) and may have incomplete documentation.
- Images and screenshots referenced in the docs are not available in plain-text skill consumption — agents should direct users to the website ([two-torial.xyz](https://two-torial.xyz/)) for visual guides.
- Hardware requirements and compatibility depend on the user's specific PC configuration; the skill provides general guidance only.

---

## Source & License

All knowledge in this skill is derived from the TWO-TORIAL repository.  
Licensed under the [Apache License 2.0](LICENSE).  
Maintained by the TWO-TORIAL community — contributions welcome at [github.com/two-torial/two-torial](https://github.com/two-torial/two-torial).
