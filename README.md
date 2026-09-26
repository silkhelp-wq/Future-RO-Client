<p align="center"><img src="docs/img/banner.jpg" alt="Future RO" width="776"></p>

<h1 align="center">Future RO</h1>

<p align="center"><b>Ragnarok Online, one episode at a time.</b><br>
Start in 2002 with eight towns and the first thirteen classes, and live through the game's
history, from Lutie and Juno to Renewal and the fourth classes.</p>

<p align="center">
<a href="https://github.com/silkhelp-wq/Future-RO-Client/releases/latest"><b>Download</b></a> ·
<a href="docs/GET-THE-CLIENT.md">Get the client</a> ·
<a href="docs/PLAYING.md">How to play</a> ·
<a href="docs/EPISODES.md">Episodes</a> ·
<a href="docs/BUILDS.md">Builds</a> ·
<a href="https://github.com/silkhelp-wq/Future-RO-Client/issues">Report a problem</a> ·
<a href="https://discord.gg/gSwM9t8Dcx">Discord</a>
</p>

---

## What makes it different

- **One world that travels through time.** Every player is in the same episode. When the world
  moves on, what kRO released then opens up: towns, dungeons, monsters, classes, skills, level
  caps, and the rules of that time.
- **Open world within the episode.** The World Warper, `@go` and `@warp` reach every map the
  episode has. No quest locks on travel.
- **Ready in a minute.** The Build Master sets your character up with a tested build for your
  class, or lets you build your own. Stat and skill points always match your levels.
- **Your own server if you like.** *Future RO solo* runs the whole world on your PC. As a GM
  there, `@episode` takes you to any era.

## Install in three steps

**1. Get the Ragnarok client with WARPGATE.** Free, 3.8 GB, about 15 minutes. We don't host the
client itself, only our files on top of it.
Step by step, with pictures: **[Get the client](docs/GET-THE-CLIENT.md)**

**2. Download Future RO** from the **[latest release](https://github.com/silkhelp-wq/Future-RO-Client/releases/latest)**:

| Your computer | Download | Then |
|---|---|---|
| **Windows 10 / 11** | `FutureRO-Setup-<version>.exe` | Run it and pick your WARPGATE folder. [Windows guide](docs/WINDOWS.md) |
| Windows, by hand | `FutureRO-<version>-files.zip` | Extract into your WARPGATE folder, run **Set up Future RO** |
| **Linux** | `FutureRO-<version>-linux.tar.gz` | Unpack, run `./install.sh`. It can open WARPGATE for you. [Linux guide](docs/LINUX.md) |
| macOS *(untested)* | `FutureRO-<version>-macos.tar.gz` | Unpack, run `./install.sh`. [macOS guide](docs/MACOS.md) |

**3. Play.** The **Future RO** icon checks for updates, then starts the game. **Future RO solo**
starts your own server first (needs [Docker Desktop](https://www.docker.com/products/docker-desktop/), free).
The main server needs a one-time [Tailscale setup](docs/CONNECTING.md) and its **address**:
**ask for it in the [Future RO Discord](https://discord.gg/gSwM9t8Dcx)** (the setup and the first start ask you for it).

> Already have the 2025-07-16 client from WARPGATE? Skip step 1. The setup checks your
> folder and only adds what Future RO needs (about 150 MB).

## A short history of the world

| Episode | Year | What opens up |
|---|---|---|
| **1.0** Start of the Adventure | 2002 | Prontera, Geffen, Payon, Morroc, Alberta, Aldebaran, Izlude · 1st and 2-1 classes · level 99 / job 50 |
| 2.0 – 4.0 | 2002–03 | Lutie, Comodo, War of Emperium and Turtle Island |
| **5.0** Juno | 2003 | Juno, Magma Dungeon · the 2-2 classes (Crusader, Monk, Sage, Rogue, Alchemist, Bard, Dancer) |
| 6.0 – 8.0 | 2003–04 | Amatsu, Gonryun, Louyang, Ayothaya, Umbala, Niflheim · Super Novice |
| **9.0** Rebirth | 2004 | Transcendent classes, job 70 · Baby classes |
| 10.1 – 13.2 | 2005–08 | Einbroch, Lighthalzen, Hugel, Rachel, Veins, Moscovia, Satan Morroc · Taekwon, Ninja, Gunslinger |
| **13.2b** Renewal | 2009 | New rules and formulas · third classes · level 150 |
| 13.3 – 16.2 | 2009–18 | El Dicastes, Mora, Dewata, Malangdo, Eclage, Lasagna · Kagerou, Oboro, Rebellion, Summoner · level 175 |
| **17.2b** Fourth classes | 2020 | Fourth classes and trait stats · level 250 |
| 18 – Chapter 2 | 2021–26 | Expanded fourth classes · level 275 |

Every episode in detail, with its towns, dungeons, classes, caps and rules:
**[Episodes](docs/EPISODES.md)**.

## Commands at a glance

| | |
|---|---|
| `@build` | Build Master: preset builds, your own build ([all presets](docs/BUILDS.md)) |
| `@go <town>` / `@warp <map>` | Travel anywhere the episode has |
| `@db` | Search items, monsters, drops and spawns of this episode |
| `@calc` | Your real stats, stat plans, chances against a monster |
| `@woe` | Queue War of Emperium for your guild (from Episode 4.0) |
| `@bug` | Report a bug right where it happens |
| `@episode` | *(GM, and on your solo server)* switch the world to another episode |

The full list, NPCs, memorial dungeons and WoE: **[How to play](docs/PLAYING.md)**.

## Updates

You never download Future RO again for an update:

- **Game files** update themselves: the **Future RO** icon checks every time you start it
  (from GitHub, no Tailscale needed).
- **Your solo server** asks when a newer one is out: **Update now**, **Later** or **Skip this
  version**. Your characters are copied first, and **Undo the last solo server update** puts
  everything back.
- **The main server** is updated by us.

## When something breaks

Future RO offers a **problem report** when an update or the solo server fails. You can send
one any time too: Start menu → Future RO → **Report a problem** (Linux/macOS: `futurero
report`). It **shows you the whole report first**: versions, your system, the logs. No
passwords; your user name and PC name are taken out. Nothing is sent unless you click **Send
report**. Reports become [issues here](https://github.com/silkhelp-wq/Future-RO-Client/issues).
Details: [Updates and problem reports](docs/UPDATES-AND-REPORTS.md).

## All guides

| Guide | For |
|---|---|
| [Get the client](docs/GET-THE-CLIENT.md) | Downloading the Ragnarok client with WARPGATE (Windows, Linux, macOS) |
| [Windows](docs/WINDOWS.md) · [Linux](docs/LINUX.md) · [macOS](docs/MACOS.md) | Installing Future RO, the solo server, settings, uninstalling |
| [Connecting to the main server](docs/CONNECTING.md) | The one-time Tailscale setup, and what to do when it won't connect |
| [How to play](docs/PLAYING.md) | Commands, NPCs, memorial dungeons, Queue WoE, levels and points |
| [Episodes](docs/EPISODES.md) | Every episode: towns, dungeons, classes, caps and the rules of the time |
| [Preset builds](docs/BUILDS.md) | Every Build Master preset, and the episodes it is offered in |
| [Updates and problem reports](docs/UPDATES-AND-REPORTS.md) | How updates work, undoing a solo update, what a report contains |

---

<sub>This repository holds the player downloads: the Future RO client files (translation,
settings, a patched 2025-07-16 game program), the setup and launcher scripts, the patcher and
the solo server image. The server code is kept separately. The client itself comes from
WARPGATE by the WARP0716 community. Ragnarok Online is a trademark of Gravity Co., Ltd.;
Future RO is a fan project, not affiliated with Gravity.</sub>
