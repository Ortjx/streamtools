# StreamPet Creator

Build a reactive stream character locally with five genuinely different art systems: illustrated realism, anime, graphic 2D, cartoon, and pixel. Mix seven species, six coat patterns, three proportions, five auras, eight accessories, expressive eyes, custom palettes, fluff, line weight, grounding and microphone sensitivity—or start from one of six polished character recipes.

Every pet is portable. Export one ZIP containing an editable `.streampet` project, six transparent PNG expressions, a self-contained HTML browser widget, and a StreamElements custom-widget bundle that can react to chat, follows, subscriptions, tips, and cheers without giving StreamPet your Twitch account.

## Version

3.0.0

## Requirements

- Windows 10 or 11
- A microphone is optional; reaction buttons and exported widgets work without one
- OBS is optional
- StreamElements is only needed if you choose to use the exported StreamElements bundle

## Quick setup

1. Run `StreamPet Creator.exe`. Your browser opens the local creator at `http://localhost:7880`.
2. Choose an art direction and build the character, or start with a ready-made recipe.
3. In OBS, add a Browser Source using `http://localhost:7880/pet` at 640 × 640.
4. Use **Export character pack** when you want files that no longer depend on the creator.

## Exported files

- `browser-widget/pet.html`: self-contained local-file Browser Source
- `streamelements/`: HTML, CSS, JS, and Fields files for a Custom Widget
- `images/`: transparent expression PNGs
- `<name>.streampet`: editable project to import back into the creator

Settings are saved locally beside the executable in `streampet.json`.
