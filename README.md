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
- **120 Method.** Encodes constant 120fps, then patches the MP4 headers so TikTok's transcoder keeps every frame. Based on [ut0ku/120fps-method](https://github.com/ut0ku/120fps-method).
- **120 Itsscale.** The classic FFmpeg `-itsscale` version, built in too.
- **60 Clean.** Plain 1080p60 for when you just want it to look right everywhere.
- **GPU encoding.** NVIDIA NVENC at its highest-quality preset, with a CPU (x264) fallback.
- **Tuned settings.** 1080×1920, H.264 High, 30 Mbps, 1-second GOP, BT.709, AAC 320k. A bitrate slider is there if you want more.
- **Motion interpolation.** Builds real in-between frames for clips under 120fps.
- **One-click TikTok.** Opens TikTok Studio in your browser with the caption already copied.

## Design

Black and white, rounded and smooth. Every card tilts in 3D toward your cursor with glare and depth. Spring animations, a live 9:16 preview, a progress ring, sound on every click, and five cursor themes.

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
2. Download **HundredTwenty-Setup-1.0.0.exe** (installer) or **HundredTwenty-1.0.0-portable.exe** (no install).
3. Windows may show "Windows protected your PC" because the app isn't code-signed. Click **More info → Run anyway**.

## How to post at 120fps

1. Export a **120fps** edit from your editor (After Effects, Premiere, CapCut…).
2. Drop it into Hundred Twenty, keep **120 Method**, hit **Export**.
3. Click **Open TikTok**. Drag the file in, press **Ctrl+V** for the caption, then **Post**.
4. Watch it in the TikTok **phone app** on a 120 Hz screen. Desktop playback may look slowed, which is normal for this method.

## Requirements

- Windows 10 or 11 (64-bit)
- NVIDIA GPU recommended (any CPU works with x264)

## Notes

Hundred Twenty uses an unofficial upload method. TikTok can change how it processes videos at any time. Use it at your own risk.

## License

Hundred Twenty is closed source. © 2026 messor1053. All rights reserved. See [LICENSE](LICENSE).
