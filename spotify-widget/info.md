# Spotify Widget

A lightweight "now playing" overlay for OBS. Run the exe and it serves a Spotify-styled
card — album art, track, artist, and a live progress bar — that you drop into your scene
as a browser source. No Spotify login, no API keys: it reads whatever Windows itself
reports as the currently playing media.

- **Download:** `Spotify Widget.exe`
- **Screenshot:** `screenshot.png`
- **Platform:** Windows 10 / 11 (64-bit)
- **Requirements:** none — no Python, no Spotify developer account

## How to use

1. Run **Spotify Widget.exe**. It starts a small local server and opens
   `http://localhost:7878/` in your browser so you can confirm it's working.
   There is no app window — that's normal, it lives in the browser source.
2. In OBS: **Sources → + → Browser**.
3. Set:
   - **URL:** `http://localhost:7878/`
   - **Width:** `480`
   - **Height:** `128`
   - Leave "Shutdown source when not visible" **off**.
4. Position the card in your scene. The background is transparent, so it composites
   straight over gameplay or your webcam.
5. Keep the exe running while you stream. Closing it blanks the source.

Start playing something in Spotify and the card fades in. It updates once a second,
crossfades on track change, and fades out when nothing is playing.

## Also included

The same server exposes two JSON endpoints, in case you want to build your own overlay
against it (CORS is open, so a browser source on any page can read them):

- `http://localhost:7878/now-playing` — `title`, `artist`, `album`, `position_percent`,
  `is_playing`, `thumbnail_b64` (base64 album art)
- `http://localhost:7878/stats` — `cpu`, `ram`, `ram_used_gb`, `ram_total_gb`, plus
  `gpu` when an NVIDIA card is present

## Troubleshooting

- **"Port 7878 is already in use"** — the widget is already running. Check Task Manager
  for an existing `Spotify Widget.exe` and end it before starting a new one.
- **Card is invisible in OBS** — nothing is playing. The card only appears once Windows
  reports an active track.
- **Album art missing** — some tracks (local files, certain podcasts) don't publish
  artwork; the widget falls back to a placeholder icon.
- **Works with more than Spotify** — anything that reports to the Windows media controls
  (Tidal, YouTube in Edge, etc.) will show up too.
