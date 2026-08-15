English | [简体中文](./README.zh.md)

<div align="center">
  <h1>MystikIM-ServerKit-V3.1</h1>
  <p><b>Unofficial</b> compatibility fork, updated to run on 7 Days to Die game version <b>V3.1</b> ("Dead Hot Summer" and later).<br/>
  Not affiliated with or endorsed by the original developers.</p>
</div>

[![license](https://img.shields.io/github/license/1249993110/7DaysToDie-ServerKit?style=flat-square)](https://en.wikipedia.org/wiki/MIT_License)

## What this is

This is a fork of [**Shisanlin's Pro3.2 (TianYiServerKit)**](https://github.com/1249993110/7DaysToDie-ServerKit) build, which is itself a fork of [**IceCoffee1024's original 7DaysToDie-ServerKit**](https://github.com/1249993110/7DaysToDie-ServerKit) — a RESTful API and web management panel mod for 7 Days to Die dedicated servers.

The game's V3.0 "Dead Hot Summer" update fundamentally reworked the modding API (new XUi system, `entitygroups.xml` format, localization moved to `.csv`, block addressing changed, and more), which broke every ServerKit release that predates it. **All the credit for the mod itself — its design, features, and the huge majority of the code — belongs to IceCoffee1024 and Shisanlin.** My contribution here is limited to the compatibility work needed to get Pro3.2 building and running again against the current game version, listed in [`CHANGELOG.md`](./CHANGELOG.md).

This exists as a stopgap so server owners aren't stuck on a broken build while the original developers work on their own official update. **Once an official V3.1-compatible release ships upstream, switch to that instead.**

## 🌐 Compatibility
Dedicated Server only. Required game version: **V3.1+** (not compatible with pre-V3.0 game versions — use the [original project](https://github.com/1249993110/7DaysToDie-ServerKit) for those).

## 📌 Getting started

### 1. Download
Get the latest release [here](../../releases) — it's a complete, ready-to-run mod folder, no build step needed.

### 2. Install
Extract the downloaded `.zip` into your `7 Days to Die Dedicated Server/Mods` folder. You should also have `0_TFP_Harmony` present (ships with the game itself as of V3.0 — `MapRendering`/`WebServer` companion mods are **not** needed anymore, that functionality is native to the game now).

### 3. Start the server
- Wait for the server process to start completely.
- Open a browser to `http://<your-server-ip>:8888`
- Default username: `admin` / Default password: `123456` — **change this immediately.**

### 🚀 Configuration
Login credentials and other panel settings are in `Mods/SdtdServerKit/Config/appsettings.json`. Restart the server after editing.

## 🛠️ Building from source
The C# project references a handful of the game's own compiled assemblies (`Assembly-CSharp.dll` and similar) to build against — these are **not included in this repository**, since they're the game developer's copyrighted code, not ours or IceCoffee1024's to redistribute. Copy them yourself from your own legally-owned game install (`<game install>/7DaysToDie_Data/Managed/`) into `src/7dtd-binaries/` before building. See [`CHANGELOG.md`](./CHANGELOG.md) for the exact list of files and the fixes applied for each game API change.

## 🌱 Changelog
V3.1 compatibility fixes are documented in [`CHANGELOG.md`](./CHANGELOG.md). For everything else — the full feature set, commands, and API docs — see the [original project's README](https://github.com/1249993110/7DaysToDie-ServerKit#readme), which this fork otherwise carries forward unchanged.

## 🙏 Credits
- [**IceCoffee1024**](https://github.com/1249993110) — original author and maintainer of 7DaysToDie-ServerKit.
- [**Shisanlin**](https://github.com/Shisanlin) — author of the Pro3.2 (TianYiServerKit) fork this is based on (lottery, level gifts, zone management, and more).
- Everyone else credited in the original project's contributor list.

## 📄 License
MIT — see [`LICENSE`](./LICENSE). The original copyright notice is unmodified; this fork does not claim authorship of the underlying project.

## 📄 Disclaimer
The source code of this project is open and transparent. Any disputes arising from or related to the use of this software should be resolved through friendly negotiation.
Any private modifications to the code of this project are the sole responsibility of the person who made these modifications. Neither this fork's maintainer nor the original author team assumes any responsibility for any form of loss or damage that may be caused to the user or others during the use of this software.
If you download, install, and use this software, that means you accept the above.
