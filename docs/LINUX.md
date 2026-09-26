# Future RO on Linux

## Install

1. Unpack the download: `tar xzf FutureRO-*-linux.tar.gz` (or right-click -> Extract).
2. Open the new folder and run `./install.sh` (or double-click it and choose *Run*).
   Install into another folder than the unpacked download.
3. Answer its questions:
   - **Folder**: press Enter for `~/FutureRO`, or type another folder or drive.
   - **Missing programs**: it shows the command it would run (Wine, Docker) and asks first.
   - **Your Ragnarok client**: Future RO goes on top of WARPGATE's "WARP0716 Full Client
     2025-07-16" (free, 3.8 GB). No client yet? Choose **1** and the installer opens WARPGATE
     for you; already have it? Choose **2** and type its folder. Step by step:
     https://github.com/silkhelp-wq/Future-RO-Client/blob/main/docs/GET-THE-CLIENT.md
   - **Main server address**: the address of the Future RO main server, handed out in the
     Future RO Discord (https://discord.gg/gSwM9t8Dcx). Press Enter to add it later (`futurero address`).
   - **Solo server**: say yes to play on your own PC too. It needs Docker (or Podman).
   - **Your solo account**: the name and password you log in with on the solo server.
4. Start **Future RO** (main server) or **Future RO solo** from your applications menu, or
   run `futurero play` / `futurero solo` in a terminal.

The unpacked download folder can be deleted after installing.

## Playing solo

**Future RO solo** starts your own server (about 30 seconds; a notification says when it is
ready), then the game, already pointed at your own server - just log in. When you close the
game the server saves and stops, so nothing keeps running.

- `futurero server status` / `futurero server logs`: is it running, and what it says.
- `futurero account NAME PASSWORD` makes another account (`gm` at the end for a GM one). It
  starts the solo server for a moment if it is not running.
- Your solo characters live in the `server-data` folder of the install folder
  (`~/FutureRO/server-data` by default). Back up that folder to keep them.

## Playing on the main server

Needs Tailscale (see below). **Future RO** installs new patches first, then starts the game;
pick **Future RO** in the server list.

## Updates and problems

- `futurero play` / `futurero solo` install game-file updates first (from GitHub).
- `futurero solo` asks when a newer solo server is out (update now / later / skip this
  version) and keeps a copy of your characters first; `futurero server rollback` goes back.
  `futurero server update` checks now.
- `futurero report` sends us a problem report. It shows you everything in it first and asks.
  The launcher also offers one when something fails.
- `futurero check` says whether the client and the Future RO files are complete;
  `futurero warpgate` opens WARPGATE again (for example to **VERIFY** the client).

## Other

- `futurero setup`: resolution and graphics options.
- `futurero uninstall`: removes Future RO (asks before deleting solo characters). The
  WARPGATE client stays; delete its folder yourself if you don't need it.

