# Streamtools

Tools for the "Stream&Tool" tab on theboardapp.org. Each tool gets its own folder with the exe, a screenshot/gif, and a short description — that's the section shown on the site.

## Structure

```
streamtools/
  spotify-widget/
    Spotify Widget.exe
    info.md
    screenshot.png
  <next-tool>/
    <tool>.exe
    info.md
    screenshot.png
```

`info.md` per tool: one-line title, 2-3 sentence description, and anything the download section needs (version, requirements).

## Workflow

- Push from either machine (this one or the laptop) to this repo.
- Pull the latest here before you sync content into theboardapp.org.
- Binaries and images are tracked via Git LFS (`.gitattributes`) so the repo doesn't bloat with history.
