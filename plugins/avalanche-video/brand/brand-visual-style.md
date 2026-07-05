# Avalanche — Brand Visual Style (Video) · v3

> Single source of truth for how Avalanche videos look, move, and sound.
> Derived from the official **Avalanche Brand Guidelines (June 2026)** — "Technology built for business."
> Every generation reads from this file. Edit here → every future video changes.

---

## 1. Essence

**Avalanche exists to put the world's most powerful technology to use.** Built for real businesses solving real problems at scale — reliability, performance, outcomes. Not experimentation, not speculation.

Two visual narratives drive everything:

- **MOMENTUM** — the unstoppable horizontal energy of an avalanche: motion blur, horizontal reveals, cascading blocks, easing curves that hit hard and settle.
- **ELEMENTAL** — an avalanche is a force of nature: snow, ice, frost, wind, and mountains referenced constantly, juxtaposed with the familiar world of banking, finance, and business.

Three words to hold on every shot: **Momentum. Elemental. Real.**

> **There is no default look.** This file is a menu, not a preset: the visual style — register, grade, palette emphasis — is decided *during* the make-video flow (Phase 3), with the editor. Do not assert or summarize a "house look" at intake, and never quote a register's traits (blue-grey snow, Avalanche IRL, red accents) before that register has been chosen.

## 2. Capture DNA (locked — how everything is shot)

The only truly global rule. All filmed/photographic material keeps the film base, whatever the register:

> Shot on 35mm film, gentle film grain, soft halation, documentary realism, photographed not rendered, no oversaturation.

**Grade belongs to the chosen register** (see §6) — e.g. cool blue-grey for snow/VFX and Avalanche IRL work, naturalistic warmth for intimate human-documentary. Never glossy, never plasticky CGI.

## 3. Audio (locked)

> Audio: diegetic only, no music, no score.

The brand embraces **audio of wind, ice, an avalanche — visual and audio ASMR.** Room tone, weather, machines, breath. Score only when a brief explicitly asks. No lip-synced or discernible dialogue unless intended. Assume muted-autoplay: the story must land silent.

## 4. The avoid list (locked — the "de-creep" rulebook)

Ships verbatim in every prompt's **AVOID** section (full tiers in `library/global-negatives.md`):

> Avoid: any facial mesh or wireframe on the face, cyan or green tech-HUD overlays, extreme eye close-ups, dot-grid scan animations, red reticles or target-locks on the face, cold clinical lab settings, surveillance or "system watching you" POV, on-screen text or UI, oversaturation, glossy plasticky CGI.

Technology in Avalanche stories is powerful but human-scaled and matter-of-fact — never surveillance-coded, never a system watching a person.

## 5. Color (2026 brand palette)

Dark mode is the default: background **#1F1F1F**. Light mode uses **#EBF0FA**.

**Red — the brand color** (a spotlight, not wallpaper; one decisive red moment per composition):

| Role | Hex |
|------|-----|
| Avalanche Red (primary) | `#E6212F` |
| Red dark ramp | `#B20F2A` · `#820419` · `#3D000A` |
| Red light ramp | `#FF394A` · `#FF7F7B` · `#FEAFAC` |

> ⚠️ **`#E84142` is the retired pre-2026 brand red.** It must never appear in a prompt, palette, or generated asset. If it surfaces anywhere (old templates, cached elements, muscle memory), replace with `#E6212F`.

**Neutrals & darks:**

| Role | Hex |
|------|-----|
| Dark-mode background | `#1F1F1F` |
| Dark ramp | `#16261C` · `#121212` · `#000000` |
| Slate / steel | `#3B484B` · `#A2AFB2` |
| Light-mode surface | `#EBF0FA` |

**Blue — secondary family** (data, UI, institutional cool; supports, never competes with red):

| Role | Hex |
|------|-----|
| Primary blue | `#0061E2` |
| Blue dark ramp | `#0E4DA0` · `#0C3F83` · `#05295B` |
| Blue light ramp | `#3176D3` · `#749DD3` · `#C5CFF5` |

**Rules:** snow carries the cool blue-grey cast (never pure white, never warm); red is the single brand accent; no rainbow gradients, no neon-purple crypto cliché, no gold coins, no oversaturation.

## 6. Imagery registers (from the guidelines — pick one per shot/sequence)

1. **Avalanche IRL** — a very specific, deliberate look: Avalanche snow taking over familiar business locations (offices, trading floors, filing cabinets, coffee stations), people completely unfazed. Conveys momentum and hidden power in real-world systems. Cool blue-grey grade. **Reference it only when this register is explicitly chosen for the video — never as ambient default context.**
2. **Natural elements** — closeups and establishing shots of snow, ice, frost, wind, drifts, avalanches, cliffs, rocks, mountains. Juxtaposes the natural and tech worlds.
3. **Motion blur** — long-exposure energy on cities, crowds, hands, infrastructure; momentum made visible. In-camera or post.
4. **Juxtaposition** — diptychs pairing finance/technology imagery with powerful avalanche/snow imagery (payment terminal | snow blast; NYSE facade | powder wave).
5. **Architectural sublime** — closeups of institutional architecture and familiar finance environments; trust, scale, steel-and-stone; near-monochrome.

## 7. Motion language

- **Horizontal momentum:** reveals, wipes, and camera moves travel horizontally — the avalanche direction. Cascading-block energy.
- **Easing with impact:** fast attack, decisive settle (the guidelines' easing curves) — motion hits, then stills.
- **Fast-paced but grounded:** cut rhythm carries energy (~2.5–3s per shot); each shot one clear idea; movement motivated by story.
- Subtle handheld for human beats; controlled/locked moves for institutional and graphic beats.
- Avoid: whip-chaos, dance/meme energy, random drift, slow-motion glamour unless briefed.

## 8. Composition

- **Horizontal layouts** on a clean, orderly grid (the brand uses a 12-column / 6-row grid, 1px vertical rules) — break the grid only for deliberate impact.
- Vertical measurement/rule lines as compositional devices (in design/post — not AI-generated on frame).
- Generous negative space; subjects placed with grid logic; depth in layers.
- Aspect: 16:9 hero · 9:16 social · 1:1 feed · 21:9 epic.

## 9. Typography on frame

Brand typefaces: **Aeonik** (Black, all-caps = primary headline; Regular = subhead/body), **Aeonik Fono** (eyebrows, captions, numbers, data), **Inter** as substitute. Headlines are big, bold, confident, often interleaved with imagery.

Default in generation: **no on-frame text** (it's in the avoid list — AI type garbles). Text overlays are set in the edit/post using the brand type; plan overlay timing in the script and leave clean compositional room.

## 10. Graphic assets (for motion-graphic work)

- **Digital blocks:** cascading horizontal rectangles in Avalanche Red `#E6212F` and slate `#A2AFB2` on `#1F1F1F`, stepping across the grid — representing data, the blockchain, consensus, a digitized avalanche. The signature graphic pattern.
- Logo: logomark (red triangle mark) + logotype; KO/white on dark, red, black on light; maintain safe space; never distort. `@avalanche-logo` element.
- Keyable assets follow the motion-graphic spec in `library/video-types.md`.

## 11. Do / Don't cheat-sheet

**Do (always):** 35mm film texture · photographed not rendered · diegetic sound only · movement motivated by story · red used as `#E6212F` when red appears at all.

**Do (when the chosen register calls for it):** cool blue-grey snow (snow/VFX/IRL registers — snow never pure white) · people unfazed by the avalanche (IRL only) · horizontal momentum · motion blur energy · juxtaposition diptychs · institutional architecture.

**Don't:** facial mesh/HUD/reticles/eye-macro (de-creep) · `#E84142` (retired red) · on-screen text or UI in generation · oversaturation · glossy plasticky CGI · garbled signage · third-party logos · music/score unless briefed · rainbow gradients · crypto clichés · crowd sameness · asserting a look before the register is chosen.

---

## 12. Growing this file

When a generation nails the look, save its job ID + exact prompt as a template in `library/scene-shot-templates.md` and note here what made it work.
