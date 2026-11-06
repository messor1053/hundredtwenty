<p align="center">
  <img src="icon.png" width="112" alt="Hundred Twenty icon" />
</p>

<h1 align="center">Hundred Twenty</h1>
<p align="center"><b>120fps exports for TikTok, in one click.</b></p>

<p align="center">
  <a href="../../releases/latest"><b>Download for Windows</b></a>
</p>

<p align="center">
  <img src="screenshots/2-loaded.png" width="820" alt="Hundred Twenty with a video loaded" />
</p>

Hundred Twenty takes any edit, encodes it at a true 120fps with FFmpeg and preps it for TikTok's 120fps upload method. You don't touch the command line, patch anything by hand or guess settings.

## Features

- **Drop and export.** Drag in an MP4, MOV, MKV or WEBM, then hit Export.
- **Patch method (temporary).** TikTok changed how it processes uploads on November 3 and the old 120fps methods stopped working. Patch exports at 120fps, then stretches the file's timing so TikTok keeps every frame. The file plays slowed on PC, that is expected. It's temporary until we have a fix.
- **Studio (maintenance).** The original 120 Studio method is grayed out until it works on TikTok again.
- **Tuned settings.** 1080×1920 H.264 at about 12 Mbps with AAC audio. A bitrate slider is there if you want more.
- **2K and 4K.** Keep a source bigger than 1080p sharper: **2K** (1440p, about 22 Mbps) or **4K** (2160p, marked Risky). 1080p stays the default.
- **Output summary.** See the frame size, bitrate, encoder and an estimated file size before you export.
- **Motion interpolation.** Builds real in-between frames for clips under 120fps.
- **One-click TikTok.** Opens TikTok Studio in your browser with the caption already copied.
- **Automatic updates.** New versions download in the background and install on restart. No more redownloading.

## Design

Make it yours. Pick a layout: **Classic**, **Steps** (one step at a time), **Pro** (sidebar, inspector and status bar) or **Bento** (every control its own tile). Pick a style: **Clean**, **Glass**, **Terminal** or **Neon**. Then a theme (Midnight, Graphite, Aurora or Light) and one of nine accent colours. Every card tilts in 3D toward your cursor with glare and depth. Spring animations, a live 9:16 preview, a progress ring, sound on every click, and five cursor themes.

<p align="center">
  <img src="screenshots/3-exporting.png" width="49%" alt="Exporting" />
  <img src="screenshots/4-done.png" width="49%" alt="Ready for TikTok" />
</p>
<p align="center">
  <img src="screenshots/5-settings.png" width="49%" alt="Settings with cursor themes" />
  <img src="screenshots/1-home.png" width="49%" alt="Home screen" />
</p>

## Install

1. Go to [Releases](../../releases/latest).
2. Download **HundredTwenty-Setup-1.2.0.exe** (installer) or **HundredTwenty-1.2.0-portable.exe** (no install).
3. Windows may show "Windows protected your PC" because the app isn't code-signed. Click **More info → Run anyway**.

**Already installed?** 1.1.0 and later update themselves to 1.3.0: restart when the title bar says **Update ready**. On 1.0.0, run the 1.2.0 installer once. It closes the app, removes 1.0.0 and keeps your settings. See the [changelog](CHANGELOG.md).

## How to post at 120fps

1. Export a **120fps** edit from your editor (After Effects, Premiere, CapCut…).
2. Drop it into Hundred Twenty, keep **Patch**, hit **Export**. The exported file plays slowed on PC, that is expected. Don't re-export it.
3. Click **Open TikTok**. Drag the file in, press **Ctrl+V** for the caption, then **Post**.
4. Give it a few minutes after posting while TikTok processes it. Patch is temporary while we work on a fix for TikTok's change.

## Requirements

- Windows 10 or 11 (64-bit)
- Any 64-bit CPU (exports use x264)

## Built with

![JavaScript 54.7%](https://img.shields.io/badge/JavaScript-54.7%25-f1e05a?style=flat-square&logo=javascript&logoColor=black)
![CSS 32.9%](https://img.shields.io/badge/CSS-32.9%25-663399?style=flat-square&logo=css&logoColor=white)
![HTML 11.3%](https://img.shields.io/badge/HTML-11.3%25-e34c26?style=flat-square&logo=html5&logoColor=white)
![SQL 0.5%](https://img.shields.io/badge/SQL-0.5%25-e38c00?style=flat-square)
![Other 0.7%](https://img.shields.io/badge/Other-0.7%25-555555?style=flat-square)

- **JavaScript** on **Electron** and **Node.js** runs the app, and a **Cloudflare Worker** handles the signed updates and anonymous stats.
- **HTML** and **CSS** draw the interface: every layout, style and theme.
- **FFmpeg** (x264 + AAC) does the encoding.
- **SQL** defines the stats tables in Cloudflare D1. Other is the Windows installer script (NSIS), a batch launcher and a VBScript starter.

The source code is private, so GitHub's language bar stays empty here. These shares are measured from it.

## Privacy

Hundred Twenty sends anonymous usage stats: a random install ID, the app version, your Windows version, the export mode you used and your country (worked out by the server; your IP address is never stored). It never sends files, file names or account details. Turn it off in Settings → Privacy.

## Notes

Hundred Twenty uses an unofficial upload method. TikTok can change how it processes videos at any time. Use it at your own risk.

## License

Hundred Twenty is closed source. © 2026 messor1053. All rights reserved. See [LICENSE](LICENSE).
