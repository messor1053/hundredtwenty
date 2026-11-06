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

Hundred Twenty takes any edit, encodes it with FFmpeg and preps it for TikTok. You don't touch the command line, patch anything by hand or guess settings.

## Features

- **Drop and export.** Drag in an MP4, MOV, MKV or WEBM, then hit Export.
- **Halftime (the default).** TikTok changed how it processes uploads on November 3: it re-encodes everything and plays it at 60 fps at most. Halftime keeps every one of your 120fps frames at 1080p by playing the edit at half speed, so it's smooth 60 fps slow motion at twice the length. Tested on TikTok: 1080p, 60 fps, every frame kept.
- **60 fps.** Normal speed at 1080p 60 fps. A 120fps edit keeps every 2nd frame, so motion stays even.
- **Studio (maintenance).** The original 120 Studio method needs TikTok to keep the original file, which it stopped doing on November 3. It's grayed out until that works again. Right now TikTok drops every 2nd frame of a Studio export, while Halftime keeps them all.
- **Tuned settings.** 1080×1920 H.264 at about 12 Mbps with AAC audio. A bitrate slider is there if you want more.
- **1080p.** TikTok shows uploads at up to 1080p right now. 2K and 4K exports are still there for sources bigger than 1080p, but TikTok scales them down to 1080p.
- **Output summary.** See the frame size, bitrate, encoder and an estimated file size before you export.
- **Motion interpolation.** Builds real in-between frames for clips under 120fps.
- **One-click TikTok.** Opens TikTok Studio in your browser with the caption already copied.
- **Keyboard shortcuts.** **Ctrl+O** to open, **Ctrl+E** to export, **Ctrl+,** for settings.
- **Automatic updates.** New versions download in the background and install on restart. No more redownloading.

## Design

Make it yours. Pick a layout: **Classic**, **Steps** (one step at a time), **Pro** (sidebar, inspector and status bar) or **Bento** (every control its own tile). Pick one of 14 styles: **Clean**, **Glass**, **Terminal**, **Neon**, **Luxe** (black and gold), **Prism** (iridescent borders), **Chrome** (brushed metal), **Soft** (raised and pressed), **Clay** (puffy and rounded), **Paper** (warm stock and serif type), **Blueprint** (drafting grid), **HUD** (sci-fi brackets), **Brutal** (thick ink and hard shadows) or **Swiss** (grotesk type and rules), or hit **Surprise me**. Then a theme (Midnight, Graphite, Aurora or Light) and one of nine accent colours. Every card tilts in 3D toward your cursor with glare and depth. Spring animations, a live 9:16 preview, a progress ring, sound on every click, and five cursor themes.

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

**Already installed?** 1.1.0 and later update themselves to 1.4.0: restart when the title bar says **Update ready**. On 1.0.0, run the 1.2.0 installer once. It closes the app, removes 1.0.0 and keeps your settings. See the [changelog](CHANGELOG.md).

## How to post at 120fps

1. Export a **120fps** edit from your editor (After Effects, Premiere, CapCut…).
2. Drop it into Hundred Twenty, keep **Halftime** (or pick **60 fps** for normal speed), hit **Export**. Don't re-export the file.
3. Click **Open TikTok**. Drag the file in, press **Ctrl+V** for the caption, then **Post**.
4. TikTok shows 540p for the first 10 to 20 minutes, then switches to 1080p 60.

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
