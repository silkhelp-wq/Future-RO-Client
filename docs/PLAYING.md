# Playing Future RO

What's different from other Ragnarok servers, the commands you can use, and where to find
things. The world's history is in [Episodes](EPISODES.md), the ready-made builds are in
[Preset builds](BUILDS.md).

## The idea in one minute

- **One world, one episode at a time.** Everyone plays the same slice of Ragnarok's history,
  starting with **Episode 1.0 (2002)**: eight towns, the first 13 classes, level 99. Then the
  world moves forward: Lutie, Comodo, War of Emperium, Juno and the 2-2 classes, rebirth,
  Renewal, third classes, fourth classes, up to today's kRO.
- **The rules of the time.** Level caps, classes, skills, monsters, maps and even balance
  follow the episode. At launch a failed refine resets the item to +0 instead of breaking it,
  and cards were stronger.
- **Open world within the episode.** Every map the episode has is open: the **World Warper**
  in Prontera, `@go` and `@warp` take you anywhere. No quest locks, no key items needed to
  travel.
- **Quick start, fair points.** The **Build Master** can set your character up with a tested
  build in one step. You never hold more stat or skill points than your levels give you.

## Your first minutes

0. For the main server you need its address and a Tailscale invite: ask in the
   [Future RO Discord](https://discord.gg/gSwM9t8Dcx), then see [Connecting](CONNECTING.md). Solo needs neither.
1. Make a character. You start at the **Prontera fountain**.
2. The **Build Master** greets you: pick a preset build for your class, build your own, or
   say no and play from level 1 the classic way. You can come back any time with `@build`.
3. Talk to the **World Warper** next to the fountain (or type `@go` plus a town name) to
   travel.
4. Type `@commands` to see every command your account may use.

## Commands

Type these in the chat box.

### Everyone

| Command | What it does |
|---|---|
| `@build` | The **Build Master**: preset builds, your own build, remove a build it gave you |
| `@go <town>` | Travel to a town, for example `@go geffen`, `@go 3` (plain `@go` lists them) |
| `@warp <map> [x y]` | Travel to any open map, for example `@warp pay_dun00` |
| `@jump [x y]` | Jump to a spot on the current map (random without coordinates) |
| `@where [name]` | Where you (or a player) are: map and coordinates |
| `@mapinfo` | Who is on this map, and its rules (PvP, no-teleport, ...) |
| `@db` | The **Archivist**: search items, monsters, drops, spawns and skills of this episode |
| `@calc` | The **Stat Scholar**: your real stats, what-if stat plans, your chances against a monster |
| `@woe` | **Queue War of Emperium** (from Episode 4.0): guild masters sign their guild up; see below |
| `@bug` | Report a bug from where you stand: it saves the map and spot, you add a note |
| `@changedress` | Take off costume looks (mounts, wedding dress, ...) |
| `@commands` | List every command your account may use |

`@go` and `@warp` refuse maps the episode doesn't have yet.

### Game masters (and you, on your own solo server)

Your solo account is a game master if you ticked **Make it a GM account** at install.

| Command | What it does |
|---|---|
| `@episode` | Show the current episode and **switch the world** to another one. The world restarts on it in about 30 seconds. On your solo server you can visit any era this way. |
| `@warper` | The World Warper menu from anywhere, including **Memorial dungeons** |
| all of rAthena's GM commands | `@item`, `@monster`, `@lvup`, `@jobchange`, ... (`@commands` lists them) |

Going back in time with `@episode` is safe: levels above the episode's cap and classes from
later episodes are kept and come back when the world moves forward again (see
[Episodes](EPISODES.md#what-happens-to-your-character-when-the-episode-changes)).

## NPCs worth knowing (Prontera)

| NPC | Where | What for |
|---|---|---|
| **Build Master** | by the fountain | preset builds, custom builds, fame rankings (Taekwon, smiths, alchemists) |
| **World Warper** | by the fountain | every open map by category or name search; **Memorial dungeons** with party checks and the prep steps done for you |
| **WoE Registrar** | Prontera | Queue War of Emperium sign-up (same as `@woe`) |
| **QWoE Quartermaster** | Prontera | trade WoE coins for rewards |

## Memorial dungeons

The World Warper's **Memorial dungeons** menu lists the instance dungeons of the current
episode (Endless Tower, Old Glast Heim, ...). The party leader picks one. The warper checks
the party size, levels, days and cooldowns, does the prep steps the official quest would want
(flags, quest items) for every member, and sends the party to the entrance NPC.

## Queue War of Emperium (from Episode 4.0)

Instead of a weekly schedule, WoE runs all the time in short matches. Guild masters queue with
`@woe` (or at the WoE Registrar) in one of three brackets:

1. **Solo guild**: 2 to 6 guilds, king of the hill. Whoever holds the Emperium longest wins.
2. **Guild vs guild**: two rounds, attack and defend, sides swap. The faster break wins.
3. **Alliance vs alliance**: like 2, each side is a guild plus its allies.

Matches pay **WoE coins** (win, lose or draw, with a daily cap) for the Quartermaster.

## Levels, points and Renewal

- **Caps follow the episode.** Launch: base 99, job 50 (Novice 10). Rebirth (9.0): transcendent
  job 70. Renewal third classes (13.2b): 150, later 160, 175, 185, 200; fourth classes
  (17.2b): 250, then 260 and 275. [The full table](EPISODES.md#all-episodes).
- **Points always match your levels.** On every map change the server makes sure your free
  stat, trait and skill points are exactly what your levels allow minus what you spent.
- **Pre-renewal and Renewal** are different games under the hood. Episodes 1.0 to 13.2 run the
  pre-renewal rules, 13.2b onwards Renewal. When the world crosses that line, **your stats and
  skills are reset once** on your next login. Spend them again, or use `@build`.

## Bugs and problems

- **In the game:** `@bug` where it happens. Staff see the map and spot, and you can add
  screenshots on the Future RO website.
- **With the game itself** (it won't start, an update failed, the solo server won't start):
  Start menu -> Future RO -> **Report a problem** (Linux/macOS: `futurero report`).
  See [Updates and problem reports](UPDATES-AND-REPORTS.md).
