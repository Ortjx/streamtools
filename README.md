# Streamtools

Tools for the "Stream&Tool" tab on theboardapp.org. Each tool gets its own folder with the exe, a screenshot/gif, and a short description — that's the section shown on the site.

## Structure

```
streamtools/
  spotify-widget/
    Spotify Widget.exe
    info.md
    screenshot.png
  stream-pet-creator/
    StreamPet Creator.exe
    info.md
    screenshot.png
  input-arcade/
    Input Arcade.exe
    info.md
    screenshot.png
```

`info.md` per tool: one-line title, 2-3 sentence description, and anything the download section needs (version, requirements).

## Tools

| Tool | Folder | What it is | Local port |
|------|--------|------------|------------|
| Spotify Widget | `spotify-widget/` | OBS browser-source "now playing" card, plus `/now-playing` and `/stats` JSON endpoints | 7878 |
| StreamPet Creator | `stream-pet-creator/` | Five-style character lab, reactive OBS pet, and portable StreamElements/PNG/HTML exports | 7880 |
| Input Arcade | `input-arcade/` | Full-size 104-key keyboard and mouse visualizer with independent hardware skins | 7890 |

Each tool's `info.md` is the copy that gets published in the Stream & Tools panel on
theboardapp.org: title, description, requirements, setup steps, troubleshooting.

## Note on sources

This repo holds the **built exes and their site copy only** — it is the publishing
staging area, not the source tree. Keep each tool's source in its own project/repo.

## Workflow

- Push from either machine (this one or the laptop) to this repo.
- Pull the latest here before you sync content into theboardapp.org.
- Binaries and images are tracked via Git LFS (`.gitattributes`) so the repo doesn't bloat with history.
