# Title-Screen-Builder

A single-file app for making animated 90s VHS-style title screens (1920 × 1080) for personal videos.

Open `index.html` in a current Chrome, Edge, Firefox or Safari. It needs no server, build step or dependencies.

## Features

- Two-line oversized title and a small top line for a date, place or subtitle
- Analog look: pink/purple glow, red/blue chromatic fringing, scanlines, tape grain, flicker, tracking noise, head-switching noise, vignette
- The title glitches in, settles, and then has occasional tracking hiccups (with an optional glitch-out at the end)
- Play / pause / replay and a timeline scrubber (Space toggles playback)
- 25 fonts with a visual picker, including tech fonts (Orbitron, Audiowide, VT323, Press Start 2P…) loaded from Google Fonts when online. You can also load your own font file
- Settings are kept in your browser between visits

## Export

**Export video** records the full animation in real time at 1920 × 1080. You get MP4 (H.264) when the browser supports it (recent Chrome/Edge and Safari) and WebM otherwise. Keep the tab visible while it records.

To convert a WebM to MP4:

```bash
ffmpeg -i vhs-title.webm -c:v libx264 -pix_fmt yuv420p -crf 16 -r 30 vhs-title.mp4
```

**Save frame** downloads the current frame as a 1920 × 1080 PNG.
