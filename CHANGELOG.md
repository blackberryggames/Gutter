# Changelog

## v1.07

- Exports are about 3x faster with the same quality
- Captions are burned in while each piece renders, instead of re-encoding the whole video at the end (one encode instead of two, so it's slightly sharper too)
- Panels are converted once instead of on every frame, and the narration track is built while the video renders
- Captions now land on exactly the right frame everywhere in long videos

## v1.06

- Export no longer just shows "Getting FFmpeg ready": if FFmpeg still needs downloading, it happens inside the export screen with a progress bar, then the export starts by itself
- The FFmpeg check at startup runs in the background, so it can't hold up the app
- Opening Projects no longer freezes for a moment: card thumbnails load in the background

## v1.05

- Fixed exports crashing at the end ("FFmpeg crashed") on PCs with an old FFmpeg installed by other apps: Gutter now ignores FFmpeg older than 7
- Outdated FFmpeg is detected and replaced automatically with Gutter's own up-to-date copy
- Gutter's FFmpeg checks for a newer release about once a week and updates itself in the background
- If a transition still makes FFmpeg crash, that one cut is exported as a crossfade instead of failing the export

## v1.04

- New installer: GutterSetup.exe with a big logo, animated progress, shortcuts, and an entry in Windows Installed apps (uninstall from there)
- Exports recover from FFmpeg crashes: a step that crashes is retried automatically, single-threaded and then on its own
- Steadier exports: fewer FFmpeg jobs run at the same time
- When an export fails or Gutter crashes, it can send a diagnostic report so it gets fixed (Settings → Reports to turn it off)
- The Export failed screen says which stage stopped and has Copy details

## v1.03

- Write scripts with your Claude app, no API key: the new Script Generator MCP lets Claude Desktop or Claude Code read your panels and write the lines into Gutter
- One-click setup for it: Write script (with "Claude app via MCP") or Settings → AI apps installs the MCP and connects Claude Desktop
- FFmpeg sets itself up: found automatically or installed in the background, nothing to click
- Export waits for FFmpeg if it's still installing instead of failing
- Setup walkthrough shows FFmpeg's status and has a "Use my Claude app instead" option
- Settings → AI apps: turn the local AI bridge on or off

## v1.02

- Projects tab: every project as a card with its first frame, length, script and voice progress
- The editor now fills the window, with a Back to Projects button
- Media bin: drag images onto the timeline, or drop files in from Explorer
- Right-click menus on clips, cuts, the preview and media
- Story info: main character, cast, notes and genre templates the AI always gets, plus intro and outro lines
- 14 transitions (Mix on every cut by default), previewed live on each tile
- Custom image or looping video backgrounds, blurred or sharp
- The blurred backdrop now scrolls with tall panels
- Sync button: finds voice lines that get cut off and fixes them
- Preview no longer clips the last word of a line
- Continue writing or voicing where you left off; Ctrl+click lines to re-voice just those
- Setup walkthrough for Groq and ElevenLabs; Groq sends 3 panels per request
- Rounded window, new logo, styled dialogs, caption font preview fix
