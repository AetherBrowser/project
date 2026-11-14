# Aether Sprint Retro Meeting

Date: 2026-11-07

Location: Microsoft Teams

Attending:
  - corentin.bergaentzle@epitech.eu
  - nathan.callegari@epitech.eu
  - matteo.milin@epitech.eu
  - thomas.richalet@epitech.eu
  - axel.battigelli@epitech.eu

## What Went Well

- **Ad blocker:** progressing well. On this branch, it only blocks domain names entered manually; users can type them in or paste the contents of a list file.
- **Bug fixes:** bugs reported by beta testers were fixed, including YouTube not loading after a YouTube update because a header exceeded the 16 KB limit.
- **Playback speed:** adjustable from a browser UI, with pitch correction so audio no longer gets higher-pitched when sped up.
- **Video playback (MPV):** the rendering context is ready. MPV no longer opens its own window, and subtitle display is left to the page.
- **Bookmarks:** assets are on master, in the resources with the other icons.
- **Beta feedback:** positive overall (lightweight, privacy-respecting). Some testers use it on regular, recent PCs, beyond the original target of older devices.
- **Planning:** sprints 6 and 7 are on track and stay unchanged.

## What Didn't Work Well

- **Devtools behind schedule:** splitting the work into branches surfaced bugs and implementation issues, so the week went into refactoring, optimization and debugging. The devtools console would be very useful for debugging.
- **Bookmarks:** little progress over the past two weeks due to other commitments. Bookmark folder management (creating and editing folders) was not anticipated in the planning.
- **Video player branches:** pause, play and mute are too intertwined for separate PRs, so this work doesn't match the GitHub breakdown and will end up as one large final branch (smaller than the stream bridge).

## Action Items for Improvement

- **Axel:** ad blocker PR next week, two weeks at most.
- **Axel:** next step for the ad blocker: Firefox-style checkboxes per category (e.g. cryptomining, trackers).
- **Corentin:** render thread and video Player, aiming to have video displaying by the next internal meeting.
- **Corentin:** look into a shared project memory for AI tooling (vector database via MCP servers) before the meeting with Lucas.
- **Corentin:** update the previous meeting notes with the missing points and write up this meeting.
- **Nathan:** test playback speed in the browser, then open the PR.
- **Thomas:** catch up on the devtools and keep tasks updated along the way.
- **Matteo:** bookmarks display first, then folder management. The scroll if he gets ahead.

## Other Topics Discussed

- **Ad blocker:** no per-site disabling for now; blocking stays global.
- **CSS:** redundant styles that cancel each other out, across our pages and Servo's, make rendering inconsistent depending on the menu. A shared style guide with reusable components would help, but the refactor is hard to scope and there's no time for it right now.
- **File upload and downloads:** Servo now uses the native system dialog for file uploads. Downloads and file saving are still not supported: not urgent, but users will ask for it.
- **Beta feedback:** some sites still struggle to render.
- **Legal structure:** Axel proposed registering Aether as an official organization to get code-signing certificates for Windows and macOS (Android still an open question).
- **Obscura:** a new headless browser built for AI agents was discussed.
