# Aether Sprint Planning Meeting

Date: 2026-11-07

Location: Teams

Attending:
  - corentin.bergaentzle@epitech.eu
  - nathan.callegari@epitech.eu
  - matteo.milin@epitech.eu
  - thomas.richalet@epitech.eu
  - axel.battigelli@epitech.eu

## Agenda:
  - Confirme 6 and 7 and assigned tasks for each member if needed
  - Check if something is urgent or bugs founds and needs a fix
  - New tasks to read and add :
    - #186 : download a file from a url, it will be the base for the downloads in general
    - As Mattéo said, improve the scroll, but it a low priority, just defined it today

## What's Done

- **Sprints 6 and 7:** confirmed as planned on 7 Nov. Assignments stay as they are; nobody needs extra tasks. Both sprints remain on track. But Mattéo ask for the case of he have finished all what was planned (see scroll).
- **Urgent work and bugs:** nothing new to pull into the sprint. Bugs reported by beta testers, including YouTube failing to load after a header went over the 16 KB limit, are already fixed. Devtools is behind, but that stays catch-up on the existing tasks, not a new fix.
- **#186 (download a file from a URL):** read and kept as the base for downloads in general. Servo already uses the native system dialog for uploads; downloads and saving a file are still missing. Not urgent, so it is not added to sprint 6 or 7. Users will ask for it later.
- **Scroll:** defined today, as Mattéo asked. Medium priority only; Mattéo is assigned and it does not enter the current sprints. It only for when he have time.

- **Ad blocker:** no way to turn it off for a single site for now. Blocking stays global.
- **CSS:** some styles cancel each other out, on our pages and in Servo, so rendering changes with the menu. A shared style guide and reusable components would help. The refactor is hard to scope, and there is no time for it in this sprint.
- **File upload and downloads:** Servo now opens the native system dialog for uploads. Downloads and saving a file are still missing. Same conclusion as #186: not urgent, but users will ask for it.
- **Legal structure:** Axel proposed registering Aether as an official organization so we can get code-signing certificates for Windows and macOS. Android is still an open question.
