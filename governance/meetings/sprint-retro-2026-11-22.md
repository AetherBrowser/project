# Aether Sprint Retro Meeting

Date: 2026-11-22

Location: Teams

Attending:
  - corentin.bergaentzle@epitech.eu
  - nathan.callegari@epitech.eu
  - matteo.milin@epitech.eu
  - axel.battigelli@epitech.eu

Absent:
  - thomas.richalet@epitech.eu

## What Went Well

- **Sprint 5, caught up:** the tasks from the previous sprint were finished during this one, one sprint late.
  - AET-43: Filtering network with ablock
  - AET-46: Store bookmarks and persistance
- **Sprint 6:** its tasks were not done here. They were moved to the next sprint, sprint 7, as anticipated at the time.
- **Video:** the render thread is in place, so video should work and be testable soon. A stop button was added for video opened directly in the browser: it pauses playback and seeks back to the start. A test page is already ready for a first demo. Player creation, which previously handled audio only, now handles video as well through that render thread. The work is progressing in a good direction.
- **Bookmarks:** already in progress, with AET-46 finished. So far there is a bar under the address bar, everything is stored in SQLite, folders can be nested without a depth limit, and a bookmarks page lists them and lets you navigate. The work is split into 3 pull requests and tasks, still in draft because cargo-deny fails on main: a stack overflow in `url` 2.5.8 (`Url::origin()` on nested `blob:` URLs), not a failing test. That check should be fixed soon. 
- **Incident resilience:** Servo moved ahead while CI was down, and some tests started crashing. They were fixed in under 2 days. The delayed Servo merges were caught up and synced with our repository in under a week.

## What Didn't Work Well

- **Tasks:** everything is behind the plan. Tasks are either not started, or in progress and not finished.
- **Bookmarks:** the page was not written as a task, but it was useful to check that everything works.
- **CI:** Three separate issues:
  - Aether is a fork. This is a known GitHub issue: Actions are disabled after about a month of inactivity, and it also seems to happen every month even with activity. CI then needs a manual reactivation from the administrator.
  - Scheduled workflows (nightly releases, daily tests) no longer run on their own. The gap between the planned time and the actual start keeps growing, so they are launched manually.
  - On Wednesday 11 November, Ubuntu services were down for about 7 hours ([Canonical status](https://status.canonical.com/#/incident/KNms6QK9ewuzz-7xUsPsNylV20jEt5kyKsd8A-3ptQFX-3WclTLkuMGEkQ0cQPf-nRNYHaA8K7mU9EKLLx1dRw%3D%3D)). Linux CI could not initialize: images, updates, and related services were unavailable. Shortly after Ubuntu recovered, GitHub had an incident ([GitHub status](https://www.githubstatus.com/incidents/dvy0t3mvh1lg)): Actions jobs stayed queued without starting, so all CI was unusable.
  - Not a total blocker: Linux and Android builds are checked locally, Windows less often, but macOS can't be tested since nobody on the team has a Mac.
- **Storage:** major documents are on Microsoft 365 (SharePoint). SharePoint was also down for 2 days because a bug spread ([Microsoft 365 status](https://x.com/MSFT365Status/status/2121485746334777593?s=20)).

## Action Items for Improvement

- **Tasks:** make sure every task has the material and the description needed to complete the work more easily.
- **Fallback:** set up a GitLab mirror, so the project still has a remote if GitHub is unavailable.
- **Migration:** move every docx file to GitHub as Markdown. That gives us templates, an easy conversion, and a copy we can duplicate anywhere. It also makes it easy to see what changed between versions.
