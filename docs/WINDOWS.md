# Future RO on Windows

## Install

Future RO goes on top of the **Ragnarok client from WARPGATE** ("WARP0716 Full Client
2025-07-16", free, 3.8 GB). Get that first - step by step: https://github.com/silkhelp-wq/Future-RO-Client/blob/main/docs/GET-THE-CLIENT.md
(short version: in WARPGATE open a gate at `C:\FutureRO`, install tab **2 CLIENT**, skip
tabs 3-5, close WARPGATE).

1. Download `FutureRO-Setup-<version>.exe` and double-click it.
   - If Windows says *"Windows protected your PC"*, click **More info**, then
     **Run anyway** (the setup isn't code-signed yet).
   - Click **Yes** when Windows asks for permission (this happens once, to
     install Microsoft's Visual C++ and DirectX runtimes if you don't have them).
2. Keep clicking **Next**.
3. On **Where is your Ragnarok client?**, pick the folder WARPGATE downloaded into (the one
   with `data.grf`; `C:\FutureRO` if you followed the guide). The setup checks the client
   there. If it is missing or incomplete it tells you what is wrong and how to fix it
   (usually: WARPGATE -> CLIENT tab -> **VERIFY**).
4. On **Main server address**, type the address of the Future RO main server. It is handed
   out in the Future RO Discord (https://discord.gg/gSwM9t8Dcx): ask there. You can leave it empty and add it later
   (the first start of **Future RO** asks for it; Start menu -> Future RO -> **Main server
   address** changes it). Playing solo needs no address.
5. On **Your solo account**, type the name and password you want for your own
   server on this PC (see *Playing solo* below). If you don't want a solo
   server, untick it on the components page instead.
6. Click **Finish**. Double-click **Future RO** on your desktop to play on the
   main server, or **Future RO solo** to play on your own.

Future RO adds about 150 MB to the client folder. The setup never changes or deletes the
client's own files (`data.grf` and the rest).

**Files only:** instead of the setup, `FutureRO-<version>-files.zip` can be extracted straight
into the client folder; then double-click **Set up Future RO** in that folder (it installs the
runtimes, asks for the main server's address and makes the icons). That way has no solo server.

## Playing solo (your own server)

**Future RO solo** starts a complete Future RO server on your own PC - no
internet, no Tailscale - then the game. A black window shows what the server is
doing; the first start takes about two minutes (later ones about half a
minute). The game then opens straight onto your own server - log in with the
account you chose during install.
When you close the game, the server saves and stops - nothing keeps running.
Leave the black window open while you play: it is what stops the server. If it
gets closed anyway (or the PC crashes), nothing breaks - the next start of
**Future RO** or **Future RO solo** puts everything right again.

If setting up the solo server fails during install (for example because Docker
Desktop wasn't running), just open **Future RO solo** later: it finishes the
setup and creates your account then.

Another solo account (or the first one, after a silent install, which skips the
account page): open PowerShell and run, with your install folder,

    powershell -ExecutionPolicy Bypass -File "C:\FutureRO\solo.ps1" -Mode account -User NAME -Pass PASSWORD

(add `-Gm` for a game-master account).

The solo server runs inside **Docker Desktop** (free,
https://docs.docker.com/desktop/setup/install/windows-install/). The installer
tells you if it's missing; you can install it before or after Future RO. On
most PCs Docker Desktop asks to turn on "WSL 2" the first time and wants one
restart - say yes, restart, done.

Your solo world starts at **Episode 1**, the very first Ragnarok (2002), and a
game master can move it through history with `@episode`. Your solo account is
a GM if you ticked that during install.

## "Checking your computer" said something

- **Graphics: basic display driver** - Windows doesn't have your graphics
  card's driver yet. Click the driver button on that page (NVIDIA, AMD or
  Intel), install it, restart, and run the setup again.
- **Memory under 4 GB** - the game may still run; close other programs first.
- **Future RO server not reachable** - see *Connecting* below. You can still
  install; the check only tells you the game won't log in yet.

## Connecting

Future RO's main server is on a private network (Tailscale). Your PC joins it once; the
full steps, and what to do when it doesn't connect, are in **Connecting to the Future RO
main server** below.

Until you're on the network the game starts, but says *"Failed to Connect to Server"* after
login.

With the solo server installed, the **Future RO** icon runs a small hidden
PowerShell script first (it undoes what an interrupted solo session left
behind). If that icon does nothing - some security software or company
policies block PowerShell scripts - start `Future RO Patcher.exe` in the
install folder directly; it is the same game and updater.

## Updates and problems

- The **Future RO** icon installs game-file updates every time (from GitHub; no Tailscale
  needed for that).
- **Future RO solo** asks when a newer solo server is out (**Update now / Later / Skip this
  version**) and keeps a copy of your characters first. Start menu -> Future RO -> **Undo the
  last solo server update** goes back.
- Start menu -> Future RO -> **Report a problem** sends us a report. It shows you everything
  in it first and asks.

## Settings and uninstalling

- Start menu -> **Future RO graphics settings** changes resolution and
  graphics options.
- Settings -> Apps -> **Future RO** -> Uninstall removes the Future RO files. It asks
  whether to delete your solo server too (characters and accounts on this PC);
  for that, Docker Desktop has to be running - it tells you if it isn't.
  The WARPGATE client stays in its folder; delete that folder yourself if you don't need it.
