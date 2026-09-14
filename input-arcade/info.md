# Input Arcade

Turn a complete 104-key keyboard and five-button mouse into a premium transparent stream overlay. Choose keyboard and mouse skins independently—from midnight aluminium, snow PBT, terminal beige and bamboo to cyber, sakura, honeycomb, or fully custom materials—then tune lighting, size, spacing, opacity, response and trails.

Input Arcade runs completely on the user's computer. It reads key and pointer state natively, works offline, requires no account, never reconstructs words, and does not save or transmit input history.

## Version

3.0.0

## Requirements

- Windows 10 or 11
- OBS is optional

## Setup

1. Run `Input Arcade.exe`.
2. Customize the overlay at `http://localhost:7890`.
3. Add `http://localhost:7890/overlay` to OBS as a Browser Source at 1600 × 650.
4. Leave Input Arcade running while streaming.

Use the live diagnostics and bench-test buttons to confirm the keyboard and mouse before opening OBS.

Settings are stored locally beside the executable in `input-arcade.json`.
