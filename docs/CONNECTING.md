# Connecting to the Future RO main server (Tailscale)

The main server is not on the open internet. It sits on a private network run by
Tailscale, a free program that links your PC to the server as if both were in the same
house. You set it up once; after that the game just connects.

You do **not** need any of this to play solo (on your own PC).

What you need from the host, both from the **Future RO Discord**
(https://discord.gg/gSwM9t8Dcx - ask there):

- **an invite link** (it looks like `https://login.tailscale.com/admin/invite/...`). Links
  expire after 30 days if nobody uses them.
- **the main server's address** (it looks like `100.x.x.x`). Future RO asks for it the first
  time you start **Future RO**; Start menu -> Future RO -> **Main server address** (Linux and
  macOS: `futurero address`) changes it later. Below it is written as `SERVER`.

## Step 1: Install Tailscale

Pick your system.

### Windows

1. Open https://tailscale.com/download/windows and click **Download Tailscale for Windows**.
2. Run the downloaded file and click through the installer (**Install**, then **Yes** when
   Windows asks for permission).
3. When it finishes, a Tailscale icon appears in the tray next to the clock (click the small
   **^** arrow if you can't see it).

### macOS

1. Open https://tailscale.com/download/mac and choose **Download from the App Store** (the
   easiest) or the standalone download.
2. Open Tailscale from Applications. macOS asks to **Allow** a VPN configuration: click
   **Allow** (and enter your Mac password if asked). Tailscale needs this to connect.
3. A Tailscale icon appears in the menu bar at the top of the screen.

### Linux

1. In a terminal: `curl -fsSL https://tailscale.com/install.sh | sh`
   (or install `tailscale` with your package manager, for example `sudo pacman -S tailscale`,
   then `sudo systemctl enable --now tailscaled`).
2. Run `sudo tailscale up`. It prints a web address: open it in your browser.

## Step 2: Sign in

1. Click the Tailscale icon (Linux: the address from step 1) and choose **Log in**.
2. Your browser opens. Sign in with **Google, Microsoft, Apple or GitHub** - whichever you
   already have. This makes your own free Tailscale account; nothing to pay, no card.
3. If asked, click **Connect** to add this PC to your account.
4. The icon now shows **Connected** (Linux: `tailscale status` lists your PC).

Remember which login you used (Google, Microsoft...). You need the same one in step 3.

## Step 3: Accept the invite

1. Open the invite link from the host in the **same browser** you just signed in with.
2. Check that the page shows the account you used in step 2 (top right). If it shows another
   one, sign out on that page and sign in with the right one.
3. Click **Accept invite**.
4. The Future RO server now appears in your Tailscale device list (it is shown as belonging
   to the host). You only get access to that one machine, and only to the game.

## Step 4: Check it works

Open this address in your browser:

    http://SERVER:8090/patch/plist.txt

(with the address from the Discord in place of `SERVER`)

- **A page with a few lines of text (or an empty white page)**: you're connected. Start the
  game.
- **"This site can't be reached" / it loads forever**: see below.

Now start Future RO (the normal **Future RO** icon, not "solo"), pick **Future RO** in the
server list and log in with the account the host gave you (or the one from the Discord
`/register` command, once that is open).

## When it doesn't work

Go down the list; most problems are the first two.

1. **Tailscale is not connected.** Click the icon. If it says *Logged out* or *Stopped*, click
   **Log in** / **Connect**. Tailscale does not always start by itself after a restart.
2. **Signed in with a different account than the one that accepted the invite.** Click the
   icon: your account's email is shown at the top. If it is not the one from step 3, choose
   **Log out** and log in with the right one (or accept the invite again with this account).
3. **The server is off.** The main server only runs while we are testing. Ask the host, or
   check Discord. Nothing to fix on your side.
4. **Another VPN is on** (work VPN, NordVPN, ...). Turn it off while playing; two VPNs often
   block each other.
5. **Your login expired.** Tailscale asks you to log in again every few months. Click the icon
   and log in.
6. **Check from Tailscale itself.** Windows: open *Command Prompt* and run
   `tailscale ping SERVER` (the address from the Discord). macOS/Linux: the same in *Terminal*. `pong` means the
   network is fine and the problem is the game or the server; `timed out` means Tailscale.
7. **School or work network.** Some networks block the direct connection; Tailscale then goes
   through a relay. It still works, only a bit slower. If nothing gets through at all, try
   another network (a phone hotspot is a quick test).
8. **Invite link says it's expired or used.** Ask the host for a new one.

The game itself says *"Failed to Connect to Server"* after you log in when any of the above
is the case. If step 4 works but the game still can't connect, tell the host: that is on our
side.

## Leaving

Click the Tailscale icon -> **Log out**, or uninstall Tailscale like any program. The host can
also remove your access at any time.

