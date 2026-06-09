---
name: chatgpt-image-2
description: Write paste-ready ChatGPT Images 2.0 (GPT Image 2) prompts for realistic, production-ready images — product ads, posters and social graphics with exact text, infographics, UI mockups, character/reference sheets, image edits, and cinematic first frames for image-to-video. Use this whenever the user mentions ChatGPT Image 2, GPT Image 2, ChatGPT Images 2.0, an image prompt for a poster/ad/product/mockup/infographic, editing or restyling an existing image, locking text inside an image, or generating a still that will later be animated. Trigger even when the model name isn't said explicitly but the request is clearly a structured/realistic image-generation prompt for marketing or product work.
---

# ChatGPT Images 2.0 (GPT Image 2) — Prompting for Realistic Images

Hand the user a final prompt they can paste straight into ChatGPT Images 2.0. Default output is a clean code block, no preamble. If they want reasoning, they'll ask.

GPT Image 2 (OpenAI, released April 2026; succeeds GPT Image 1.5) is integrated into GPT-4o with reasoning in the generation step, and knowledge through December 2025. Its real edge is **structured visual work**: readable in-image text, clean layouts, product-ready compositions, world-aware photorealism, and editable reference images. It rewards a production brief, not a keyword chain.

Before writing, check `references/user-findings.md` for project-specific notes — brand palettes, recurring product specs, layouts that worked. User findings take precedence over the general patterns below.

## Decide what's being asked for

| Request looks like… | Output type |
| --- | --- |
| "Product ad / hero shot / campaign visual" | Product/ad prompt (job + layout + lighting) |
| "Poster / social graphic with text on it" | Exact-text poster prompt (text as locked asset) |
| "Infographic / diagram / explainer" | Infographic prompt (labels + hierarchy) |
| "App screen / dashboard / UI mockup" | UI mockup prompt (shipped-interface language) |
| "Character / reference sheet" | Character-sheet prompt (turnaround + palette) |
| "Edit / restyle / swap something in this image" | Edit prompt (change / preserve / match) |
| "A still I'll turn into video" | Video-ready first-frame prompt (depth + motion cue) |
| Photorealistic scene / portrait / lifestyle | Photoreal prompt (camera + light + texture) |

When unsure, ask ONE question, then write the prompt.

## The core structure

The most reliable pattern — name the job first, because GPT Image 2 follows the brief better when it knows how the image will be judged:

```
Create [type of image] for [use case].
Main subject: [specific subject + visible details].
Exact text, if any: "[copy that must appear]".
Composition: [framing, layout, subject placement, negative space].
Style and lighting: [visual language, medium, mood, light type + direction].
Constraints: [what must not change, no extra words, no watermark].
Output format: [aspect ratio; transparent background or video-ready frame if relevant].
```

You won't fill every line every time, but `job → subject → text → composition → style → constraints → format` is the order that works.

## The five skills that matter

### 1. Name the job before the style
Lead with the output type — product ad, poster, app screen, infographic, edit, first frame. `A cool futuristic speaker, cinematic, high detail` gives the model nothing to optimize toward. `Create a premium product ad for a matte black speaker, 16:9 banner, product on the right, headline left, clean negative space, sharp edges` tells it the success standard.

### 2. Treat text as a locked asset
This is GPT Image 2's signature strength — use it deliberately. Put exact copy in quotation marks, name the role of each block, and constrain against invention:
```
Headline: "SOUND YOU CAN FEEL". Render verbatim. Bold white sans-serif, left of composition, readable from a distance. No extra words, no duplicate text, no fake logo.
```
Put each line of copy on its own line in the prompt. If it misspells, regenerate with less text, larger type, and stricter `exact text only` language. Don't ask for "a slogan" unless you want the model to write one.

### 3. Give it a camera and a layout
State composition explicitly: camera distance, angle, subject placement, negative space, aspect ratio.
- `Close-up` — product texture, hands, faces, labels, materials
- `Wide shot` — environments, story scenes, video-ready frames
- `Top-down` — food, flat-lays, desk scenes, packaging kits
- `Left third / right third` — ad layouts balancing product and text
- `Clean grid` — UI mockups, character sheets, diagrams, infographics

### 4. Write edits in three sentences
Separate the change, the locked elements, and the physical match. This is far stronger than "make it better":
```
Replace the parked car with a vintage bicycle.
Preserve the house, fence, driveway, landscaping, lighting direction, camera angle, and time of day exactly.
Match the bicycle's scale, contact shadow, and perspective to the existing scene.
```
For multi-reference edits, label each image by role: `Image 1 is the product, Image 2 is the background style` — then state what transfers and what stays locked. GPT Image 2 holds identity well (face-preserving reference lock), so name the face/product as a thing to preserve.

### 5. Add motion cues for video-ready first frames
When the still will be animated (e.g. handed to the `seedance-2` skill for image-to-video), prompt for depth and motion-readiness: clear foreground / midground / background, a clean subject silhouette, and ONE visible motion cue — dust, fabric, hair, rain, reflection, steam, a rotating product, or a camera push path.
```
A cinematic first frame for an image-to-video clip: [subject] at [setting], [element] ready to move in the wind, strong foreground silhouette, clear depth layers, [light] horizon light, no text, no watermark. 16:9.
```

## Making it look REAL (photorealism)

Realism comes from describing **what a camera would actually see**, not from quality adjectives. Drop `beautiful`, `professional atmosphere`, `high quality`, `8K` — they add nothing. Instead specify:

- **Lens & framing:** `50mm documentary feel`, `shallow depth of field`, `eye-level`, `macro`
- **Light type + direction:** `soft natural daylight from the left`, `warm tungsten fill from overhead pendants`, `gentle shadows on the right side of the face` — name two sources and their directions when you can
- **Time of day & environment:** `blue hour`, `after rain`, `wet pavement reflections`
- **Texture & wear:** `visible dust`, `tiny scratches on the case`, `realistic skin texture`, `worn wood`
- **Ordinary background detail:** practical clutter reads as photographed; a clean void reads as rendered
- **Real-world anchors:** naming an era, film stock, or lighting type (`Kodak Portra palette`, `35mm grain`, `tungsten-vs-neon color mixing`) makes the model reason about physics — reflections, color mixing, grain — instead of averaging a generic look

To avoid the over-polished CGI look, add documentary details and `no glamour retouching`. Negative instructions (`no text`, `no watermark`, `no real brand logos`) work well — use them, but sparingly. Reference styles, not living artists (`in the style of ukiyo-e woodblock prints`, not a named contemporary artist).

## Use-case quick reference

- **Product ad:** name the product material/color, place it left-third or right-third, headline opposite, rim or softbox light, `sharp product edges, no fake logo`. For cutouts: `transparent background, crisp silhouette, no halos, no fringing, preserve geometry and label text`.
- **Poster / social text:** off-white or single-color ground, generous negative space, quote every string, name each text block's role, `exact text only`.
- **Infographic:** title in quotes, list the exact labels, `flat editorial icons, arrows between steps, readable sans-serif labels, consistent spacing`. Fewer labels = more legible; reduce and regenerate if dense.
- **UI mockup:** describe it as a shipped interface — `left sidebar, KPI cards, line chart, table, readable labels, realistic spacing` — not concept art. Put it `inside a phone frame, shown straight-on` for mobile.
- **Character sheet:** `front / side / back turnaround, expression row, costume callouts, color palette swatches, clean white background, consistent face and outfit across views`.

## Aspect ratios

`1:1` (feed, e-commerce), `4:5` and `2:3` (vertical social, book/poster), `9:16` (Stories/Reels, phone UI), `16:9` (banners, video-ready frames, dashboards), `3:2` and `4:3` (editorial, tablet UI). Always state one — a good square can fail as a vertical ad.

## Where GPT Image 2 struggles (plan around it)

Exact brand-logo reproduction, proprietary fonts, tiny legal/compliance copy, and high-volume draft batches. If the asset must carry a real logo, licensed typeface, or product label, generate the layout and **composite the real asset in afterward** rather than trusting the model to reproduce it.

## Iteration discipline

Start with the core scene, then refine ONE variable at a time. For text tasks, check spelling and label accuracy first — a beautiful image with wrong words is unusable. For edits, success means the locked elements stayed locked. Save prompts that worked into `references/user-findings.md`.

## Output format

Default: one clean, paste-ready prompt in a code block. No preamble. When producing multiple artifacts, separate with headers so each can be grabbed independently:

```
## Product ad — [product]
[paste-ready prompt]

## First frame for video — [scene]
[paste-ready prompt]
```
