# Example Prompts & Response Patterns

This file provides example user queries and the expected agent response pattern using the TWO-TORIAL arcade skill. These are intended to help AI agent authors validate correct skill usage.

---

## Setup Questions

### "How do I set up IIDX 31 EPOLIS?"

**Source:** `docs/games/iidx31/setup.md`

**Expected response pattern:**
- Mention that SpiceTools / Spice2x is required as a launcher
- Recommend setting Windows audio to 44100 Hz before starting
- Describe the game data folder structure (e.g., `contents/` directory)
- Explain how to configure `spicecfg.exe` (or `spice2x`) with the correct DLL
- Note the option to use a local server (Asphyxia Core) or eAmuse network
- Warn about read-only file attributes on extracted game data
- Link to full guide: `https://two-torial.xyz/games/iidx31/setup/`

---

### "How do I get CHUNITHM VERSE running?"

**Source:** `docs/games/chunithmverse/setup.md`

**Expected response pattern:**
- List prerequisites (Windows 10/11, required runtime libraries)
- Explain segatools configuration (`segatools.ini`)
- Mention setting up `amdaemon` and device emulation settings
- Describe the CHUNITHM-specific slider and air sensor controller options
- Note that a local server (ARTEMiS or Aqua) is optional but recommended
- Warn about drive letter restrictions for game data (not `E:\` or `Y:\`)
- Link to full guide: `https://two-torial.xyz/games/chunithmverse/setup/`

---

### "How do I set up maimai DX BUDDiES?"

**Source:** `docs/games/maimaidx/buddies/setup.md`

**Expected response pattern:**
- Cover segatools / ALL.Net P-ras MULTI emulation setup
- Explain the dual-monitor / dual-touch screen configuration
- Reference the controllers guide for touch screen polling rates
- Mention ALLS hardware emulation for the ring controller
- Link to full guide: `https://two-torial.xyz/games/maimaidx/buddies/setup/`

---

## Troubleshooting & Error Codes

### "I'm getting BEMANI error 5-2900-0003, what does it mean?"

**Source:** `docs/errorcodes/bemani.md`

**Expected response pattern:**
- Look up error code `5-2900-0003` in the BEMANI error codes file
- State the error name and cause
- Give the recommended resolution steps
- Recommend verifying game data integrity if cause is unclear
- Link to full error code list: `https://two-torial.xyz/errorcodes/bemani/`

---

### "SDVX EXCEED GEAR crashes on startup — how do I fix it?"

**Source:** `docs/games/sdvx6/troubleshooting.md`, `docs/extras/audio.md`

**Expected response pattern:**
- Start with the most common cause: audio configuration (wrong sample rate)
  - Recommend 44100 Hz in Windows audio settings
- Check that SpiceTools / Spice2x is up-to-date
- Verify the correct DLL (`soundvoltex.dll`) is specified
- Mention checking that game data is not read-only
- Suggest running as administrator
- Link to troubleshooting guide: `https://two-torial.xyz/games/sdvx6/troubleshooting/`

---

### "Why is my CHUNITHM SUN not detecting my controller/slider?"

**Source:** `docs/games/chunithmsun/controllers.md`

**Expected response pattern:**
- Explain the different controller options (real slider, keyboard, gamepad)
- Describe how to configure the controller in `segatools.ini`
- Mention the IO4 emulation settings for slider input
- Reference polling rate requirements for USB sliders
- Link to controllers guide: `https://two-torial.xyz/games/chunithmsun/controllers/`

---

## Patching

### "How do I patch IIDX 32 using Spice2x?"

**Source:** `docs/extras/patchsp2x.md`

**Expected response pattern:**
- Explain that Spice2x has a built-in patcher in `spicecfg.exe` under the "Patches" tab
- Describe how to fetch patches from a patch server URL
- Note which commonly used patches exist (e.g., force offline, skip tutorials, unlock songs)
- Warn that patches may break on game updates and need to be reapplied
- Link to: `https://two-torial.xyz/extras/patchsp2x/`

---

### "How do I manually hex patch an arcade game?"

**Source:** `docs/extras/hexguide.md`

**Expected response pattern:**
- Explain what hex patching is (editing binary offsets in game DLLs/EXEs)
- Recommend using a hex editor like HxD or ImHex
- Describe how to find the correct file and offset from a patch database
- Warn that this is error-prone and to make a backup first
- Link to: `https://two-torial.xyz/extras/hexguide/`

---

## Audio

### "How do I set up ASIO audio for arcade games?"

**Source:** `docs/extras/audio.md`

**Expected response pattern:**
- Explain ASIO vs WASAPI and when each is preferable
- Describe how to configure the ASIO driver (e.g., ASIO4ALL or manufacturer driver)
- Show how to point the game's audio config to the ASIO device
- Mention the required sample rate (44100 Hz for most BEMANI games)
- Link to: `https://two-torial.xyz/extras/audio/`

---

### "My audio is cutting out or another app is taking over the audio device"

**Source:** `docs/extras/streamaudio.md`

**Expected response pattern:**
- Explain exclusive audio mode and why it blocks other apps
- Describe how to set Windows audio to shared mode
- Cover SpiceTools workarounds for exclusive WASAPI
- Link to: `https://two-torial.xyz/extras/streamaudio/`

---

## Networking

### "How do I connect two CHUNITHM cabinets for cab-to-cab play?"

**Source:** `docs/games/chunithmverse/c2c.md`, `docs/extras/softether.md`

**Expected response pattern:**
- Explain that cab-to-cab requires both machines on the same network segment
- Describe the SoftEther VPN setup for linking machines over the internet
- Cover the specific `segatools.ini` settings for enabling cab-to-cab mode
- Note that both machines must be on the same game version
- Link to game-specific c2c guide: `https://two-torial.xyz/games/chunithmverse/c2c/`

---

### "How do I set up a local e-amusement server?"

**Source:** `docs/extras/asphyxia.md`

**Expected response pattern:**
- Explain that Asphyxia Core is the commonly used local server for BEMANI games
- Describe installation (Node.js dependency, running `asphyxia start`)
- Explain how to point SpiceTools at the local server using `-ea` flag or `prop/ea3-config.xml`
- Note that Asphyxia saves scores, cards, and settings locally
- Warn that it is for offline/local use only, not for connecting to official networks
- Link to: `https://two-torial.xyz/extras/asphyxia/`

---

## Hardware

### "What arcade controller do I need for O.N.G.E.K.I.?"

**Source:** `docs/games/ongekibrightmemory/controllers.md`, `docs/extras/ascs.md`

**Expected response pattern:**
- Describe the O.N.G.E.K.I. original controller (lever + buttons + side buttons)
- List compatible third-party ASCs or DIY alternatives
- Reference polling rate requirements for the lever
- Link to controllers guide: `https://two-torial.xyz/games/ongekibrightmemory/controllers/`

---

### "What touch monitors work well for maimai DX?"

**Source:** `docs/extras/pollingrates.md`

**Expected response pattern:**
- Explain that touch monitors must support at least 4-point multi-touch
- Describe the polling rate requirement (typically 8ms or 125 Hz)
- List known-compatible monitor models from the community
- Warn about monitors with poor USB polling that cause touch lag
- Link to: `https://two-torial.xyz/extras/pollingrates/`

---

## Data Mods

### "How do I install Omnimix for IIDX?"

**Source:** `docs/extras/datamods.md`

**Expected response pattern:**
- Define Omnimix (a data mod that unlocks all songs/charts in a game)
- Describe the installation process (extracting files into the game data directory)
- Warn that Omnimix replaces game data files — always back up first
- Note that Omnimix may not be compatible with all game versions
- Link to: `https://two-torial.xyz/extras/datamods/`

---

## Response Guardrails

AI agents using this skill **must not**:
- Provide links to, or instructions for obtaining, copyrighted game data
- Help users circumvent software copy protection mechanisms
- Claim authoritative knowledge about game versions not documented in this repository

AI agents **should always**:
- Recommend backing up game files before making changes
- Specify which game version a guide applies to
- Distinguish between official online play and offline/local server setups
- Direct users to the TWO-TORIAL Discord (`https://discord.gg/cZRUmEPK78`) for direct support when the skill cannot resolve an issue
