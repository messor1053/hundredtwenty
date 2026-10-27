# Changelog

## 1.2.0 · October 27, 2026

**On 1.1.0 this installs itself.** It downloads in the background, then the title bar shows **Update ready · Restart**. Still on 1.0.0? Run the 1.2.0 installer once.

### New

- **2K export.** A **Resolution** choice sits with Audio in the export options: **1080p** (the long-proven default), **2K** or **4K**. 2K keeps sources bigger than 1080p at up to 1440p (about 22 Mbps) and works on TikTok right now. 4K (2160p, 45 Mbps) is marked Risky and is patched on TikTok right now.
- **Four layouts.** Pick one in Settings → Layout:
  - **Classic**: the preview on the left and every setting on the right, like before.
  - **Steps**: one step at a time (Video, Method, Quality, Export) with Back and Next.
  - **Pro**: tabs in a sidebar, the preview in the middle, an inspector on the right and a status bar along the bottom.
  - **Bento**: every control is its own tile, with a big bitrate readout and an Export tile.
- **Four styles.** Pick one in Settings → Style: **Clean** (like before), **Glass** (frosted panels over soft colour), **Terminal** (monospace, square corners, scanlines) or **Neon** (glow, gradients and a grid horizon). Every style works with every theme and accent colour.
- **Output summary.** Steps, Pro and Bento show what your export will be before you hit Export: method, frame size, bitrate, frame rate, encoder and an estimated file size.
- **Number keys.** Jump between steps in Steps and between tabs in Pro.

### Improved

- **Sharper Studio exports.** A slower, better-tuned encode at the same 12 Mbps. On a 4K test clip, quality went from 34.7 to 42.4 dB (PSNR), and SSIM from 0.942 to 0.983.

### Fixed

- **Mushy exports from 4K sources.** Original framing sent 4K sources through at a 1080p bitrate. They're now scaled down sharply to TikTok's 1080p.
- **Exporting an export.** You now get a warning, since it lowers quality, and the file name no longer stacks up "_tiktok_120fps".

## 1.1.0 · October 20, 2026

**Reinstall once.** 1.0.0 can't update itself, so download 1.1.0 and run the installer. It closes Hundred Twenty if it's open, removes 1.0.0 and keeps your settings. After this, updates install themselves.

### New

- **Automatic updates.** New versions download in the background. When one is ready, the title bar shows **Update ready · Restart**. Every update is signed, and if one ever fails to start, the app goes back to the last version that worked.
- **Themes.** Midnight, Graphite, Aurora and Light, plus nine accent colours. Find them in Settings → Theme and Accent.
- **Studio is marked as the best method.** Pick another method and a **Use Studio** button switches you back in one click.
- **Hands-off upgrades.** The installer closes a running copy and removes the old version for you.
- **Anonymous usage stats.** The app sends a random install ID, the app version, your Windows version, the export mode you used and your country (worked out by the server; your IP address is never stored). No files, names or accounts. Turn it off in Settings → Privacy.

## 1.0.0 · October 18, 2026

First release.

- **120 Studio**: true 120fps exports that TikTok serves untouched.
- Experimental Pass, Method and Itsscale modes, plus 60 Clean.
- NVIDIA NVENC encoding with a CPU fallback, and motion interpolation.
- One-click TikTok with the caption copied.
- 3D hover tilt, click sounds and five cursor themes.
