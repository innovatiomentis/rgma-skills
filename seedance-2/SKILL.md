---

name: seedance-2
description: Write paste-ready Seedance 2.0 video prompts for realistic AI video clips with believable motion, natural camera behavior, synced audio, realistic voices, accents, dialogue, ambient sound, product shots, UGC videos, testimonials, social ads, b-roll, and image-to-video animation. Use this whenever the user mentions Seedance, Seedance 2.0, a Seedance prompt, text-to-video, image-to-video, reference-to-video, video-to-video, AI video prompts, realistic UGC video, talking-head video, product video, voiceover, dialogue, accents, lip sync, or asks why a generated clip looks plasticky, fake, static, glitchy, overproduced, or unnatural.
---

# Seedance 2.0 Prompting Skill

Default output: give the user one clean, paste-ready prompt in a code block. Do not include scenario, analysis, explanation, or “Skill Execution” unless the user explicitly asks for reasoning.

The goal is to write realistic Seedance 2.0 prompts that produce believable video, not fake-looking AI clips. Prioritize real camera behavior, practical lighting, natural movement, believable sound, grounded dialogue, and simple physical actions.

Avoid overproduced AI-video language. Do not rely on phrases like “cinematic masterpiece,” “ultra realistic,” “8k,” “epic,” “award-winning,” “perfect lighting,” “Hollywood quality,” or “insanely detailed.” Those often create plastic skin, glossy product surfaces, fake motion, and over-polished commercial visuals.

## Core rule

Seedance prompts should feel like production notes for a real short video.

A strong prompt defines:

* shot type
* subject
* one clear action
* environment
* camera behavior
* lighting direction
* motion realism
* audio
* voice or dialogue, if needed
* constraints
* aspect ratio and duration

Most prompts should focus on one subject and one action per shot.

## Decide the video type first

| Request looks like                                    | Output type                       |
| ----------------------------------------------------- | --------------------------------- |
| Product reveal, product ad, object animation          | product video prompt              |
| Realistic creator video, casual ad, social media clip | UGC / RAW phone video prompt      |
| Person speaking to camera                             | talking-head / testimonial prompt |
| A photo that needs movement                           | image-to-video prompt             |
| Atmosphere, business location, food, lifestyle detail | realistic b-roll prompt           |
| Multi-angle ad with cuts                              | short multi-shot prompt           |
| Dialogue or voice                                     | audio-video prompt                |
| Spanish or English voice with accent                  | voice-controlled dialogue prompt  |
| Video looks fake, plastic, or glitchy                 | troubleshooting rewrite           |

## The structure that works

Use this order:

```text
Create [video type], [duration], [aspect ratio].

Subject:
[one primary subject with concrete visible details]

Action:
[one clear physical action]

Scene:
[real location, time of day, background details]

Camera:
[shot size, angle, lens feel, camera movement, handheld or stable]

Lighting:
[practical light source, direction, color temperature, shadows]

Motion realism:
[small natural movements, physics, pacing, what should move and what should stay stable]

Audio:
[ambient sound, room tone, foley, music if needed, no music if not instructed]

Voice / dialogue:
[language, accent, delivery, exact line, lip sync notes]

Constraints:
[what to avoid]
```

## Realism rules

Realism comes from camera behavior, physical movement, light direction, and natural sound.

Good realism details:

* RAW iPhone video
* smartphone back camera
* vertical 9:16
* natural handheld movement
* slight autofocus breathing
* slight exposure adjustment
* natural motion blur
* real room tone
* subtle background noise
* practical daylight
* tungsten indoor light
* neon reflections
* imperfect framing
* compression artifacts
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

## RAW phone video style

Use this for UGC, social ads, creator videos, casual business videos, and realistic everyday clips.

Strong phrases:

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
* no cinematic color grading
* not a professional commercial

Template:

```text
Create a RAW iPhone-style video, [duration], vertical 9:16.

Subject:
[person or product]

Action:
[one clear action]

Scene:
[real setting, time of day, ordinary background details]

Camera:
Smartphone back camera, natural handheld movement, slightly imperfect framing, eye-level or chest-level angle, subtle autofocus breathing.

Lighting:
[practical light source] from [direction], natural shadows, no studio lighting.

Motion realism:
Small natural movements, realistic hand motion, natural blinking and breathing if a person is present, no exaggerated gestures.

Audio:
Real room tone with subtle ambient sound from the setting.

Constraints:
No text, no watermark, no fake logos, no plastic skin, no CGI look, no cinematic color grading, no glossy commercial style.

Output:
[duration], 9:16.
```

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
* one short line of dialogue
* realistic room tone
* clear language and accent
* natural pacing

Avoid:

* long paragraphs
* multiple speakers
* huge gestures
* overly perfect lip sync
* announcer voice unless requested
* fake corporate background
* stock-video smile

Template:

```text
Create a realistic talking-head video, [duration], vertical 9:16.

Subject:
[person description, wardrobe, expression]

Action:
The person speaks directly to the camera with a small natural nod, relaxed posture, natural blinking, and a slight breath before the line.

Scene:
[real room or location], softly out-of-focus background, ordinary details.

Camera:
Static smartphone back camera or tripod phone shot, eye-level medium close-up, slight natural phone sharpness.

Lighting:
Soft practical light from [direction], gentle shadows, realistic skin texture, no beauty filter.

Audio:
Clean but natural phone-recorded voice, light room tone, no music unless requested.

Voice / dialogue:
Language: [English / Spanish / bilingual].
Accent: [specific accent].
Delivery: [friendly, casual, confident, calm, helpful, excited, etc.].
Exact line: “[short spoken line]”

Lip sync:
Natural mouth movement, small pauses, realistic facial expression, no exaggerated lip movement.

Constraints:
No subtitles unless requested, no text overlays, no watermark, no fake logos, no plastic skin, no robotic voice, no announcer voice, no overacting.

Output:
[duration], 9:16.
```

## Voice and accent control

When the video includes speech, specify voice clearly.

Always include:

* language
* accent or dialect
* age range or voice type
* tone
* speed
* recording style
* exact spoken line

Good voice details:

* English, natural American accent
* English with a subtle Mexican-American accent
* Spanish, natural Mexican accent
* Spanish, northern Mexico accent
* Spanish, New Mexico / border-region influence
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

Voice template:

```text
Voice / dialogue:
Language: [English / Spanish / bilingual].
Accent: [specific accent].
Voice: [gender/age/tone if relevant].
Delivery: natural, conversational, not announcer-like, with small pauses and realistic breathing.
Exact spoken line: “[short line]”
Audio style: [phone-recorded / clean lav mic / indoor room tone / outdoor ambient noise].
```

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

If the speaker should sound regional, say:

```text
Accent: natural Mexican Spanish with a northern / border-region feel, casual and conversational, not exaggerated.
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

Do not make bilingual speech too long. The more language switching, the more likely the lip sync or timing can fail.

## Lip sync rules

For better lip sync:

* one speaker at a time
* face visible
* medium close-up
* no food or objects covering the mouth
* no fast talking
* no long sentences
* no heavy head turns while speaking
* no camera whip movement during dialogue
* avoid background speakers
* avoid singing unless the user specifically asks

Add this for dialogue clips:

```text
Lip sync:
Keep the face visible while speaking, natural mouth shapes, realistic blinking, small head movement, no exaggerated lip motion.
```

## Ambient sound and foley

Realistic video feels better when audio matches the scene.

Add simple sound details:

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

Do not overload sound. One to three audio details are enough.

Template:

```text
Audio:
Natural room tone, [one ambient sound], [one foley sound tied to the action]. Keep audio realistic and not overly produced.
```

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

Template:

```text
Create a realistic product video, [duration], [aspect ratio].

Subject:
[product description]

Action:
The product remains still while [one motion happens: slow camera push-in / slow 180-degree orbit / steam rises / condensation moves / hand places it down].

Scene:
[real surface and background]

Camera:
[close-up / medium product shot], [slow push-in / slow orbit], stable and physically possible.

Lighting:
[soft window light / softbox / practical light] from [direction], realistic contact shadows, believable reflections.

Motion realism:
Only the camera and small physical details move. Preserve the product shape, label, logo placement, colors, and proportions.

Audio:
[subtle foley if needed]

Constraints:
No fake text, no changed labels, no warped packaging, no duplicate products, no floating product, no CGI look, no glossy fake reflections.

Output:
[duration], [aspect ratio].
```

## UGC style product demo

For UGC videos with hands, keep the action simple.

Good actions:

* holds product toward camera
* places product on table
* opens package
* takes one bite
* pours drink
* points once
* shows before/after once
* walks into frame and stops

Avoid:

* complex hand choreography
* spinning product in hand
* tossing product
* multiple products
* product changes hands repeatedly
* fast cuts with talking

Template:

```text
Create a realistic UGC product-demo video, [duration], vertical 9:16.

Subject:
[creator description] holding [product].

Action:
The creator [one clear action] while speaking one short line to camera.

Scene:
[real environment]

Camera:
RAW iPhone video, smartphone back camera, handheld chest-level framing, slight autofocus breathing, imperfect framing.

Lighting:
[practical light] from [direction], realistic shadows and natural skin texture.

Voice / dialogue:
Language: [language].
Accent: [accent].
Delivery: casual and conversational, not announcer-like.
Exact spoken line: “[short line]”

Audio:
Phone-recorded voice with natural room tone and subtle background noise.

Constraints:
No subtitles unless requested, no text overlays, no fake logos, no warped hands, no extra fingers, no plastic skin, no CGI look, no stock-video polish.

Output:
[duration], 9:16.
```

## Image-to-video

For image-to-video, the uploaded image defines the subject and scene. Do not redescribe the whole image unless the user specifically asks for changes.

Describe only:

* camera movement
* subject micro-motion
* lighting shift
* audio
* what must stay unchanged

Template:

```text
Animate the uploaded image into a realistic video, [duration], [aspect ratio].

Motion:
[one clear motion: slow push-in / steam rising / hair moving slightly / light shifting / hand lifting / product turning slightly]

Camera:
[subtle camera movement], stable and physically possible.

Lighting:
Preserve the original lighting direction. Add only a subtle natural light shift if needed.

Audio:
[ambient sound or no audio]

Preserve:
Keep the subject identity, background, clothing, product shape, labels, colors, composition, and camera angle unchanged.

Constraints:
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

Template:

```text
Create a realistic [style] video, [total duration], [aspect ratio], with [number] shots.

Overall look:
[realistic visual style, location, lighting, subject consistency]

Cut 1:
[wide or medium establishing shot, subject, one action]

Cut 2:
[closer shot, same subject, one action]

Cut 3:
[detail shot or reaction, one action]

Camera:
Natural camera movement, no impossible transitions.

Audio:
[ambient sound, voice, foley, music if needed]

Consistency:
Keep the same subject, wardrobe, environment, lighting direction, and color temperature across all cuts.

Constraints:
No teleporting, no outfit changes, no background changes, no warped hands, no fake text, no watermark, no CGI look.
```

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

For text overlays, specify:

* exact text
* timing
* position
* size
* style
* no extra words
* no misspellings

Example:

```text
Text overlay:
At 0:01, show the exact text “Websites for Local Businesses” in large white clean sans-serif text near the lower third. Keep it readable. No extra words, no misspellings, no duplicate text.
```

If the text is critical, consider generating video without text and adding the text in editing software.

## Common problems and fixes

| Problem                                | Likely cause                                         | Fix                                                              |
| -------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------------------- |
| Looks plastic                          | no practical lighting, too much “cinematic” language | add real light source, direction, no CGI look, no plastic skin   |
| Looks static                           | no clear action                                      | add one physical action and one camera move                      |
| Hands glitch                           | action too complex                                   | simplify to one hand action, slow movement                       |
| Lip sync is bad                        | dialogue too long or face not visible                | use one short sentence, medium close-up, face visible            |
| Voice sounds fake                      | vague voice instruction                              | specify language, accent, tone, pace, recording style            |
| Accent is exaggerated                  | prompt says only “Spanish accent” or “Latino accent” | specify natural, subtle, regional, not exaggerated               |
| Scene changes randomly                 | too many cuts or weak consistency                    | lock wardrobe, lighting, environment, subject                    |
| Image-to-video drifts                  | prompt redescribes image or changes too much         | describe motion only, add no identity/background change          |
| Product warps                          | too much motion or vague product lock                | preserve product shape, label, proportions, colors               |
| Audio feels detached                   | no room tone or foley                                | add ambient sound tied to scene                                  |
| Looks like an ad when it should be UGC | too polished                                         | RAW iPhone video, handheld, natural room tone, imperfect framing |

## Negative instructions

Use negatives based on the likely failure, not huge lists.

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

## Strong templates

### RAW iPhone UGC video

```text
Create a RAW iPhone-style UGC video, 6 seconds, vertical 9:16.

Subject:
[person description] in [real setting].

Action:
[one clear action] while [speaking / not speaking].

Scene:
[ordinary real environment, time of day, background details].

Camera:
Smartphone back camera, handheld chest-level framing, slight natural shake, slight autofocus breathing, imperfect framing, natural phone sharpness.

Lighting:
[practical light source] from [direction], realistic shadows, natural skin texture.

Motion realism:
Small natural body movement, realistic hand motion, natural blinking and breathing, no exaggerated gestures.

Audio:
Natural phone-recorded audio with light room tone and [ambient sound].

Voice / dialogue:
Language: [language].
Accent: [specific accent].
Delivery: conversational, natural, not announcer-like.
Exact spoken line: “[short line]”

Constraints:
No subtitles unless requested, no text overlays, no fake logos, no plastic skin, no warped hands, no robotic voice, no exaggerated accent, no CGI look, no glossy commercial style.

Output:
6 seconds, 9:16.
```

### Realistic talking-head video

```text
Create a realistic talking-head video, 6 seconds, vertical 9:16.

Subject:
[person description, wardrobe, expression].

Action:
The person speaks directly to camera with a relaxed posture, small natural nod, realistic blinking, and a slight breath before speaking.

Scene:
[real background] softly out of focus with ordinary details.

Camera:
Static smartphone back camera, eye-level medium close-up, natural phone sharpness, no dramatic camera movement.

Lighting:
Soft practical light from [direction], gentle shadows, realistic skin texture, no beauty filter.

Audio:
Clean but natural phone-recorded voice, subtle room tone, no music.

Voice / dialogue:
Language: [English / Spanish / bilingual].
Accent: [specific accent].
Delivery: [friendly / confident / calm / helpful], conversational, not announcer-like.
Exact spoken line: “[short sentence]”

Lip sync:
Face remains visible while speaking, natural mouth movement, small pauses, no exaggerated lip motion.

Constraints:
No subtitles unless requested, no text overlays, no watermark, no plastic skin, no robotic voice, no exaggerated accent, no distorted mouth.

Output:
6 seconds, 9:16.
```

### Spanish talking-head video

```text
Create a realistic Spanish talking-head video, 6 seconds, vertical 9:16.

Subject:
[person description].

Action:
The person speaks directly to the camera with a natural expression, relaxed posture, small head movement, and realistic blinking.

Scene:
[real setting], softly out-of-focus background, ordinary details.

Camera:
RAW iPhone-style video, smartphone back camera, eye-level medium close-up, slight handheld movement.

Lighting:
[practical light source] from [direction], realistic shadows, natural skin texture.

Audio:
Natural phone-recorded voice with subtle room tone.

Voice / dialogue:
Language: Spanish.
Accent: natural Mexican Spanish with [regional detail if needed], casual and conversational, not exaggerated.
Delivery: friendly, clear, natural pace.
Exact spoken line: “[short Spanish line]”

Lip sync:
Keep the mouth visible, natural mouth movement, small pauses, no overacting.

Constraints:
No subtitles unless requested, no text overlays, no watermark, no robotic voice, no exaggerated accent, no plastic skin, no distorted mouth.

Output:
6 seconds, 9:16.
```

### Product video

```text
Create a realistic product video, 5 seconds, [aspect ratio].

Subject:
[product description].

Action:
The product stays still while [one motion: slow camera push-in / slow orbit / steam rises / hand places it down].

Scene:
[real surface and background].

Camera:
[shot size], [one camera movement], stable and physically possible.

Lighting:
[soft window light / softbox / practical light] from [direction], realistic contact shadows and believable reflections.

Motion realism:
Subtle natural movement only. Preserve product shape, label placement, colors, packaging proportions, and texture.

Audio:
[subtle foley or ambient sound].

Constraints:
No fake text, no changed labels, no warped packaging, no duplicate products, no floating product, no CGI look, no glossy fake reflections.

Output:
5 seconds, [aspect ratio].
```

### Image-to-video

```text
Animate the uploaded image into a realistic video, 5 seconds, [aspect ratio].

Motion:
[one clear motion].

Camera:
[subtle push-in / gentle handheld drift / locked-off camera], physically possible and not distracting.

Lighting:
Preserve the original lighting direction with only a subtle natural shift.

Audio:
[ambient sound or no audio].

Preserve:
Keep the subject identity, background, clothing, product shape, labels, colors, composition, and camera angle unchanged.

Constraints:
No identity change, no background change, no new objects, no text distortion, no warped hands, no product deformation, no CGI look.

Output:
5 seconds, [aspect ratio].
```

## Final output behavior

Default response must be only one paste-ready prompt in a code block.

Do not include:

* scenario
* skill execution
* analysis
* explanation
* tutorial
* “here is your prompt”
* extra commentary

When multiple prompt options are useful, separate with short headers:

```markdown
## RAW iPhone version

[prompt]

## Talking-head version

[prompt]

## Image-to-video version

[prompt]
```
