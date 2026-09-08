# Spotify Widget

A lightweight, customizable “now playing” overlay for OBS. Run the exe and it serves a
transparent album-art card with the current track, artist, playback state, and live
progress bar. It reads the Windows media session, so there is no Spotify login, API key,
or extra runtime to install.

- **Download:** `Spotify Widget.exe`
- **Screenshot:** `screenshot.png`
- **Platform:** Windows 10 / 11 (64-bit)
- **Requirements:** none — no Python or Spotify developer account

## Choose a layout

Open `http://localhost:7878/` in a normal browser and **right-click anywhere on the
page**. The studio opens with 15 live options across five layout families:

- **Compact:** Classic, Aurora, Vinyl Strip, Frost, Minimal, Cyber
- **Square:** Album Tile, Orbit, Corner Bubble
- **Collector:** Turntable, Cassette
- **Vertical:** Polaroid, Vertical Stack
- **Video:** Cinema, Spectrum

These are not just colour themes: artwork can become a full square cover, circular
progress halo, spinning record, cassette deck, portrait card, floating corner bubble,
video poster, or animated spectrum. The studio also includes a safe **70–100% size
slider**, five quick colour swatches, and a full custom accent-colour picker. Adjust the
look, then click the layout you want. The studio closes, your selection appears
immediately, and the app remembers the full combination for OBS and future launches.

## Add it to OBS

1. Run **Spotify Widget.exe**. It starts a local server and opens
   `http://localhost:7878/` in your browser.
2. Choose the look you want by right-clicking the page.
3. In OBS, go to **Sources → + → Browser**.
4. Set:
   - **URL:** `http://localhost:7878/`
   - **Width / Height:** use the exact canvas size shown for your selected layout
   - Leave “Shutdown source when not visible” **off**.
5. Keep the exe running while you stream. Closing it blanks the source.

Start playing something in Spotify and the widget fades in. It updates once a second,
crossfades when the track changes, and fades out when nothing is playing. The background
is transparent, so it composites directly over gameplay or a webcam.

## JSON endpoints

The local server keeps the existing open-CORS endpoints for custom overlays:

- `http://localhost:7878/now-playing` — title, artist, album, progress, playback state,
  and base64 album art
- `http://localhost:7878/stats` — CPU, RAM, and NVIDIA GPU data when available

## Troubleshooting

- **“Port 7878 is already in use”** — the widget is already running. End the existing
  `Spotify Widget.exe` process in Task Manager, then start it again.
- **Card is invisible in OBS** — nothing is playing. The card appears when Windows
  reports an active track.
- **Album art is missing** — local files and some podcasts do not publish artwork, so
  the widget uses its built-in music placeholder.
- **Other players appear** — the widget follows the active Windows media session, so
  Tidal, browser video, and other compatible players work too.
