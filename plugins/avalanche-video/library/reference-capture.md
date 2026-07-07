# Reference Capture — the workshop (runs inside Phase 4)

References define the film. Stock-feeling references produce stock-feeling video — this workshop exists to make every character, prop, and location still feel photographed, specific, and ours.

## Step 1 — Element interview (structured, never a fragile form)

Work through the confirmed element-needs map one element at a time, using AskUserQuestion batches for choices and chat for prose (never custom form widgets). Capture enough specificity that the still can't come back generic:

- **Character:** age range · build · hair · one distinguishing feature · wardrobe in exact words (this sentence becomes the bible's locked phrasing) · demeanor/energy · context they belong to. Invented faces only — never a real person's likeness.
- **Location:** what it is · time of day + light quality · condition (lived-in, worn, cluttered, pristine?) · 2–3 objects that make it specific · staging notes (where action happens).
- **Prop:** exact shape/material/finish · scale cues · signs of use/wear · how it's held or sits in the scene.

Answers land in the continuity bible (§2–4) as locked phrasing before any prompt is written.

## Step 2 — Reference prompts (canonical paragraph form, shown before any spend)

One prompt per still, written as flowing paragraphs — subject (locked phrasing verbatim), then context/staging, then LOOK, then framing, then AVOID:

- **LOOK:** always the film base — *"Shot on 35mm film, gentle film grain, soft halation, documentary realism, photographed not rendered, no oversaturation"* — plus the chosen register's grade. Reference stills obey the same capture DNA as the video.
- **Framing defaults:** character → eye-level 3/4 medium, candid neutral expression, in their context (not a void); location → establishing wide at the staging height; prop → clean three-quarter close-up in situ, natural light.
- **AVOID (anti-stock set, always appended to the global negatives):** *no stock-photography look, no studio seamless backdrop, no posed smile at camera, no corporate gloss, no perfect symmetry, no pristine showroom feel — lived-in, specific, imperfect.*

Show the full set of prompts for review and approval. Image generations cost credits: preflight and confirm like any other spend.

## Step 3 — Generate & review (`generate_image` → `nano_banana_2` / NanoBanana Pro)

Generate the approved set. Review as a batch against the bible: identity + wardrobe verbatim? Register grade present? Anything reading "stock"? Iterate only the failing stills — one targeted fix per round.

## Step 4 — Lock → register → download (automatic once the editor locks the set)

For every locked still, without being asked:
1. **Download it into `<project>/references/`** named `@name_ref-v{n}.png` (fetch the result URL; if a direct download isn't possible, link the still and have the editor save it there from the widget before proceeding).
2. **Register it as a Higgsfield reference element** — element name = the @name exactly.
3. **Record** @name → element_id in the continuity bible §1 and `library/reference-assets.md`.

No prompt composition (Phase 6) starts until every mapped element is locked, registered, and downloaded.

## Step 5 — Attachment routing (how references reach the video model)

| Video model | How references attach |
|-------------|----------------------|
| `seedance_2_0` / `seedance_2_0_mini` | Embed `<<<element_id>>>` in the prompt (multiple per shot). Hero props: dual-pass — embed AND explicit `medias` image-reference. |
| `kling3_0`, `cinematic_studio_3_0` | Elements embeddable via `<<<element_id>>>` too — same as seedance. |
| `veo3_1`, `veo3_1_lite`, other start-frame-only models | No element embedding: choose the strongest reference still (or a generated first frame built FROM the references) as `start_image` / `end_image`. Note which @ref anchors which generation in the shotlist. |
| `higgsfield_preset` | Requires exactly one image — the reference still. |

Record the chosen routing per generation in the brief sheet so the prompt's FORMAT line and the submit call always agree.

## Step 6 — Continuity across generations: frame-pull, never video-chaining

**Hard rule: never feed a generated video back into the next generation as a video reference.** Chaining generations compounds artifacts — each hop inherits the last one's noise and quality degrades in a feedback loop.

- **Identity continuity** comes from the SAME original locked reference stills (the registered elements), attached fresh to every generation. G5 uses the identical @woman element that G1 used — never "the @woman from G4's output."
- **Compositional continuity** (G2 must open where G1 ended — same position, same light) uses a **frame pull**:
  1. The G1 video is already downloaded in `generations/` (Phase 8). Extract the exact frame locally with ffmpeg — e.g. last frame: `ffmpeg -sseof -0.1 -i G1.mp4 -frames:v 1 out.png`, or a chosen timestamp: `ffmpeg -ss 00:00:07.5 -i G1.mp4 -frames:v 1 out.png`. Offer the editor 2–3 candidate frames around the target moment and let them pick.
  2. Save the chosen frame to `references/` as `@scene_G1-frame-{t}s.png`.
  3. Upload it (`media_upload` → `media_confirm`) and attach it to the next generation as **`start_image` only** — never as an identity/image reference and never register it as an element.
- A pulled frame anchors ONE generation and is then retired. If its quality is already compromised, fix G1 first instead of propagating it.
