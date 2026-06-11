---
name: real-video-2
description: Write paste-ready Seedance 2.0 prompts for believable realistic videos using one strict multi-line format with exact headers - Create, Subject, Action, Scene, Camera, Lighting, Motion realism, Audio, Voice - dialogue, Constraints, Output. Use for Seedance prompts, AI video, text-to-video, image-to-video, UGC, product videos, testimonials, talking-head videos, voiceover direction, dialogue direction, accents, lip-sync guidance, ambient sound, and fixing videos that look fake or overproduced.
---
# Seedance 2.0 Prompting Skill

Default output: return only one paste-ready Seedance prompt inside one `text` code block.

Do not include scenario setup, sample input, task summary, analysis, explanation, tutorial, skill execution notes, or extra commentary unless the user explicitly asks for reasoning.

The goal is to produce believable captured video, not overproduced AI clips. The best Seedance prompts use controlled simplicity: a locked source frame, one primary motion, practical lighting continuity, realistic audio direction, short dialogue only when needed, and failure-specific constraints.

## Required final answer format

Every final answer must be one code block using this exact structure:

```text
Create [specific realistic video type], [duration], [aspect ratio].

Subject:
[one primary subject with concrete visible details, or locked source-frame preservation for image-to-video]

Action:
[one clear physical action for short clips, or timestamped beats when the clip truly has multiple events]

Scene:
[real location, time of day, background details, or source-frame scene preservation]

Camera:
[shot size, angle, phone or lens feel, camera movement]

Lighting:
[practical light source, direction, color temperature, shadow continuity]

Motion realism:
[what moves, what stays stable, pacing, natural micro-movement]

Audio:
[ambient sound, room tone, foley, music only if requested or needed]

Voice / dialogue:
[language, subtle accent if needed, delivery, exact spoken line, lip-sync guidance, or None.]

Constraints:
[short list of likely failure points]

Output:
[duration], [aspect ratio].
```

The final prompt must always include every header shown above.

Use `Voice / dialogue: None.` when there is no speech.

Do not rename, remove, reorder, bracket, or combine headers.

Do not output a paragraph prompt.

Do not add any other sections.

A prompt fails this skill if it does not start with `Create`, does not include `Constraints:`, or does not end with `Output:`.

## Core rule

The secret key is controlled simplicity around a locked source frame.

Default to:

* one primary subject
* one primary action
* one motion layer
* one camera behavior
* one lighting setup
* one simple audio bed
* one short spoken line only when needed
* short, failure-specific constraints

Do not solve realism by adding more action, more camera movement, more dialogue, or more cinematic language.

## Image-to-video rule

For image-to-video, still use the same required structure.

Use the uploaded image as the locked source frame and include preservation instructions inside `Subject:` and `Constraints:`.

Do not create a separate image-to-video format.

Always treat the reference image as the source of truth, not as loose inspiration.

Strong `Subject:` language:

```text
The uploaded ChatGPT Image 2.0 image is the locked source frame. Preserve the same identity, facial structure, skin tone, hairstyle, wardrobe, accessories, product shape and label if present, background layout, lighting direction, shadow pattern, camera angle, lens feel, framing, and overall composition. Do not redesign the frame.
```

Strong `Action:` language:

```text
Animate only one requested motion: [slow push-in / slight handheld drift / blink once / subtle breathing / hair moving lightly / steam rising / small smile change / one product lift].
```

Strong `Constraints:` language:

```text
Do not redesign the frame. No identity drift, no face warp, no mouth distortion, no hand deformation, no product deformation, no label drift, no background melting, no lighting drift, no fake text. Animate only the requested motion.
```

## Realism goal

Prioritize:

* real camera behavior
* source-frame preservation
* practical lighting continuity
* natural movement
* believable audio direction
* grounded dialogue only when needed
* simple physical actions
* realistic skin texture
* one subject unless the user requests more
* one main action for 4 to 6 second clips
* timestamped beats only when the clip actually needs sequencing

Avoid overproduced AI-video language such as:

* cinematic masterpiece
* ultra realistic
* 4k
* 8k
* epic
* award-winning
* perfect lighting
* Hollywood quality
* insanely detailed
* flawless skin
* perfect

These often encourage plastic skin, fake motion, glossy surfaces, overactive lighting, and over-polished commercial visuals.

## Verified vs cautious capabilities

Seedance 2.0 research supports treating image, video, and audio references as important control surfaces. It also supports a 4 to 15 second workflow and audio-video generation language in current materials. Still, do not overclaim exact control for accents, lip sync, negative-prompt syntax, aspect ratio limits, or dialogue reliability unless the actual Seedance surface being used confirms those controls.

Practical rule:

* Use `Audio:` and `Voice / dialogue:` as direction.
* Treat exact accent, voice, and lip sync as items to QA.
* If audio is not supported in the current tool surface, the audio lines become production direction for post-processing.
* Never promise perfect lip sync or perfect accent reproduction.

## One mover rule

For the most realistic image-to-video results, decide what moves.

Use only one primary mover by default:

* subject moves, camera stays mostly stable
* camera moves, subject motion stays minimal
* environment moves subtly, subject and camera stay stable

Do not combine strong subject motion, strong camera motion, and environmental motion in the same short clip unless the user specifically asks and realism is less important.

Good combinations:

* static camera + natural blink and breathing
* slight push-in + almost no subject movement
* slight handheld drift + small smile change
* static product + steam rising
* locked source frame + background reflections shifting lightly

Risky combinations:

* fast camera move + hand gesture + speaking
* walking + talking + zooming
* product spin + camera orbit
* nightclub crowd motion + subject dancing + fast handheld camera
* face close-up + long dialogue + head turns

## Realistic camera language

Use camera details that make the clip feel captured, not rendered.

Good details:

* realistic phone-video feel
* RAW iPhone video
* smartphone back camera
* front-camera mirror video
* handheld phone footage
* natural vertical framing
* slightly imperfect composition
* natural HDR
* slight phone sharpening
* slight autofocus breathing
* subtle exposure shift
* natural motion blur
* compression artifacts in shadows
* eye-level medium close-up
* chest-level handheld framing
* no cinematic color grading

For vertical social videos, usually use 9:16 and close-up or medium framing.

For image-to-video, do not ask for a new camera angle unless the user wants the scene redesigned. From a single source frame, large camera moves can create impossible parallax and background melting.

## Practical lighting

Always specify a real light source and direction.

For image-to-video, preserve the source frame's lighting:

* same light source
* same direction
* same shadow pattern
* same color temperature
* same exposure
* same reflections

Good lighting details:

* natural daylight from a nearby window
* soft morning light from camera-left
* warm tungsten light from overhead
* cool bathroom daylight from the mirror side
* neon reflections on wet pavement
* practical indoor lamp light
* gentle shadows on the right side of the face
* realistic darkness in low-light scenes
* no studio lighting if the style is UGC

Do not say only “good lighting” or “perfect lighting.”

## Motion realism

Use one clear action. Keep movement physically possible.

Safest actions:

* subtle breathing
* one blink
* tiny eye shift
* small head turn
* slight smile change
* hair moving lightly
* fabric shifting slightly
* steam rising
* dust moving in sunlight
* reflections shifting lightly
* slow camera push-in
* very slight handheld drift

Medium-risk actions:

* holds product toward camera
* places product on table
* opens package once
* applies product once
* sprays mist once
* takes one bite
* pours drink
* slices bread
* walks one or two steps and stops
* speaks one short line to camera
* adjusts posture once

High-risk actions to avoid by default:

* complex hand choreography
* spinning product in hand
* tossing product
* dancing
* running
* fight scenes
* fast cuts
* multiple competing subjects
* too many actions in one clip
* impossible camera moves
* exaggerated gestures
* long dialogue while the head turns

## Audio and foley

Realistic video feels better when sound matches the visible scene.

Use the lowest-risk audio that fits the goal:

1. Silence
2. Quiet room tone
3. Simple ambience
4. One or two foley cues tied to visible action
5. Music only if requested or useful
6. Dialogue only when necessary

Good audio details:

* quiet room tone
* phone-recorded room tone
* light traffic outside
* soft footsteps
* fabric movement
* spray bottle hiss
* cup placed on table
* paper rustle
* soda fizz
* grill sizzle
* coffee shop murmur
* distant nightclub bass
* wind through trees
* subtle echo in a room
* no music unless requested

Do not write generic audio like “cinematic soundscape” for realistic UGC or image-to-video.

If the user does not ask for music, usually say no music.

## Voice and dialogue

When speech is included, always fill `Voice / dialogue:` with:

* language
* subtle accent or dialect if relevant
* delivery style
* pace
* recording style
* exact spoken line
* lip-sync guidance

Keep dialogue short. One natural sentence is usually best.

Good voice details:

* English, natural American accent
* English with a subtle Mexican-American accent
* Spanish, natural Mexican accent
* Spanish, northern Mexico accent
* Spanish with New Mexico or border-region influence
* bilingual English and Spanish with one casual code-switch
* casual phone-recorded voice
* clean close speech
* natural pauses
* realistic breathing
* not announcer-like
* not robotic
* no exaggerated accent

For Spanish, write the exact spoken line in Spanish.

Good Spanish line:

```text
“No tienes que gastar miles para tener una página que se mire bien.”
```

For bilingual:

```text
“Your website should work for you, no nomás estar ahí.”
```

Treat accent and lip-sync quality as QA items. Do not promise perfect accent or perfect lip sync.

## Lip-sync guidance

For better lip-sync odds:

* one speaker at a time
* face visible
* medium close-up
* mouth unobstructed
* no fast talking
* no long sentences
* no heavy head turns while speaking
* no camera whip movement during dialogue
* no background speakers
* no singing unless requested

Include lip-sync notes inside `Voice / dialogue:`.

Example:

```text
Voice / dialogue:
Spanish, natural northern Mexican accent, warm conversational delivery, exact line: “La página por fin nos empezó a traer clientes de verdad.” One speaker only, visible mouth, moderate pace, not announcer-like.
```

## Product realism

For product videos, preserve the product.

Include:

* product material
* product shape
* label or logo preservation
* surface
* lighting direction
* contact shadows
* reflection behavior
* no warped packaging
* no changed label
* no fake extra text
* no duplicate products

Keep product motion simple.

Best product motions:

* slow push-in
* light steam rising
* condensation moving slightly
* hand enters once to pick up the product
* product placed on table once
* package opens once

Avoid:

* product spinning
* product floating
* product morphing
* label changing
* new products appearing
* impossible reflections

## Duration guidance

Shorter clips are usually more realistic.

* 4 seconds: product micro-motion, b-roll, simple image animation, silent hero motion
* 5 to 6 seconds: UGC hook, simple talking-head line, product reveal, local business owner clip
* 7 to 10 seconds: two-part reveal, short testimonial, simple product demo, use beats when there are multiple events
* 10 to 15 seconds: only simple multi-beat stories or demos, use four or five beats maximum

If realism matters, start with 4 to 6 seconds.

## Timeline beats

Timeline beats are a workflow tool, not a magic syntax.

For 4 to 6 second videos, timeline beats are optional and usually unnecessary when there is only one motion.

For 7 to 15 second videos, use timestamped beats when the clip has multiple events, dialogue timing, product-demo steps, a reveal, or both camera movement and subject action.

Do not force timestamped beats for a simple 7 second clip that only needs one sustained push-in, steam rise, hair movement, or subtle light shift.

Timeline beats must stay inside the `Action:` section. Do not use timeline beats as top-level headers. Do not replace the required Seedance headers.

Correct format for a 7 to 10 second video:

```text
Action:
[0s-2s] Establish the subject and setting with subtle natural movement.
[2s-5s] The main action begins.
[5s-8s] Dialogue, reaction, or a second small movement happens naturally.
[8s-10s] Hold on the final expression, product, or result.
```

Correct format for a 10 to 15 second video:

```text
Action:
[0s-3s] Establish the subject and setting with subtle natural movement.
[3s-7s] The main action begins.
[7s-12s] The subject continues the action or delivers the main spoken line.
[12s-15s] Hold on the final expression, product, or result.
```

Incorrect:

```text
[0s-3s]:
She lifts the serum bottle.

[3s-7s]:
She applies the serum.
```

## Aspect ratios

Always include an aspect ratio.

* 9:16: Reels, TikTok, Shorts, UGC, phone footage
* 16:9: website hero, YouTube, horizontal b-roll
* 1:1: feed post
* 4:5: Instagram feed video
* 2.35:1: cinematic widescreen, only when requested

Verify aspect-ratio support in the Seedance surface being used. If the surface rejects a ratio, choose the closest supported ratio.

## Negative instructions

Use negatives based on likely failure points. Keep constraints short and targeted. Four to eight constraints are usually enough.

Useful constraints by failure type:

Identity:

* no identity drift
* no face change
* same facial structure
* same skin tone
* same hairstyle

Face and mouth:

* no mouth distortion
* no lip jitter
* no rubber lips
* no warped jawline
* no dental artifacts

Hands:

* no warped hands
* no extra fingers
* no fused fingers
* no broken knuckles
* no impossible hand poses

Product:

* no product deformation
* no label drift
* no changed labels
* no duplicate products
* no fake extra text

Background:

* no background melting
* no background redesign
* no shifting walls
* no duplicated objects
* no drifting furniture

Lighting:

* no lighting drift
* no shadow direction change
* no exposure jump
* no color-temperature shift

Camera:

* no whip pan
* no crash zoom
* no orbit
* no impossible parallax
* no sudden reframing

Audio and dialogue:

* no robotic voice
* no announcer voice unless requested
* no exaggerated accent
* no mismatched ambience
* no overlapping speakers

General:

* no CGI look
* no 3D render
* no cartoon look
* no plastic skin
* no beauty filter
* no glossy commercial style
* no fake logos
* no watermark
* no fake text

## Output line rule

The `Output:` section must contain only duration and aspect ratio.

Correct:

```text
Output:
6 seconds, 9:16.
```

Incorrect:

```text
Output:
High-fidelity 4K realistic video.
```

Do not put quality terms, resolution terms, platform names, or style descriptions in the `Output:` section.

Forbidden in `Output:`:

* 4K
* 8K
* high-fidelity
* realistic video
* cinematic
* professional
* ultra realistic
* Instagram Reel
* social media ad

## Strong prompt templates

### ChatGPT Image 2.0 reference to subtle realistic video

```text
Create subtle realistic image-to-video, 5 seconds, 9:16.

Subject:
The uploaded ChatGPT Image 2.0 image is the locked source frame. Preserve the same identity, facial structure, hairstyle, wardrobe, background layout, lighting direction, camera angle, and composition.

Action:
Animate only one micro-action: [blink once / slight inhale and exhale / tiny head turn / small smile change / hair moving lightly].

Scene:
Keep the original location exactly as shown in the source frame.

Camera:
No major camera movement. Same framing as the source image, with only a very slight push-in if needed.

Lighting:
Preserve the original light direction, shadow pattern, exposure, and color temperature.

Motion realism:
Natural breathing, realistic blink timing, tiny posture settling, stable body proportions, stable background, physically plausible motion only.

Audio:
Quiet room tone or silence, no music.

Voice / dialogue:
None.

Constraints:
Do not redesign the frame. No identity change, no face warp, no hand distortion, no wardrobe changes, no background melting, animate only the requested motion.

Output:
5 seconds, 9:16.
```

### RAW iPhone UGC image-to-video

```text
Create realistic UGC image-to-video, 6 seconds, 9:16.

Subject:
The uploaded image is the locked source frame. Preserve the same person, clothing, hairstyle, phone-camera framing, background, and practical lighting.

Action:
The subject gives one natural reaction to camera: [small nod / slight smile / lifts the product once / adjusts posture once].

Scene:
Keep the scene exactly as shown, with the same casual real-world context and background clutter.

Camera:
Handheld phone-video feel, same eye-level framing, extremely slight handheld drift only.

Lighting:
Keep the existing natural or practical light exactly consistent with the source frame.

Motion realism:
Natural body weight shift, realistic breathing, slight handheld sway, no dramatic motion.

Audio:
Phone-recorded room tone or light outdoor ambience, no music.

Voice / dialogue:
[None. Or: English, casual conversational delivery, phone-recorded voice, exact line: “[short UGC line].” One speaker only, face visible, mouth unobstructed.]

Constraints:
No glossy ad look, no beauty filter, no identity change, no mouth distortion, no warped hands, no background change.

Output:
6 seconds, 9:16.
```

### Product b-roll video

```text
Create realistic product image-to-video b-roll, 5 seconds, 16:9.

Subject:
The uploaded image is the locked source frame. Preserve the exact product shape, label placement, packaging proportions, colors, reflections, and surface contact.

Action:
Animate one simple product-related motion only: [slow push-in / light steam rising / tiny condensation movement / hand entering once to pick up the product].

Scene:
Keep the original product environment exactly as shown in the source image.

Camera:
Controlled slow push-in or locked-off product shot, same angle and scale as the source frame.

Lighting:
Preserve the same light direction, highlight behavior, reflections, and contact shadows.

Motion realism:
Stable product geometry, stable label text, realistic material behavior, no floating or spinning.

Audio:
One or two subtle foley cues tied to the action, no music unless requested.

Voice / dialogue:
None.

Constraints:
No label drift, no fake text, no extra products, no warped packaging, no impossible reflections, no background melting.

Output:
5 seconds, 16:9.
```

### Talking-head UGC video with dialogue

```text
Create realistic talking-head image-to-video, 6 seconds, 9:16.

Subject:
The uploaded image is the locked source frame. Preserve the same face, hair, wardrobe, background, lighting, and medium close-up framing.

Action:
The subject delivers one short line to camera with minimal head movement and one small natural gesture.

Scene:
Keep the original setting exactly as shown in the source frame.

Camera:
Static or extremely slight push-in, medium close-up, eye-level.

Lighting:
Preserve the same realistic practical light and shadow continuity.

Motion realism:
Natural blink timing, subtle breathing, small jaw and lip movement, slight head nod only.

Audio:
Clean close speech with light room tone, no music.

Voice / dialogue:
English, natural American accent or subtle Mexican-American accent, casual delivery, not robotic, exact line: “[short spoken line].” One speaker only, visible mouth, no fast speech.

Constraints:
No identity change, no mouth distortion, no lip jitter, no announcer voice, no exaggerated accent, no background drift.

Output:
6 seconds, 9:16.
```

### Realistic nightclub or event video

```text
Create realistic nightlife image-to-video, 5 seconds, 9:16.

Subject:
The uploaded image is the locked source frame. Preserve the same subject identity, outfit, crowd density, practical lights, and composition.

Action:
Animate one simple event motion only: [small head turn / slight drink raise / hair movement / ambient crowd movement in the background].

Scene:
Keep the original nightclub or event environment exactly as shown in the source frame.

Camera:
Handheld phone-video feel, slight drift only, same framing as the source image.

Lighting:
Preserve realistic darkness, mixed practical colored light, and existing shadow relationships. Do not brighten the scene unnaturally.

Motion realism:
Low-light believable motion, mild ambient crowd movement only, stable subject proportions, stable light continuity.

Audio:
Distant bass, crowd murmur, room reverb, no clean studio sound.

Voice / dialogue:
None.

Constraints:
No overbright nightclub look, no face warping, no hand distortion, no floating subjects, no background melting, no glossy commercial sheen.

Output:
5 seconds, 9:16.
```

## Video repair rule

When the user says the video looked fake, identify the failure and reduce complexity.

Use this pattern:

```text
Create a repaired realistic image-to-video pass, [duration], [aspect ratio].

Subject:
Use the uploaded image as the locked source frame and preserve the same identity, facial structure, wardrobe, background, lighting direction, camera angle, and composition.

Action:
Repeat the intended action in a smaller and more controlled way: [describe the original intended action].

Scene:
Keep the original environment exactly unchanged from the source image.

Camera:
Reduce camera movement to [static / very slight push-in / very slight handheld drift].

Lighting:
Preserve the original exposure, light direction, shadow pattern, and color temperature exactly.

Motion realism:
Reduce motion amplitude, stabilize the face and hands, keep the background static, keep all movement physically plausible.

Audio:
[Silence / simple ambience / same short line as before], no music.

Voice / dialogue:
[None. Or: exact short line], slower pace, one speaker, visible mouth, cleaner sync.

Constraints:
No identity change, no face remapping, no mouth distortion, no warped hands, no background melting, no label drift, animate only the corrected motion.

Output:
[duration], [aspect ratio].
```

## Final self-check

Before answering, silently verify:

* The response is one code block.
* The first line starts with `Create`.
* The exact headers appear in this order:
  * Subject:
  * Action:
  * Scene:
  * Camera:
  * Lighting:
  * Motion realism:
  * Audio:
  * Voice / dialogue:
  * Constraints:
  * Output:
* The prompt includes `Constraints:`.
* The prompt includes `Output:`.
* The prompt is not a paragraph.
* No custom labels or bracket labels were used.
* For image-to-video, `Subject:` declares the uploaded image as the locked source frame.
* For 4 to 6 second clips, the prompt has one primary motion.
* For longer clips, timestamped beats are used only when the clip has multiple events, dialogue timing, product-demo steps, or a reveal.
* If voice is included, the line is short, the speaker is visible, and lip-sync risk is controlled.
* `Output:` contains only duration and aspect ratio.

If any check fails, rewrite the prompt before answering.
