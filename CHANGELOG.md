# Changelog

## 1.5.0 · November 12, 2026

**This installs itself.** It downloads in the background, then the title bar shows **Update ready · Restart**.

**Studio is back, and it is true 120 fps again.** Since November 3 TikTok re-encoded every upload and capped it at 60 fps. Studio now writes the file with a new container patch, and TikTok keeps it exactly as uploaded. Tested on a public post on November 12: TikTok served the original 1080p file at 120 fps, every frame, right after posting.

### New

- **Studio, rebuilt.** The default again, marked with the star. Your edit is encoded at true 120 fps (H.264 High, about 12 Mbps, AAC stereo) and the file gets the new patch: a short silent tail on the sound and a second copy of the audio track. The picture is not touched by the patch.
- **120 fps right away.** No waiting for TikTok to process a better copy: the original 1080p 120 fps file is what plays.
- **Videos without sound work too.** Studio needs a sound track, so a silent one is added when your edit has none or Audio is off.

### Changed

- **Halftime, Clearframe, 60 fps and FFMPEG stay** as they were, for 60 fps uploads. Halftime no longer carries the star.
- **Resolution.** The new Studio is tested at 1080p. 2K and 4K are still there, but not tested with it yet.

### Good to know

- Upload from a PC browser and don't re-export the file.
- This is an unofficial method. It passed one public test so far, and TikTok can change how it handles uploads at any time, like it did on November 3.

## 1.4.0 · November 6, 2026

**This installs itself.** It downloads in the background, then the title bar shows **Update ready · Restart**.

On November 3 TikTok changed how it processes uploads. It now re-encodes every video and plays it at 60 fps at most, so a true 120 fps file can't come through anymore. Studio relied on TikTok keeping the original file, which is why it's still under maintenance. This update adds **Halftime**, the best result you can get under TikTok's limit, plus a big design update.

### New

- **Halftime method.** The new default, marked with the star. It builds your edit at 120 fps and blends each pair of frames into one 60 fps frame at 1080p, so the edit keeps its own speed and motion looks smoother than when half the frames are dropped.
- **60 fps method.** Normal speed at 1080p 60 fps. A 120 fps edit keeps every 2nd frame, so motion stays perfectly even.
- **Ten new styles.** Luxe, Prism, Chrome, Soft, Clay, Paper, Blueprint, HUD, Brutal and Swiss, plus **Surprise me** for a random style and accent. That makes 14 styles, and every one works with every layout, theme and accent.
- **Premium touches.** A short launch intro, subtle film grain, keyboard focus rings and toasts with a timer bar. There are also keyboard shortcuts, listed in Settings: **Ctrl+O** to open, **Ctrl+E** to export and **Ctrl+,** for settings.

With both methods, TikTok shows 540p for the first 10 to 20 minutes after posting, then switches to 1080p 60.

### Halftime vs Studio right now

Since November 3, TikTok re-encodes a Studio export like any other upload. It shows 540p first, then 1080p 60 with every 2nd frame dropped. Halftime gets the same 1080p 60 and blends all 120 frames in pairs instead. Studio comes back as soon as TikTok lets 120 fps through again.

### New in hot update 1.4.6

- **FFMPEG: Double duration.** The FFMPEG section now starts on **Double duration**, the classic ffmpeg method (`-itsscale 2`): your frames are copied untouched and every timestamp is doubled, so the video is twice as long and plays slowed. Every frame is placed exactly 1/60 s apart (the broken timestamps in Topaz files are fixed without re-encoding), the audio is slowed to match by default (**Original** and **Normal** are still there), and Motion interpolation builds a 60 fps source up to 120 first. TikTok plays it 2x slow on every device; for normal speed use Halftime. **Re-encode** keeps every 1.4.5 setting.
- **Faster fixes.** Small fixes for your version can now arrive in the background without a new version number: the title bar shows **Fix ready · Restart**. A fix that doesn't start properly rolls itself back.
- **Privacy.** Anonymous stats now also send your device's time zone. The server only compares it with where the connection comes from and doesn't store it.

**Fix 1 for 1.4.6 (November 9):** the FFMPEG section is now just **60 fps** or **120 fps**, picked from your video. It's always the classic `-itsscale 2` method: your frames copied untouched and every timestamp doubled, with every frame exactly evenly spaced. The Double duration / Re-encode switch, the audio choice and Frame check are gone. The title bar shows **1.4.6 (fix 1)** once it's in.

### New in hot update 1.4.5

- **Halftime versions.** Halftime now has a Version switch: **R12** (the default, the same export Halftime always made), **R11** (the same 12 Mbps with x264's standard adaptive quantisation) and **R9** (constant quality, CRF 14). All three were tested on TikTok with the same edit and kept every frame at 1080p 60.
- **Clearframe.** A new method built from our own TikTok tests: Halftime's smooth 1080p 60 saved as 10-bit HEVC, using your NVIDIA GPU when you have one. The same edit uploaded seven different ways came out within a fraction of a point on TikTok, and 10-bit HEVC got there from the smallest file, so it uploads faster and exports in seconds.
- **FFMPEG section.** Pick FFMPEG as the method to choose everything yourself: 1080p 60 or 1080p 120, x264, x265 or NVIDIA NVENC (H.264, HEVC, AV1), quality, bitrate or 2-pass, MP4, MOV, MKV or AVI, 10-bit, and blending 120 down to 60. It shows the exact ffmpeg command, and **Frame check** tells you whether your video's frame rate is real or padded with repeated frames. 1080p 120 is only built from real 120 fps frames, never duplicated ones. TikTok plays 60 fps at most right now, so 1080p 120 is for other platforms and your archive.
- **TikTok optimiser.** Off by default, under Extras. Makes Halftime R12 and 60 fps files smaller with every frame and the same frame rate, checked frame by frame against your edit (16.5 MB down to 10.9 MB on a Topaz edit, quality 98.6). TikTok re-encodes every upload anyway, so it's about a smaller, faster upload.
- **Framing tips.** Hover Original, Fit or Fill to see what each does: Fill zooms a square or wide edit to 9:16 and cuts off the sides.

### Fixed (hot updates 1.4.1 to 1.4.4)

- **No slow motion (1.4.2 to 1.4.4).** Halftime briefly played your edit slowed down to show every frame, and 1.4.3 had a Speed switch for it. TikTok plays any slowed file as slow motion on every device, so it's gone: Halftime always plays at your edit's own speed.
- **Audio stays in sync (1.4.1).** The slowed audio of the old half-speed export used to drift ahead of the picture. Halftime no longer slows anything, so your audio is exactly as you edited it.
- **No dropped frames from Topaz (1.4.1).** Topaz writes a couple of broken timestamps in its 120 fps files, and two frames got dropped. Every frame is kept now, perfectly even, for both Halftime and 60 fps.

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
