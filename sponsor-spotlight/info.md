# Sponsor Spotlight

Your sponsors as short 3D animations on stream. Add each sponsor once — logo, one line, a code, a website — and the overlay plays one on a timer, on a hotkey (it works mid-game), from the customiser, or from a Stream Deck button. 13 animations, 11 borders, and every detail of the look is yours — fonts (even your own), colours, card, logo, layout, speed and a sound per sponsor. A see-through PNG logo gets real depth.

It runs completely on your computer, needs no account, and refuses requests from other websites.

## Version

1.2.0

## Setup

1. Switch it on in Workbench › Stream & Tools (or run `Sponsor Spotlight.exe`).
2. Customise it at `http://localhost:7895`: add sponsors, pick a style per sponsor, how often it plays and where.
3. Add `http://localhost:7895/overlay` to OBS as a Browser Source at 1920 × 1080.
4. Stream Deck: a Website action pointed at `http://localhost:7895/api/play` plays the next sponsor (`?id=…` for a certain one).
