---
description: Save the current script and exact canonical prompts to the project's script/ folder (asks before overwriting or iterating)
---

Save the current make-video project's writing artifacts. Steps:

1. **Locate the project.** Use the working folder established in Phase 0 of the make-video pipeline (`<working folder>/<project-slug>/`). If no working folder exists in this session, ask the user to point to the project folder (or run Phase 0 setup now), then continue.
2. **Assemble the content:**
   - `script-v{n}.md` — the current script: numbered beats with action + overlay/VO lines, the locked hook at the top, version number and status (LOCKED / in workshop), and a one-line change log versus the previous version.
   - `prompts-v{n}.md` — the exact canonical prompts, one block per generation, in the format from `library/prompt-format.md`: the human review view (@names) AND the submit view (`<<<element_id>>>`), each with its continuity-lint result and the FORMAT line (model, aspect, duration, shots).
3. **Check what exists in `script/`.** If saving would collide with existing files, ASK the user (AskUserQuestion): **overwrite** the current version files, or **new iteration** (bump to `script-v{n+1}.md` / `prompts-v{n+1}.md`)? Never silently overwrite. If nothing exists, write v1 directly.
4. Write the files and confirm with the exact paths written.
