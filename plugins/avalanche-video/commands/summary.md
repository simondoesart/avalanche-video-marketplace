---
description: Generate the project summary into project/summary.md (asks before overwriting or iterating)
---

Generate and save an auto-summary of the current make-video project. Steps:

1. **Locate the project.** Use the working folder established in Phase 0 of the make-video pipeline (`<working folder>/<project-slug>/`). If none exists in this session, ask the user to point to the project folder, then continue.
2. **Compose the summary** from the brief sheet (`project/brief.md`), continuity bible (`project/continuity.md`), notes (`project/notes.md`), and this session's history:
   - Project name, date, phase status (which phases locked/approved/pending).
   - The hook / creative strategy (verbatim) and how the concept answers it.
   - Intake/form answers: aspect, target length, platform, text plan, style register, model.
   - Script: current version, LOCKED or in-workshop, one-paragraph synopsis, count of workshop rounds.
   - Elements: table of @name → type → element_id → new/reused.
   - Shotlist + generation packing state.
   - Generation log: job IDs, models, credits spent, results kept vs rejected, files in `generations/`.
   - Context provided for the script (sources, references, anything pasted in).
   - Open questions and next steps.
3. **Check `project/`.** If `summary.md` (or the latest `summary-v{n}.md`) exists, ASK the user (AskUserQuestion): **overwrite** it, or write a **new iteration** (`summary-v{n+1}.md`)? Never silently overwrite. If none exists, write `summary.md` directly.
4. Write the file and confirm with the exact path written.
