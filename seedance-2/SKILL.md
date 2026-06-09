---
name: seedance-2
description: Write paste-ready Seedance 2.0 video prompts for realistic, commercial-grade clips — product ads, UGC/creator shorts, testimonials, social video, cinematic b-roll, and image-to-video animation. Use this whenever the user mentions Seedance, a Seedance prompt, a text-to-video or image-to-video prompt for a marketing/product/social clip, animating a still image into video, or asks why a generated clip looks plasticky, static, or glitchy. Trigger even when "Seedance" isn't said explicitly but the request is clearly a realistic AI video prompt for ad/product/social use. This is the TOOL skill for Seedance prompt grammar and realism — distinct from any cinematic-narrative filmmaking skill, which owns multi-scene story continuity.
---

# Seedance 2.0 — Prompting for Realistic Video

Hand the user a final prompt they can paste straight into Seedance 2.0. Default output is a clean code block, no preamble, no tutorial. If they want the reasoning, they'll ask.

Seedance 2.0 produces 2K video at 24fps with native audio-video sync (dual-channel stereo), supports up to 12 reference inputs, and handles text-to-video (T2V), image-to-video (I2V), reference-to-video (R2V), and video-to-video (V2V). It follows natural-language logic and rewards structure over adjective-stacking.

Before writing anything, check `references/user-findings.md` for project-specific notes — brand looks, product names, hooks that converted, aspect ratios per platform, things that diverge from the patterns below. User findings take precedence when they conflict with general guidance.

## Decide what's being asked for

| Request looks like… | Output type |
| --- | --- |
| "Prompt for a product reveal / ad clip…" | Single-shot product prompt (orbit/push-in) |
| "UGC clip of someone using / holding…" | Vertical creator-short prompt |
| "Testimonial / talking-head clip…" | Talking-head prompt (one action, eye-level) |
| "B-roll / atmosphere / establishing shot…" | Single-shot cinematic prompt |
| "Animate this image / make this photo move" | Image-to-video prompt (motion only) |
| "A scene with cuts / multi-angle sequence" | Multi-shot prompt (one generation, 2–4 cuts) |
| "Why does my clip look plastic / static / glitchy?" | Troubleshooting — see table below |

When unsure, ask ONE question, then write the prompt. The default is to deliver, not to coach.

## The core structure

Seedance responds best to elements stated in this order. This single ordering is the highest-leverage thing in the whole skill:

```
[Shot type], [subject + concrete visual details], [one clear action], [environment + time of day], [camera movement], [lighting + direction], [visual style], [aspect ratio]
```

Every strong prompt answers five questions in order: **what is the shot, who/what is the subject, what moves, where, what style.** Most good prompts land at 35–80 words. Shorter works for simple animation; commercial and cinematic clips need the detail.

**Filled example:**
```
Close-up tracking shot, a ceramic coffee cup on a walnut desk, steam rising slowly while morning light moves across the surface, cozy apartment kitchen at sunrise, subtle dolly forward, soft golden window light from the right, realistic cinematic style, 16:9
```

Two non-negotiables for clean output:
- **One primary subject per generation.** Multiple equally-weighted subjects compete for the model's attention and produce inconsistency.
- **One visible action per shot.** Use a concrete present-tense verb: `steam rising`, `camera orbiting`, `fabric fluttering`, `pouring`, `walking slowly`.

## Making it look REAL (anti-plastic)

This is the whole job for RGMA work. Realism comes from three levers:

1. **Practical lighting with a stated direction.** Name the source and where it comes from: `soft window light from the left`, `hard side light`, `warm tungsten from overhead`, `neon reflections on wet pavement`. Vague "good lighting" or no lighting line produces flat, fake-looking results. Add `color temperature: warm` or `color temperature: cool` for a strong directional cue.
2. **The anti-plastic phrase.** If skin, product, or surfaces look too smooth or CGI, append `no 3D, no cartoon, no VFX`. This forces Seedance toward a photographed look instead of a rendered one.
3. **Concrete subject specificity.** Not "a businesswoman" → "a woman in her early 30s, dark navy blazer, hair in a loose bun, serious expression." Not "a perfume bottle" → "a glass perfume bottle with a gold cap, amber liquid, clean white surface." The model bakes in detail it's given and averages everything it isn't.

## Use-case templates (RGMA workhorses)

### Product ad
```
Studio product shot, [product with material + color], slow 180-degree camera orbit, small highlights moving across the surface, clean [surface] background, premium softbox lighting, crisp commercial style, no text, no logo distortion, 16:9
```
Keep the background simple so the model spends detail on the object, reflections, and motion.

### UGC / creator short
```
Vertical medium close-up, [creator] holding [product] toward the camera, quick confident gesture, subtle handheld camera energy, bright room with natural window light, energetic social-media product-demo style, no warped hands, 9:16
```
The load-bearing parts: vertical framing, ONE visible action, a clear object interaction. Handheld energy reads as authentic; over-stabilized reads as stock.

### Testimonial / talking head
```
Static medium shot, [person] speaking to camera with a small natural nod and breath before the line, relaxed posture, [room] background softly out of focus, soft key light from the left with gentle fill, realistic skin texture, documentary style, 9:16
```
For dialogue audio, transcribe tricky brand/product names phonetically inline and keep the real spelling in parentheses.

### Cinematic b-roll
```
Wide cinematic shot, [subject] moving through [location], slow tracking camera, atmosphere in the background, golden hour lighting, realistic film color, shallow depth of field, 16:9
```
If the first output is too busy, strip background details before touching the subject.

### Image-to-video (animate a still)
```
Animate this image with [one motion: slow push-in / gentle hair movement / steam rising], natural micro-movement, soft cinematic lighting, realistic motion, no camera shake, no identity change, no background change, no extra objects, no text distortion
```
**Do not redescribe the subject.** The uploaded image already defines it. Redescribing causes identity and background drift. Describe only motion, camera, and light shift. This is the cleanest path to consistency — and it pairs directly with first frames built in the `chatgpt-image-2` skill.

## Multi-shot (cuts in one generation)

Use when a sequence needs 2–4 angles that share lighting and blocking. State the structure at the very top — **shot count, total duration, aspect ratio** — then script each cut.

```
[Style/look], [N] shots, [total] seconds, [aspect ratio].
[Establishing context: location, lighting, characters present, palette.]

Cut 1 — [wide or medium establishing angle, subject, action]
Cut 2 — [angle, subject, action]
Cut 3 — [angle, subject, action]

Keep lighting and wardrobe consistent across all cuts.
```

Always open Cut 1 with a wide or medium establishing shot so the model locks positions before any close-up. If Cut 1 is a close-up, the model has no anchor for where everything is and subjects teleport between cuts.

## References, text overlays, aspect ratios

- **References:** be explicit about what to pull — `use the composition from Image 1`, `follow the action from Video 2`, `match the product in Image 1 exactly`. The model extracts core features and combines them with the text.
- **Text overlays:** supported across T2V/I2V/R2V/V2V. Specify the exact string, color, style, timing, and position. Use common characters; rare glyphs render unreliably.
- **Aspect ratios:** `16:9` (YouTube, web hero), `9:16` (Reels/Shorts/TikTok/UGC), `1:1` (feed), `2.35:1` (cinematic). Favor close-up and medium shots for vertical; wides read better in 16:9.

## Iteration discipline

- **First prompt rarely lands.** Change ONE variable at a time — camera move, lighting, OR subject detail, never all three — so you learn what actually moved the output. This is also the fastest way to build the findings file.
- **Reuse what worked.** If a lighting setup or style line produced a good clip, keep it verbatim for the next generation. Consistency across a sequence comes from holding subject description + lighting character + style constant and changing only shot type and action.
- **Shorter often beats longer.** A crisp 4–5s clip usually outperforms a stretched 10s one. Failed clips aren't waste — two good seconds are still two usable seconds; note the timecode and harvest.
- **Save every prompt that produced a usable clip** into `references/user-findings.md`, with aspect ratio and source-image type. That library beats any generic example list.

## Common Seedance issues — quick fixes

| Issue | Likely cause | Fix |
| --- | --- | --- |
| Nothing moves / too static | No motion description | Add a concrete action verb + subtle camera drift |
| Skin/product looks plastic or CGI | Smoothing + no light direction | Append `no 3D, no cartoon, no VFX`; name a practical light source and its direction |
| Subject doesn't match description | Prompt too abstract or conflicting | Replace adjectives with concrete visual detail (color, material, age, wardrobe) |
| Lighting looks flat | No lighting line | Specify source + quality + direction; add color temperature |
| Looks low-quality on Seedance 2.0 | Short, thin prompt | Use the full 8-part structure; 35–80 words |
| Subjects inconsistent across frames | Too many competing elements | One primary subject; simplify background and props |
| Characters teleport between cuts | No establishing shot in a multi-shot | Open Cut 1 with a wide/medium frame |
| Identity/background drifts in I2V | Redescribing the source image | Describe motion only; add `no identity change, no background change` |
| Complex camera move falls apart | Multiple simultaneous moves | One camera move per shot; avoid "rotate + zoom + subject runs at camera" |

## Output format

Default: one clean, paste-ready prompt in a code block. No "here's your prompt." When producing multiple artifacts in one response, separate with headers so each block can be grabbed independently:

```
## Product prompt — [product]
[paste-ready prompt]

## UGC short — [concept]
[paste-ready prompt]
```
