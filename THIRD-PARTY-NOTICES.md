# Third-party notices

ShotReel includes the components below. Each keeps its own licence; ShotReel's own code is covered by the ShotReel licence.
Full licence texts ship inside the installed app under `resources/app/node_modules/<package>/` and `resources/`.

## Bundled programs and models

| Component | Licence | Notes |
|---|---|---|
| Electron 45 (includes Chromium) | MIT, plus Chromium's BSD-style licences | Licence list: `LICENSES.chromium.html` next to the exe |
| chrome-headless-shell (Chromium) | BSD-3-Clause and others | Renders video frames |
| FFmpeg (BtbN LGPL build, no GPL or nonfree parts) | LGPL-2.1-or-later | Separate `ffmpeg.exe` in `resources/bin`, replaceable. Source: https://ffmpeg.org/download.html and https://github.com/BtbN/FFmpeg-Builds |
| Kokoro-82M v1.0 ONNX voice model | Apache-2.0 | `onnx-community/Kokoro-82M-v1.0-ONNX` |
| ShotReel.Capture (.NET) | Microsoft .NET runtime licences (MIT) | Mouse hook and UI Automation |

## npm runtime dependencies (production tree)

| Licence | Packages |
|---|---|
| MIT | 81, including fflate, zod |
| Apache-2.0 | 14, including hyperframes, kokoro-js, @huggingface/transformers |
| BSD-3-Clause | 15 |
| ISC | 9 |
| BlueOak-1.0.0 | tar, minipass, chownr, yallist |
| CC0-1.0 | mdn-data |
| 0BSD, MIT OR CC0-1.0 | 1 each |
| LGPL-3.0-or-later (with Apache-2.0 / MIT) | `@img/sharp-win32-x64` (libvips, a separate DLL in `node_modules`, replaceable) |
| GreenSock "Standard no charge" licence | `gsap` 3.12.5. **Not open source.** See below |

Regenerate the counts: walk `dependencies` in `package.json` and read each `license` field.

## Interface fonts

IBM Plex Sans and IBM Plex Mono (via `@fontsource`): SIL Open Font License 1.1.

## GSAP

GSAP is used inside rendered video pages. GreenSock's Standard licence allows free use, including in commercial products, but
forbids use in a product that competes with GreenSock's own tools, such as a visual animation builder sold to others.
Before selling a Pro edition, read https://gsap.com/standard-license and decide whether ShotReel qualifies. If unsure, ask
GreenSock or replace GSAP with a small custom timeline.

## LGPL notice (FFmpeg, libvips)

Both libraries are used unmodified as separate files. You may replace them with your own builds of the same library.
