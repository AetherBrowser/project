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
  - AET-67: Pause a video (not started, will be done within the next 3 weeks, including seeking while paused)
  - AET-76: Play common videos formats (not started)
Nathan:
  - AET-52: Play an audio (finished)
  - AET-55: Mute and unmute an audio (finished)
  - AET-56: Adjust volume's audio (finished)
  - AET-66: Play a video (in progress)
  - AET-68: Stop a video (not started)
  - AET-69: Adjust volume's video (not started)
  - AET-70: Mute and unmute a video (not started)
Mattéo:
  - AET-20: Store url and metadata to have a history (finished)
  - AET-47: Clear history after a delay (finished)
  - AET-33: Bookmark button to mark a page (finished)
  - AET-46: Store bookmarks and persistance (finished)
  - AET-34: List of bookmarks (in progress: first version with folders, should be finished within a few days)
Thomas:
  - AET-40: Dev tools console in read mode (not started because it's not track, errors displayed directly in the browser)
  - AET-41: Dev tools network (not started)
Axel:
  - AET-43: Filtering network with ablock (finished)
  - AET-44: Configure adblock lists (not started)

### Outside the sprint
Some work was done about these tasks but nothing is track
Thomas:
  - AET-42: Dev tools inspector
  - AET-41: Dev tools network
  - AET-45: Dev tools storage
  - AET-103: Dev tools performance
  - Dev tools resizing and docking on the right side

## Remark
  - Blocker: CI. Three separate issues:
    - Aether is a fork. This is a known GitHub issue: Actions are disabled after about a month of inactivity, and it also seems to happen every month even with activity. CI then needs a manual reactivation from the administrator.
    - Scheduled workflows (nightly releases, daily tests) no longer run on their own. The gap between the planned time and the actual start keeps growing, so they are launched manually.
    - On Wednesday 11 November, Ubuntu services were down for about 7 hours ([Canonical status](https://status.canonical.com/#/incident/KNms6QK9ewuzz-7xUsPsNylV20jEt5kyKsd8A-3ptQFX-3WclTLkuMGEkQ0cQPf-nRNYHaA8K7mU9EKLLx1dRw%3D%3D)). Linux CI could not initialize: images, updates, and related services were unavailable. Shortly after Ubuntu recovered, GitHub had an incident ([GitHub status](https://www.githubstatus.com/incidents/dvy0t3mvh1lg)): Actions jobs stayed queued without starting, so all CI was unusable.
    - Not a total blocker: Linux and Android builds are checked locally, Windows less often, but macOS can't be tested since nobody on the team has a Mac.
  - Keep documenting what is set up (tech watch, automation, CVE tracking, architecture, ...) as it is set up, and record what changes over time.
  - Architecture document is hard to follow for new people on the project. The class diagram can't be read as is, detailed parts are hard to locate in the global architecture, and some links are outdated.
  - Performance: set up a reproducible test protocol. Identify something that does not perform well enough, measure it, improve it step by step, and use the protocol to show the improvement.

## Objectives
Technology Monitoring & Hard Problem:
  - OpenGL will be used as the rendering engine. The first version relies only on libmpv, which renders on the CPU only.
  - Obscura, a browser built from scratch by AI and for AI, was looked at. It is also written in Rust, and is reported to have more security flaws, slowdowns, and memory leaks. Not really relevant for us.
  - Security updates take a lot of time. cargo-deny runs on every CI run and blocks merges when a dependency fails its checks: known CVEs, unmaintained packages, and identified issues such as buffer overflows. This process is not documented yet.
Architecture & Reliability:
  - The schema is published in the project book (Design > Documentation > Architecture). It was not finished yet when it was published.
  - Evolutions worth documenting: the video module moving from MPV-only rendering to OpenGL, and the SQLite schema changes for bookmarks. Everything else is mostly new features added on top of the existing architecture.
Open Source:
  - No change apart from the CI issues. Release discussions are updated with a new message for each release.
  - Communication to attract contributors is planned once the project is more functional, likely in December.
  - The label for beginner-friendly issues exists, but few issues, if any, have been selected for it.
Measure, Test & Optimize:
  - WPT tests are already in place, but they still need some documentation.
  - Comparisons were done a few months ago: other browsers against Servo, then with an early MPV integration.
  - Main benchmarks once the MPV integration is complete (expected around mid-December): GStreamer against MPV, then with OpenGL. It is too early to choose the improvement target; audio and video are the most likely candidates.
  - Performance objectives have been mentioned and written down, but they are not detailed or quantified yet.
