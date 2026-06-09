---

name: seedance-2
description: Write paste-ready Seedance 2.0 video prompts using a strict multi-line format for realistic AI video clips with believable motion, natural camera behavior, synced audio, realistic voices, accents, dialogue, ambient sound, product shots, UGC videos, testimonials, social ads, b-roll, and image-to-video animation. Use this whenever the user mentions Seedance, Seedance 2.0, a Seedance prompt, text-to-video, image-to-video, reference-to-video, video-to-video, AI video prompts, realistic UGC video, talking-head video, product video, voiceover, dialogue, accents, lip sync, or asks why a generated clip looks plasticky, fake, static, glitchy, overproduced, or unnatural.
---

# Seedance 2.0 Prompting Skill

Default output: return only one clean, paste-ready Seedance prompt inside one `text` code block.

Do not include scenario setup, sample input, task summary, analysis, explanation, tutorial, skill execution notes, or extra commentary unless the user explicitly asks for reasoning.

The goal is to write realistic Seedance 2.0 prompts that produce believable video, not fake-looking AI clips. Prioritize real camera behavior, practical lighting, natural movement, believable sound, grounded dialogue, and simple physical actions.

Avoid overproduced AI-video language. Do not rely on phrases like `cinematic masterpiece`, `ultra realistic`, `8k`, `epic`, `award-winning`, `perfect lighting`, `Hollywood quality`, or `insanely detailed`. These often create plastic skin, glossy product surfaces, fake motion, and over-polished commercial visuals.

## Non-negotiable output contract

Every final Seedance prompt must use the required multi-line structure.

The prompt must begin with one of these opening lines:

```text
Create [video type], [duration], [aspect ratio].
```

or, for image-to-video:

```text
Animate the uploaded image into a realistic video, [duration], [aspect ratio].
```

Do not output a paragraph prompt.

Do not invent new headers.

Do not use bracketed labels.

Do not combine sections.

Do not omit `Constraints:`.

Do not omit `Output:`.

A prompt that uses different headers, bracketed labels, or a paragraph summary has failed the skill, even if the visual idea is good.

## Required format for non-speaking videos

```text
Create [video type], [duration], [aspect ratio].

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

Constraints:
[what to avoid]

Output:
[duration], [aspect ratio].
```

## Required format for videos with speech

```text
Create [video type], [duration], [aspect ratio].

Subject:
[one primary subject with concrete visible details]

Action:
[one clear physical action while speaking]

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
Language: [English / Spanish / bilingual].
Accent: [specific accent or dialect].
Delivery: [tone, pace, naturalness].
Exact spoken line: “[short spoken line]”
Lip sync: face visible while speaking, natural mouth movement, realistic blinking, small pauses, no exaggerated lip motion.

Constraints:
[what to avoid]

Output:
[duration], [aspect ratio].
```

## Required format for image-to-video

```text
Animate the uploaded image into a realistic video, [duration], [aspect ratio].

Preserve:
[what must stay unchanged from the uploaded image]

Motion:
[one clear motion]

Camera:
[subtle camera movement, stable and physically possible]

Lighting:
[preserve original lighting direction, optional subtle natural light shift]

Motion realism:
[keep movement subtle and physically believable]

Audio:
[ambient sound or no audio]

Constraints:
[what to avoid]

Output:
[duration], [aspect ratio].
```

## Format compliance check

Before finalizing, silently check the prompt.

A valid Seedance prompt must:

* start with `Create [video type], [duration], [aspect ratio].`, except image-to-video
* use `Subject:` exactly for text-to-video
* use `Preserve:` exactly for image-to-video
* use `Action:` exactly for text-to-video
* use `Motion:` exactly for image-to-video
* use `Scene:` exactly
* use `Camera:` exactly
* use `Lighting:` exactly
* use `Motion realism:` exactly
* use `Audio:` exactly
* include `Voice / dialogue:` when the video has speech
* include `Constraints:` every time
* end with `Output:` every time
* keep every section separate
* never collapse the prompt into a final paragraph

If any required header is missing, renamed, bracketed, or combined into another section, rewrite the prompt before answering.

Invalid header names include:

* `[SCENE:]`
* `[MOTION:]`
* `[AUDIO:]`
* `[VOICE:]`
* `[VISUAL STYLE:]`
* `[CHARACTER:]`
* `[VOICE/AUDIO:]`
* `[ACTION/MOTION:]`
* `[PROMPT:]`
* `Character:`
* `Visuals:`
* `Prompt:`
* `Ambient:`
* `Voice:`

These are invalid even if the prompt content is good.

## Core realism rules

Seedance prompts should feel like production notes for a real short video.

A strong prompt defines:

* one primary subject
* one clear action
* a real environment
* camera behavior
* practical lighting direction
* realistic motion
* audio or room tone
* voice and accent, if speech is included
* constraints
* duration and aspect ratio

Most prompts should focus on one subject and one action per shot.

Good realism details:

* RAW iPhone video
* smartphone back camera
* real handheld phone footage
* natural vertical framing
* slightly imperfect composition
* natural HDR
* slight phone sharpening
* slight autofocus breathing
* subtle exposure shift
* natural motion blur
* compression artifacts in shadows
* real room tone
* practical daylight
* tungsten indoor light
* neon reflections
* realistic skin texture
* natural blinking
* small head movement
* natural breathing
* believable hand motion

Avoid:

* 8k
* cinematic masterpiece
* ultra realistic
* perfect lighting
* flawless skin
* glossy commercial look
* floating camera with impossible movement
* over-smoothed skin
* perfect lip sync with no natural face movement
* dramatic movie trailer voice unless requested
* too many actions in one shot

## Choosing the video type

| Request looks like                                  | Use this type                     |
| --------------------------------------------------- | --------------------------------- |
| Realistic creator video, casual ad, social clip     | RAW iPhone-style UGC video        |
| Person speaking to camera                           | talking-head or testimonial video |
| Product reveal, object animation, food, packaging   | product video                     |
| A photo that needs movement                         | image-to-video                    |
| Atmosphere, location, food detail, lifestyle detail | realistic b-roll                  |
| Multi-angle ad with cuts                            | short multi-shot video            |
| Spanish or English voice with accent                | voice-controlled dialogue video   |
| Video looks fake, plastic, or glitchy               | troubleshooting rewrite           |

## RAW iPhone-style UGC video

Use this for creator videos, casual ads, testimonials, product demos, local business videos, and social media clips.

Include:

* vertical 9:16 unless the user asks otherwise
* smartphone back camera or front camera mirror video
* handheld framing
* slight natural shake
* slight autofocus breathing
* practical light
* natural room tone
* imperfect framing
* no cinematic color grading

Good actions:

* holds product toward camera
* places product on table
* applies product
* takes one bite
* pours drink
* points once
* walks into frame and stops
* speaks one short line to camera

Avoid:

* complex hand choreography
* spinning product in hand
* tossing product
* fast cuts
* multiple products competing for attention
* long dialogue

## Talking-head and testimonial videos

Talking-head clips need natural human imperfections. The person should not look like a perfect avatar.

Include:

* one person
* eye-level camera
* medium close-up
* relaxed posture
* natural blinking
* small head movements
* slight breath before speaking
* one short spoken line
* realistic room tone
* clear language and accent
* natural pacing

Avoid:

* long paragraphs
* multiple speakers
* huge gestures
* announcer voice unless requested
* fake corporate background
* stock-video smile
* perfect beauty-filter skin

For better lip sync:

* keep the face visible
* avoid objects covering the mouth
* avoid fast talking
* avoid heavy head turns
* avoid camera whip movement during dialogue
* avoid background speakers
* avoid singing unless requested

## Voice and accent control

When the video includes speech, always specify:

* language
* accent or dialect
* voice type, if relevant
* delivery style
* pace
* recording style
* exact spoken line
* lip sync behavior

Good voice details:

* English, natural American accent
* English with a subtle Mexican-American accent
* Spanish, natural Mexican accent
* Spanish, northern Mexico accent
* Spanish, New Mexico or border-region influence
* bilingual English and Spanish, casual code-switching
* warm female voice in her late 20s
* friendly male voice in his early 30s
* calm local business owner tone
* casual phone-recorded voice
* clean lavalier mic sound
* slight room tone
* natural pauses
* not announcer-like
* not robotic
* no exaggerated accent

Bad voice details:

* perfect voice
* professional voice
* viral voice
* cinematic narration
* generic Spanish accent
* generic Latino accent
* over-the-top salesman
* robotic clarity
* too fast
* too much dialogue

## Spanish dialogue rules

For Spanish videos, write the exact spoken line in Spanish.

Keep the line short and natural. Do not overformalize it unless the user asks.

Good:

```text
Exact spoken line: “No necesitas gastar miles para tener una página profesional.”
```

Better for casual social video:

```text
Exact spoken line: “No tienes que gastar miles para tener una página que se mire bien.”
```

For a regional sound:

```text
Accent: natural Mexican Spanish with a northern or border-region feel, casual and conversational, not exaggerated.
```

Avoid vague accent instructions like:

```text
Spanish accent.
```

## English dialogue rules

For English videos, specify whether the voice should sound native, regional, bilingual, or lightly accented.

Examples:

```text
Accent: natural American English, friendly and casual.
```

```text
Accent: English with a subtle Mexican-American accent, natural and not exaggerated.
```

```text
Accent: Southwest U.S. English, casual local business tone.
```

Keep dialogue short. One sentence usually works best.

## Bilingual dialogue rules

Use bilingual dialogue only when the user asks or when it clearly fits the concept.

Keep the switch natural.

Good:

```text
Language: bilingual English and Spanish.
Accent: casual Mexican-American bilingual speaker.
Exact spoken line: “Your website should work for you, no nada más estar ahí.”
Delivery: natural code-switching, friendly and conversational.
```

Do not make bilingual speech too long. The more language switching, the more likely lip sync or timing can fail.

## Product videos

Product videos should keep the product physically accurate. Do not let the model redesign it.

Include:

* product material
* product shape
* label or logo preservation
* surface
* lighting direction
* one camera movement
* realistic contact shadows
* no warped packaging
* no changed label
* no fake extra text

Product motion should be simple:

* slow camera push-in
* slow 180-degree orbit
* steam rising
* condensation moving
* hand placing product down
* hand opening package
* liquid pouring

Avoid:

* floating products
* impossible rotations
* fast spins
* product changing shape
* labels changing
* duplicate products

## Image-to-video rules

For image-to-video, the uploaded image already defines the subject and scene.

Do not redescribe the whole image unless the user specifically asks for changes.

Describe only:

* what must stay unchanged
* one motion
* camera movement
* lighting shift
* audio
* constraints

Use `Preserve:` instead of `Subject:`.

Use `Motion:` instead of `Action:`.

Always include:

```text
No identity change, no background change, no new objects, no text distortion, no warped hands, no product deformation, no CGI look.
```

## Multi-shot videos

Use multi-shot prompts only when the user truly needs cuts.

Keep it to 2 to 4 shots.

Always state:

* total duration
* aspect ratio
* consistent subject
* consistent wardrobe
* consistent lighting
* each cut’s shot size and action

A multi-shot prompt may use `Cut 1:`, `Cut 2:`, and `Cut 3:` only inside the `Action:` section. The final prompt must still include the required headers.

## Audio and foley

Realistic video feels better when audio matches the scene.

Use one to three audio details:

* quiet room tone
* light traffic outside
* soft footsteps
* fabric movement
* cup placed on table
* paper rustle
* soda fizz
* grill sizzle
* coffee shop murmur
* distant nightclub bass
* wind through trees
* phone-recorded ambient noise
* subtle echo in a room
* no music unless requested

Do not overload sound.

## Duration guidance

Shorter clips are usually more realistic.

* 4 seconds: product motion, b-roll, simple image animation
* 5 to 6 seconds: UGC hook, simple talking-head line, product reveal
* 7 to 10 seconds: testimonial or simple multi-shot ad
* 10 to 15 seconds: only when the user needs a longer concept and the action is simple

Do not stretch a weak idea to 15 seconds. If the clip needs realism, start with 4 to 6 seconds.

## Aspect ratios

Always include an aspect ratio.

* 9:16: Reels, TikTok, Shorts, UGC, phone footage
* 16:9: website hero, YouTube, horizontal b-roll
* 1:1: feed post
* 4:5: Instagram feed video
* 2.35:1: cinematic widescreen, only when requested

For vertical video, prefer close-up or medium shots. Wide shots often lose detail in 9:16.

## Text overlays

Use text overlays only if the user asks.

For text overlays, specify inside the `Action:` or `Scene:` section:

* exact text
* timing
* position
* size
* style
* no extra words
* no misspellings

If the text is critical, recommend generating the video without text and adding the text in editing software.

## Common problems and fixes

| Problem                                | Likely cause                                       | Fix                                                              |
| -------------------------------------- | -------------------------------------------------- | ---------------------------------------------------------------- |
| Looks plastic                          | no practical lighting, too much cinematic language | add real light source, direction, no CGI look, no plastic skin   |
| Looks static                           | no clear action                                    | add one physical action and one camera move                      |
| Hands glitch                           | action too complex                                 | simplify to one slow hand action                                 |
| Lip sync is bad                        | dialogue too long or face not visible              | use one short sentence, medium close-up, face visible            |
| Voice sounds fake                      | vague voice instruction                            | specify language, accent, tone, pace, recording style            |
| Accent is exaggerated                  | prompt says only Spanish accent or Latino accent   | specify natural, subtle, regional, not exaggerated               |
| Scene changes randomly                 | too many cuts or weak consistency                  | lock wardrobe, lighting, environment, subject                    |
| Image-to-video drifts                  | prompt redescribes image or changes too much       | describe motion only, add no identity/background change          |
| Product warps                          | too much motion or vague product lock              | preserve product shape, label, proportions, colors               |
| Audio feels detached                   | no room tone or foley                              | add ambient sound tied to scene                                  |
| Looks like an ad when it should be UGC | too polished                                       | RAW iPhone video, handheld, natural room tone, imperfect framing |

## Negative instructions

Use negatives based on likely failure points, not huge lists.

Useful negatives:

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

## Final output reminder

Default response must be only one paste-ready Seedance prompt in a single code block.

The prompt must use the required multi-line template with exact headers.

Do not output a paragraph prompt.

Do not use bracketed labels.

Do not invent new headers.

Always include `Constraints:`.

Always include `Output:`.
****
