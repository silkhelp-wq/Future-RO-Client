# Get the Ragnarok client with WARPGATE

Future RO runs on the **Ragnarok Online client from 16 July 2025**. We don't host that client
ourselves (it is 3.8 GB and not ours to share). A free program called **WARPGATE** downloads
it for you from its own mirrors and checks every piece as it arrives. Our download then adds
the Future RO files on top.

You do this **once**. Afterwards the Future RO patcher keeps everything up to date.

| | |
|---|---|
| What you download | "WARP0716 Full Client 2025-07-16" (WARPGATE calls it the **Full Client**, release 1.0.1) |
| Size | 3.80 GB, 5,443 files. Leave about 6 GB free on that drive. |
| Time | 5 to 30 minutes, depending on your internet |
| Cost | Free, no account needed |

**The short version (Windows):** download WARPGATE, open a *gate* (a folder) at `C:\FutureRO`,
install the **CLIENT** (tab 2), close WARPGATE, run `FutureRO-Setup`. Skip tabs 3, 4 and 5:
Future RO brings its own English translation and its own patched game program.

Pick your system:

- [Windows](#windows)
- [Linux](#linux)
- [macOS](#macos)
- [Something went wrong](#something-went-wrong)

---

## Windows

### 1. Download WARPGATE

1. Open **https://mirror2.romirrors.com/downloads/Warpgate.zip** in your browser. The download
   starts right away (about 5 MB).
2. Open your **Downloads** folder, right-click **Warpgate.zip** and choose **Extract All...**,
   then **Extract**.
3. In the new folder, double-click **Warpgate.exe**.
   - If Windows says **"Windows protected your PC"**, click **More info**, then **Run anyway**.
     WARPGATE has no code signature, so Windows warns about it the first time. This is normal.
   - If nothing appears for a while the first time, wait a minute. WARPGATE uses Microsoft Edge
     WebView2, which Windows 10 and 11 already have. If you see a message about WebView2
     missing, install it from https://developer.microsoft.com/microsoft-edge/webview2/
     ("Evergreen Bootstrapper"), then open WARPGATE again.

### 2. Open a gate (the folder the game goes into)

WARPGATE first shows **"Five steps to play"**. Its tabs run along the top: **1 GATE**,
**2 CLIENT**, **3 LANG**, **4 RAGEXE**, **5 WARP**. You only need tabs **1** and **2**.

![WARPGATE's welcome window with the five steps](img/warpgate-01-welcome.jpg)

1. Click **Open the gate hall**.
2. In the gate hall, click the big **+** (**Open a new gate**).

   ![The gate hall with "Open a new gate"](img/warpgate-02-gate-hall.jpg)

3. A folder window opens. Make a new folder **`C:\FutureRO`** and choose it:
   - Click **This PC** on the left, then **Local Disk (C:)**.
   - Click **New folder**, type `FutureRO`, press Enter.
   - Click the new **FutureRO** folder once, then **Select Folder**.

   Another drive works too (for example `D:\FutureRO`). **Remember the folder:** the Future
   RO setup asks for it later. Avoid `C:\Program Files`, where Windows blocks the game from
   saving its settings.

   Already have this exact client somewhere? Use **Add existing folder** under the **+**
   instead and pick that folder. WARPGATE checks it and only downloads what is missing.

The **GATE** tab at the top now shows your folder instead of "none yet".

### 3. Install the client (tab 2)

1. Click **2 CLIENT** at the top.
2. It shows **READY TO INSTALL · 3.80 GB · 5,443 files**. Check that the install folder is
   the one from step 2 (click **BROWSE...** to change it).
3. Click **INSTALL**.
4. Wait. The bar shows the progress (`data.grf` is the biggest file, 3.4 GB). You can use
   your PC meanwhile.
5. When it says the client is **installed / complete**, you're done with WARPGATE.

**Skip tabs 3 LANG, 4 RAGEXE and 5 WARP.** Future RO's own files include the English
translation and a patched game program made for our server. If you already ran those tabs,
that's fine: the Future RO setup puts its own versions over them.

### 4. Close WARPGATE, then install Future RO

1. Close WARPGATE (the **X** at the top right).
2. Download **FutureRO-Setup** from
   [the latest release](https://github.com/silkhelp-wq/Future-RO-Client/releases/latest) and
   run it.
3. On **Where is your Ragnarok client?**, choose the same folder (`C:\FutureRO`). The setup
   checks the client there before it installs anything.

4. On **Main server address**, type the address from the [Future RO Discord](https://discord.gg/gSwM9t8Dcx) (ask
   there), or leave it empty and add it later.

That's it. The **Future RO** icon on your desktop checks for updates and then starts the game.

Prefer to copy files yourself? Download `FutureRO-...-files.zip` instead and follow the
**READ ME FIRST** inside it: extract it into the same folder, then run **Set up Future RO**.

---

## Linux

WARPGATE is a Windows program, so it runs through **Wine**. The Future RO installer does all
of that for you: it sets up Wine, Microsoft's WebView2 (the part WARPGATE draws its window
with) and WARPGATE itself, then opens it.

1. Download `FutureRO-...-linux.tar.gz` from
   [the latest release](https://github.com/silkhelp-wq/Future-RO-Client/releases/latest) and
   unpack it (`tar xzf FutureRO-*-linux.tar.gz`).
2. In the new folder, run `./install.sh`.
3. At **3. Your Ragnarok client**, choose **1) Download it now with WARPGATE**.
   - The first time this downloads WebView2 from Microsoft (about 200 MB) and sets it up.
     That takes a few minutes.
   - The terminal shows the folder to use in WARPGATE, in Windows form, for example
     `Z:\home\you\FutureRO\game`. Keep the terminal open.
4. WARPGATE opens. Do [steps 2 and 3 of the Windows guide](#2-open-a-gate-the-folder-the-game-goes-into),
   but in the folder window type the folder the terminal showed you into the path box and
   press Enter.
   - The **Z:** drive is your Linux file system under Wine.
   - If the page stays black or empty for a minute, wait: the installer reloads it once by
     itself. Still empty? Close WARPGATE and choose option 1 again.
   - If the tabs along the top are hidden under the window's title bar, wait a few seconds:
     the installer moves the page down for you.
5. When the client is installed, close WARPGATE. The installer checks the client and carries on.

Already downloaded it (on this PC, or on a Windows PC and copied over)? Choose
**2) I already have it** and type its folder.

Later, `futurero warpgate` opens WARPGATE again, for example to repair the client with
**VERIFY**. `futurero check` tells you whether the client and the Future RO files are complete.

---

## macOS

**Not tested yet** (we have no Mac). WARPGATE is a Windows program, and its window needs
Microsoft's WebView2, which is unreliable under Wine on macOS.

The dependable way is to **download the client on a Windows PC** (or a Windows virtual
machine) with the [Windows steps 1 to 3](#windows), then copy the whole folder to your Mac:
over the network, or with a USB stick formatted as exFAT (data.grf is larger than FAT32
allows). Then run the macOS `install.sh`, choose **2) I already have it** and give it that
folder.

You can also try **1) Download it now with WARPGATE** in the macOS installer. It works the
same way as on Linux, but it may show an empty window.

---

## Something went wrong

**The Future RO setup says "not the one Future RO needs" or "data.grf is ... bytes".**
The download didn't finish, or the folder holds a different client. Open WARPGATE, make sure
the gate is that folder, and on the **CLIENT** tab press **VERIFY**. WARPGATE re-downloads only
what is missing or damaged. Then run the Future RO setup again.

**Windows or my antivirus removed a file.**
The game program has no code signature, so some antivirus programs quarantine it. Restore
it, add your game folder (`C:\FutureRO`) to the antivirus' exclusions, then press **VERIFY**
in WARPGATE and run the Future RO setup again.

**The download is very slow or stops.**
Close WARPGATE and open it again: it continues where it stopped and checks what it already
has. Pausing a VPN helps sometimes.

**I used WARPGATE's LANG or RAGEXE tab after installing Future RO.**
Those replace some Future RO files with WARPGATE's versions. Run the Future RO setup again
(Linux: `./install.sh`) to put ours back. Your settings and characters are not touched.

**The game says a .dll is missing, or closes right away.**
The Future RO setup installs Microsoft's runtimes the game needs (Visual C++ 2012 and
2015-2022, DirectX 9). If you used the files-only zip, run **Set up Future RO** in the game
folder. It does the same.

**Still stuck?** Start menu -> Future RO -> **Report a problem** (Linux: `futurero report`).
It shows you the whole report before sending anything. Or
[open an issue](https://github.com/silkhelp-wq/Future-RO-Client/issues/new) and describe
what you see.

---

*WARPGATE, WARP0716 and their mirrors are made by the WARP0716 community (LegacyGamers
Network), not by Future RO. Thank them on their Discord.*
