# Aether External Mentoring Meeting

Date: 2026-11-12

Location: Teams

Attending:
  - corentin.bergaentzle@epitech.eu
  - nathan.callegari@epitech.eu
  - matteo.milin@epitech.eu
  - thomas.richalet@epitech.eu
  - axel.battigelli@epitech.eu
  - jean-philippe.roze@epitech.eu

## Work presentation
Corentin:
  - AET-52: Play an audio (finished)
  - AET-53: Pause an audio (finished)
  - AET-54: Stop an audio (finished)
  - AET-66: Play a video (in progress: setting up the MPV rendering context, video display expected within the next 2 weeks)
  - AET-67: Pause a video (to do within the next 3 weeks, including seeking while paused)
Nathan:
  - AET-52: Play an audio (finished)
  - AET-55: Mute and unmute an audio (finished)
  - AET-56: Adjust volume's audio (finished)
  - AET-66: Play a video (in progress)
  - AET-74: Change playback speed of a video (worked on: speed x0.5, x1, x2; issue still open)
  - Resizing the render to the video size (to do, to be confirmed)
  - End of video: videos currently don't restart automatically (to do)
  - Stopping and restarting the video (to do)
Mattéo:
  - AET-20: Store url and metadata to have a history (finished, merged into main)
  - AET-47: Clear history after a delay (finished, merged into main)
  - AET-33: Bookmark button to mark a page (finished)
  - AET-46: Store bookmarks and persistance (finished)
  - AET-34: List of bookmarks (in progress: first version with folders, should be finished within a few days)
  - Scroll improvement (to do)
Thomas:
  - AET-40: Dev tools console in read mode (working, issue still open: errors displayed directly in the browser)
  - AET-42: Dev tools inspector (issue still open)
  - AET-41: Dev tools network (issue still open)
  - AET-45: Dev tools storage (issue still open)
  - AET-103: Dev tools performance (issue still open: optimizations, and a fix for the dev tools disrupting the page display)
  - Dev tools resizing and docking on the right side (to do)
  - Other dev tools tabs (to do)
Axel:
  - AET-43: Filtering network with ablock (finished: sites to block entered manually)
  - Next step: community-maintained blocklists such as EasyList

## Remark
  - Blocker: CI. An Ubuntu outage of about 7 hours prevented CI from initializing. Then GitHub Actions jobs stayed queued without starting, and scheduled workflows (nightly releases, daily tests) no longer run, so they are launched manually. This is a known GitHub issue affecting forked repositories. Not a total blocker: Windows and Linux builds are checked locally, but macOS can't be tested since nobody on the team has a Mac.
  - Everything set up (tech watch, automation, CVE tracking) must be documented as it is set up.
  - Architecture document: hard to follow. The class diagram can't be read as is, detailed parts are hard to locate in the global architecture, and some links are outdated. Jean-Philippe Roze also questioned the name "process sampler".
  - The EIP expects documented architecture evolutions (what changed, why, in which context).
  - Performance track: the school expects identifying something that doesn't work well enough, measuring it, improving it step by step and proving the improvement with a reproducible test protocol.
  - Requested for the next meeting: a description of our performance objectives, and a description of the CVE tracking process.

## Objectives
Mandatory objective 1:
  - OpenGL will be used as the rendering engine. The first version relies only on libmpv, which renders on the CPU only.
  - A new browser built entirely by AI was looked at: rebuilt from scratch, also in Rust, and reported to have more security flaws, slowdowns and memory leaks. Not really relevant for us.
  - Security updates take a lot of time. CVEs are tracked with cargo-deny, which runs on every CI run and blocks merges when a dependency has a known CVE. Not documented yet.
Mandatory objective 2 (architecture):
  - The schema is published in the project book (Design > Documentation > Architecture). It was not finished yet when it was published.
  - Candidate evolutions to document: the video module moving from MPV-only rendering to OpenGL, and SQLite schema changes for bookmarks.
Complementary objective 1 (performance tests):
  - WPT tests are already in place.
  - Comparisons were done a few months ago: other browsers vs Servo, then with an early MPV integration.
  - Main benchmarks once the MPV integration is complete (expected around mid-December): GStreamer vs MPV, then with OpenGL. Too early to choose the improvement target, most likely audio/video.
  - Performance objectives to be documented.
Complementary objective 2 (open source):
  - No change apart from the CI issues.
  - Communication to attract contributors once the project is more functional, likely in December.
  - The label for beginner-friendly issues exists; the issues still have to be selected.

## Next meeting
December 3, 2026, 2:00 PM
