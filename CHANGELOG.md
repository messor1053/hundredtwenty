# Changelog

## 1.4.0 · November 6, 2026

**This installs itself.** It downloads in the background, then the title bar shows **Update ready · Restart**.

On November 3 TikTok changed how it processes uploads. It now re-encodes every video and plays it at 60 fps at most, so a true 120 fps file can't come through anymore. Studio relied on TikTok keeping the original file, which is why it's still under maintenance. This update adds **Halftime**, the best result you can get under TikTok's limit, plus a big design update.

### New

- **Halftime method.** The new default, marked with the star. It keeps every one of your 120 fps frames at 1080p. TikTok plays at most 60 fps, so Halftime plays your edit at half speed: smooth 60 fps slow motion at twice the length. A 20 second edit becomes 40 seconds, not 2 minutes like the old Patch. The audio is slowed to match. Tested on TikTok: 1080p, 60 fps, every frame kept.
- **60 fps method.** Normal speed at 1080p 60 fps. A 120 fps edit keeps every 2nd frame, so motion stays perfectly even.
- **Ten new styles.** Luxe, Prism, Chrome, Soft, Clay, Paper, Blueprint, HUD, Brutal and Swiss, plus **Surprise me** for a random style and accent. That makes 14 styles, and every one works with every layout, theme and accent.
- **Premium touches.** A short launch intro, subtle film grain, keyboard focus rings and toasts with a timer bar. There are also keyboard shortcuts, listed in Settings: **Ctrl+O** to open, **Ctrl+E** to export and **Ctrl+,** for settings.

With both methods, TikTok shows 540p for the first 10 to 20 minutes after posting, then switches to 1080p 60.

### Halftime vs Studio right now

Since November 3, TikTok re-encodes a Studio export like any other upload. It shows 540p first, then 1080p 60 with every 2nd frame dropped. Halftime gets the same 1080p 60 and keeps all 120 frames. Studio comes back as soon as TikTok lets 120 fps through again.

### Changed

- **The old Patch method is replaced.** TikTok played it at 540p and 20 fps, 6x slowed, with choppy audio.
- **Resolution.** TikTok shows uploads at up to 1080p right now, and the app says so. 2K and 4K are still there, but TikTok scales them down to 1080p.

## 1.3.0 · November 6, 2026

**This installs itself.** It downloads in the background, then the title bar shows **Update ready · Restart**.

On November 3 TikTok changed how it processes uploads, and the 120fps methods stopped working for everyone. This update adds a temporary method while we work on a fix.

### New

- **Patch method (temporary).** The new default. It exports at 120fps, then stretches the file's timing so TikTok keeps every frame. The exported file plays slowed on PC, that is expected. Upload it from a PC browser and don't re-export it. It's temporary: it will be replaced as soon as we have a fix.
- **Method card.** Patch shows a **Temporary** badge. **Studio** is grayed out and marked **Maintenance** until it works on TikTok again.

### Changed

- **Your edit keeps its shape.** **Original** framing is now the default: square, landscape and portrait edits stay that shape and are only scaled down to fit 1080p (2K and 4K keep more). Fit and Fill are still there if you want a 9:16 frame.
- **Old methods removed.** Pass, Method, Itsscale and 60 Clean stopped working with TikTok's change and are gone. Studio is under maintenance (grayed out, not clickable) until it works again.
- **CPU encoding.** Exports run on the CPU (x264). The GPU (NVENC) switch is gone.

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
