---

name: seedance-2
description: "Write paste-ready Seedance 2.0 prompts for realistic AI videos using one strict multi-line format with exact headers: Create, Subject, Action, Scene, Camera, Lighting, Motion realism, Audio, Voice / dialogue, Constraints, Output. Use for Seedance prompts, AI video, text-to-video, image-to-video, UGC, product videos, testimonials, talking-head videos, voiceover, dialogue, accents, lip sync, ambient sound, and fixing videos that look fake or overproduced."
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Seedance 2.0 Prompting Skill

Default output: return only one paste-ready Seedance prompt inside one `text` code block.

Do not include scenario setup, sample input, task summary, analysis, explanation, tutorial, skill execution notes, or extra commentary unless the user explicitly asks for reasoning.

## Required final answer format

Every final answer must be one code block using this exact structure:

```text
Create [specific video type], [duration], [aspect ratio].

Subject:
[one primary subject with concrete visible details]

Action:
[one clear physical action]

Scene:
[real location, time of day, background details]

Camera:
[shot size, camera angle, phone or lens feel, camera movement]

Lighting:
[practical light source, direction, color temperature, shadows]

Motion realism:
[what moves, what stays stable, pacing, natural micro-movement]

Audio:
[ambient sound, room tone, foley, music only if requested]

Voice / dialogue:
[language, accent, delivery, exact spoken line, lip sync notes, or None.]

Constraints:
[what to avoid]

Output:
[duration], [aspect ratio].
```

The final prompt must always include every header shown above.

Use `Voice / dialogue: None.` when there is no speech.

Do not rename, remove, reorder, bracket, or combine headers.

Do not output a paragraph prompt.

Do not add any other sections.

A prompt fails this skill if it does not start with `Create`, does not include `Constraints:`, or does not end with `Output:`.

## Image-to-video rule

For image-to-video, still use the same required structure.

Use the uploaded image as the subject and include preservation instructions inside `Subject:` and `Constraints:`.

Do not create a separate image-to-video template.

Example approach inside the required format:

Subject:
The uploaded image is the source frame. Preserve the subject identity, background, clothing, product shape, labels, colors, composition, and camera angle.

Action:
Animate only one motion, such as a slow push-in, steam rising, hair moving slightly, light shifting, or a hand lifting.

## Realism goal

The goal is to produce believable video, not fake-looking AI clips.

Prioritize:

* real camera behavior
* practical lighting
* natural movement
* believable sound
* grounded dialogue
* simple physical actions
* realistic skin texture
* natural voice delivery
* one subject
* one main action

Avoid overproduced AI-video language such as:

* cinematic masterpiece
* ultra realistic
* 4k, 8k
* epic
* award-winning
* perfect lighting
* Hollywood quality
* insanely detailed
* flawless skin

These often create plastic skin, fake motion, glossy surfaces, and over-polished commercial visuals.

## Realistic camera language

Use camera details that make the clip feel captured, not rendered.

Good details:

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
* soft background blur
* no cinematic color grading

For vertical social videos, usually use 9:16 and close-up or medium framing.

## Practical lighting

Always specify a real light source and direction.

Good lighting details:

* natural daylight from a nearby window
* soft morning light from camera-left
* warm tungsten light from overhead
* cool bathroom daylight from the mirror side
* neon reflections on wet pavement
* practical indoor lamp light
* gentle shadows on the right side of the face
* no studio lighting, if the style is UGC

Do not say only “good lighting” or “perfect lighting.”

## Motion realism

Use one clear action. Keep movement physically possible.

Good actions:

* holds product toward camera
* places product on table
* opens package
* applies product
* sprays mist once
* takes one bite
* pours drink
* slices bread
* walks into frame and stops
* speaks one short line to camera
* slow camera push-in
* slow handheld drift

Avoid:

* complex hand choreography
* spinning product in hand
* tossing product
* fast cuts
* multiple competing subjects
* too many actions in one clip
* impossible camera moves
* exaggerated gestures

## Voice and dialogue

When speech is included, always fill `Voice / dialogue:` with:

* language
* accent or dialect
* delivery style
* pace
* recording style
* exact spoken line
* lip sync behavior

Keep dialogue short. One natural sentence is usually best.

Good voice details:

* English, natural American accent
* English with a subtle Mexican-American accent
* Spanish, natural Mexican accent
* Spanish, northern Mexico accent
* Spanish with New Mexico or border-region influence
* bilingual English and Spanish with casual code-switching
* casual phone-recorded voice
* clean lavalier mic sound
* natural pauses
* realistic breathing
* not announcer-like
* not robotic
* no exaggerated accent

For Spanish, write the exact spoken line in Spanish.

Good Spanish line:
“No tienes que gastar miles para tener una página que se mire bien.”

For bilingual:
“Your website should work for you, no nada más estar ahí.”

## Lip sync

For better lip sync:

* one speaker at a time
* face visible
* medium close-up
* no object covering the mouth
* no fast talking
* no long sentences
* no heavy head turns while speaking
* no camera whip movement during dialogue
* no background speakers
* no singing unless requested

Include lip sync notes inside `Voice / dialogue:`.

## Audio and foley

Realistic video feels better when the sound matches the scene.

Use one to three audio details:

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

If the user does not ask for music, usually say no music.

## Product realism

For product videos, preserve the product.

Include:

* product material
* product shape
* label or logo preservation
* surface
* lighting direction
* realistic contact shadows
* no warped packaging
* no changed label
* no fake extra text
* no duplicate products

Keep product motion simple.

## Duration guidance

Shorter clips are usually more realistic.

* 4 seconds: product motion, b-roll, simple image animation
* 5 to 6 seconds: UGC hook, simple talking-head line, product reveal
* 7 to 10 seconds: testimonial or simple multi-shot ad, use timeline beats when there is dialogue, a product demo, or more than one action
* 10 to 15 seconds: only when the action is simple, use timeline beats, but keep it to four or five beats maximum

If realism matters, start with 4 to 6 seconds.

## Timeline beats

Timeline beats are mandatory for any video longer than 6 seconds.

For 4 to 6 second videos, timeline beats are optional.

For 7 to 15 second videos, the Action: section must include timestamped beats.

Timeline beats must stay inside the Action: section. Do not use timeline beats as top-level headers. Do not replace the required Seedance headers.

Correct format for a 7 to 10 second video:

Action:
[0s-2s] Establish the subject and setting with subtle natural movement.
[2s-5s] The main action begins.
[5s-8s] Dialogue, reaction, or a second small movement happens naturally.
[8s-10s] Hold on the final expression, product, or result.

Correct format for a 10 to 15 second video:

Action:
[0s-3s] Establish the subject and setting with subtle natural movement.
[3s-7s] The main action begins.
[7s-12s] The subject continues the action or delivers the main spoken line.
[12s-15s] Hold on the final expression, product, or result.

For 10 to 15 second videos, use four or five beats maximum. Do not write a separate beat for every single second unless exact timing is important.

Use timeline beats for:

product demos longer than 6 seconds
testimonials longer than 6 seconds
talking-head videos longer than 6 seconds
multi-step UGC videos
food preparation
before-and-after style clips
image-to-video with more than one movement
clips with both camera movement and subject action

Avoid timeline beats when:

the clip is 4 to 6 seconds and has only one simple movement
image-to-video only needs a slow push-in, steam rising, hair movement, or subtle light shift
the timeline would make a short prompt crowded

Correct:

Action:
[0s-3s] She lifts the serum bottle toward the mirror and smiles naturally.
[3s-7s] She applies a few drops to her cheek while beginning the spoken line.
[7s-12s] She gently rubs the serum into her skin with realistic hand movement and natural blinking.
[12s-15s] She holds the bottle near her face and finishes with a genuine smile.

Incorrect:

[0s-3s]:
She lifts the serum bottle.

[3s-7s]:
She applies the serum.

The required headers must still appear exactly:

Subject:
Action:
Scene:
Camera:
Lighting:
Motion realism:
Audio:
Voice / dialogue:
Constraints:
Output:

Before finalizing, silently check this rule:

If the video is longer than 6 seconds and the Action: section does not include timestamped beats, rewrite the prompt before answering.

## Aspect ratios

Always include an aspect ratio.

* 9:16: Reels, TikTok, Shorts, UGC, phone footage
* 16:9: website hero, YouTube, horizontal b-roll
* 1:1: feed post
* 4:5: Instagram feed video
* 2.35:1: cinematic widescreen, only when requested

## Negative instructions

Use negatives based on likely failure points.

Useful constraints:

* no CGI look
* no 3D render
* no cartoon look
* no plastic skin
* no beauty filter
* no glossy commercial style
* no cinematic color grading, if RAW phone style
* no fake logos
* no watermark
* no fake text
* no warped hands
* no extra fingers
* no distorted mouth
* no robotic voice
* no announcer voice, unless requested
* no exaggerated accent
* no identity change
* no background change
* no product deformation
* no changed labels

## Output line rule
The Output: section must contain only duration and aspect ratio.

Correct:

Output:
15 seconds, 9:16.

Incorrect:

Output:
High-fidelity 4K realistic video.

Do not put quality terms, resolution terms, platform names, or style descriptions in the Output: section.

Forbidden in Output::

4K
8K
high-fidelity
realistic video
cinematic
professional
ultra realistic
Instagram Reel
social media ad

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

If any check fails, rewrite the prompt before answering.
