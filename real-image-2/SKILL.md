---
name: chatgpt-image-2
description: "Write paste-ready prompts for ChatGPT Images 2.0 / GPT Image 2 that produce believable, realistic images instead of fake-looking AI visuals. Use this skill whenever the user asks for an image prompt, realistic photo prompt, RAW iPhone-style image, product image, ad creative, social graphic, poster, image edit, restyle, background generation, text-in-image layout, or a still image that may later be animated. The full method is in this file — ALWAYS read this entire skill before producing anything."
---

# ChatGPT Images 2.0 / GPT Image 2 Prompting Skill

Default output: give the user one clean, paste-ready prompt in a code block. No long explanation unless they ask.

Before writing, check `references/user-findings.md` for project-specific rules — they override anything below.

The goal is to create prompts that produce believable, usable images. Avoid the over-polished AI look. The best prompts describe what a real camera would see, including ordinary details, imperfect framing, real lighting, texture, shadows, grain, and compression.

## Core rule

Do not use lazy quality words as the main realism strategy.

Avoid phrases like:

- 8k
- ultra realistic
- hyper realistic
- masterpiece
- cinematic masterpiece
- insanely detailed
- award-winning
- perfect lighting
- flawless skin
- unreal engine
- octane render
- glossy commercial look

These broad quality terms tend to encourage over-polished, stock-like results.

Use the word photorealistic or phrases like "real photograph" or "taken on a real camera" to set the intended realism mode instead of piling on generic quality adjectives. Camera descriptors (for example, "iPhone photo," "35 mm lens feel," or "professional photography") should act as high-level style cues rather than literal optical specifications. Choose descriptors that fit the use case — professional photography might be appropriate for product or hero images, while candid phone shots demand casual capture language.

Instead, use grounded camera language:

- RAW iPhone photo
- smartphone back camera
- real candid frame grabbed from a phone video
- natural daylight
- practical indoor lighting
- low-light grain
- slight motion blur
- soft autofocus
- imperfect framing
- compression artifacts
- natural skin texture
- visible pores
- real shadows
- believable reflections
- ordinary background clutter
- no glamour retouching

## Decide the image type first

| Request looks like | Output type |
| --- | --- |
| Realistic person, lifestyle scene, candid moment | RAW iPhone / documentary prompt |
| Social ad or local business visual | realistic marketing prompt |
| Product photo or website hero image | product / hero prompt |
| Poster or graphic with words | exact-text layout prompt |
| Infographic or explainer | infographic prompt |
| Website, app, dashboard, mobile screen | UI mockup prompt |
| Edit an uploaded image | edit prompt |
| Extend, upscale, fix proportions, change background | image repair prompt |
| First frame for image-to-video | video-ready first-frame prompt |
| Character or repeated subject | consistency prompt |

## The structure that works

Use this order:

```
Create [specific image type] for [use case].

Main subject:
[who or what is in the image, with specific visible details]

Scene:
[real location, time of day, background, ordinary details]

Composition:
[camera distance, crop, angle, subject placement, negative space]

Lighting:
[real light sources, direction, shadows, reflections]

Camera / realism:
[camera type, lens feel, focus, grain, motion blur, compression, imperfections]

Text / product / brand requirements:
[exact text, locked product details, logo instructions, what must stay accurate]

Constraints:
[what to avoid]

Output:
[aspect ratio]
```

## How to make images look real

Realism comes from physical detail, not hype words.

Good realism details:

- what type of camera captured it
- whether it is front camera, back camera, or main camera
- time of day
- light direction
- real shadows
- imperfect framing
- background blur that makes sense
- motion blur when people are moving
- low-light grain when indoors or at night
- skin texture without retouching
- practical clutter in the background
- believable contact shadows under objects
- natural reflections on glass, metal, plastic, or wet pavement

Bad realism details:

- 8k resolution
- perfect lighting
- ultra sharp everything
- flawless symmetry
- polished skin
- dramatic cinematic color grading when the image should feel candid
- overly clean backgrounds when the scene should feel real
- too many adjectives without camera or lighting direction

## RAW iPhone style

Use this when the image should feel real, casual, social, candid, or user-generated.

Strong phrases:

- RAW iPhone photo
- vertical 9:16
- smartphone back camera
- real candid phone photo
- real frame grabbed from a phone video
- not posed
- not professional
- not commercial
- imperfect framing
- slight motion blur
- soft autofocus
- natural HDR
- low-light grain
- compression artifacts in shadows
- realistic skin texture
- no glamour retouching

Example style line:

```
Camera / realism:
RAW iPhone photo, smartphone back camera, 26mm equivalent lens, natural HDR,
slight phone sharpening, imperfect framing, realistic skin texture, no glamour
retouching.
```

For low light:

```
Camera / realism:
RAW iPhone photo, smartphone back camera, low-light grain, soft autofocus,
slight motion blur, compression artifacts in the shadows, mixed practical
lighting, imperfect framing.
```

Avoid combining RAW iPhone style with studio or luxury-commercial language.

Do not say:

```
RAW iPhone photo, cinematic masterpiece, 8k, ultra sharp, perfect studio
lighting.
```

That creates a confused prompt.

Note: camera specifications such as focal length, sensor type, or lens feel should be treated as broad style cues rather than literal technical requirements. Choose a small number of coherent descriptors (e.g., "main back camera," "35 mm lens feel") and avoid mixing conflicting camera modes.

## Documentary realism

Use this when the image should look like a real photo but not necessarily a phone shot.

Good phrases:

- documentary-style photo
- eye-level camera
- 35mm lens feel
- 50mm lens feel
- natural skin texture
- practical light only
- real background detail
- shallow depth of field
- soft natural shadows
- no glamour retouching
- slightly imperfect composition

Example:

```
Documentary-style photo, eye-level camera, 35mm lens feel, natural skin texture,
practical daylight only, soft background blur, slight imperfections in framing,
no glamour retouching.
```

## Product realism

Use this for e-commerce images, website hero images, product ads, packaging, food, and object scenes.

Always include:

- preserve product shape
- preserve label placement
- preserve packaging proportions
- realistic contact shadows
- believable scale
- no warped labels
- no fake text
- no extra products
- no melted or inflated packaging
- no impossible reflections

For product cutouts:

```
Plain white or other solid opaque background, crisp product silhouette,
realistic edges, no halo, no fringing, preserve product geometry and label
placement.
```

(Transparent backgrounds are not supported by GPT Image 2. Use an opaque background here and remove it later in post-processing if transparency is required.)

For product scenes:

```
Place the product on a real surface with believable contact shadows, natural
reflections, realistic scale, and subtle background detail. Do not change the
label, packaging shape, or product proportions.
```

## Website hero images

Hero images need room for layout and cropping.

Always state:

- 16:9 unless another ratio is requested
- subject on one side
- clean negative space on the other
- no text inside the image unless requested
- important details away from the edges
- usable as a website banner
- safe crop for desktop and mobile

Example:

```
Create a realistic website hero image, 16:9. Place the main subject on the right
third of the image, with clean negative space on the left for a website headline
overlay. Keep important details away from the top, sides, and bottom so it crops
safely on desktop and mobile. No text inside the image.
```

## Exact text in images

When text must appear in the image, keep it short and controlled.

Rules:

- quote every exact phrase
- label each text block by role
- use fewer words
- request large readable text
- say "render verbatim"
- say "no extra words"
- say "no duplicate text"
- avoid tiny legal copy

Example:

```
Exact text:
Headline: "YOUR WEBSITE SHOULD WORK FOR YOU"
Subheadline: "Professional websites for local businesses"
Button text: "Start Today"

Render all text verbatim. No extra words, no duplicate text, no fake logo, no
misspellings.
```

If the text is long, recommend shortening it. A realistic image with wrong text is not usable.

## Image edits

For edits, separate the change from what must stay locked.

Use this structure:

```
Edit the uploaded image by [specific change].
Preserve [locked elements] exactly.
Match the new area to the original image's perspective, scale, lighting
direction, shadows, reflections, focus, grain, and camera quality.
Do not add extra objects, fake text, watermarks, warped shapes, or unrealistic
shadows.
```

Example:

```
Edit the uploaded image by replacing the background with a realistic open field
during late afternoon.
Preserve the product exactly, including its shape, label, color, proportions,
and placement.
Match the new background to the original camera angle, depth of field, lighting
direction, contact shadows, and image quality.
No extra products, no fake text, no watermark, no warped packaging.
```

## Background generation

When adding or replacing a background, do not just say "make a realistic background."

Specify:

- location type
- time of day
- depth of field
- horizon height
- light direction
- surface the subject sits on
- contact shadows
- how much attention the background should take

Good example:

```
Add a realistic softly blurred field background at golden hour. Keep the product
as the clear focus in the foreground. The horizon should sit low in the frame,
with warm sunlight coming from camera-left. Add a believable contact shadow
under the product. The background should support the product, not distract from
it.
```

## Fixing proportions

Use when the user says the image looks warped, too wide, too tall, or the product changed.

Prompt pattern:

```
Adjust the proportions of the uploaded image so the subject looks natural and
physically accurate.
Preserve the product identity, label, colors, textures, and arrangement exactly.
Correct any stretched, inflated, compressed, warped, or oversized elements. Keep
realistic scale, perspective, shadows, and camera angle.
Do not redesign the product, do not add new objects, and do not change the
background unless needed to support the corrected proportions.
```

## First frames for image-to-video

A good video first frame needs depth and one clear motion cue.

Include:

- foreground
- midground
- background
- clean subject silhouette
- one visible motion cue
- believable camera path
- no text unless needed
- no watermark

Good motion cues:

- hair about to move
- fabric lifting
- dust in sunlight
- steam rising
- drink being raised
- papers mid-fall
- rain on pavement
- neon reflections shimmering
- confetti falling
- product slightly angled as if ready for a slow push-in

Template:

```
Create a video-ready first frame for an image-to-video clip.

Scene:
[subject and setting]

Composition:
[foreground, midground, background, clear subject silhouette, camera angle]

Motion cue:
[one visible motion element]

Lighting:
[realistic light source and direction]

Camera / realism:
[RAW iPhone, documentary, or cinematic camera details]

Constraints:
No text, no watermark, no distorted hands, no extra logos, no fake signage.

Output:
[aspect ratio]
```

## Negative instructions

Use negative instructions based on likely failure points. Short, targeted lists (around three to six items) are usually sufficient. Overly long catch-all blacklists can dilute the model's focus. Tailor the negatives to the specific scene rather than copying huge lists verbatim.

Useful negatives:

- no 8k
- no CGI look
- no plastic skin
- no airbrushed face
- no glamour retouching
- no stock-photo look
- no fake text
- no watermark
- no fake logo
- no readable fake signage
- no distorted hands
- no extra fingers
- no warped products
- no changed product labels
- no duplicate products
- no unrealistic shadows

## Aspect ratios

Always include an aspect ratio.

- 1:1: product square, e-commerce, social feed
- 4:5: Instagram feed portrait
- 2:3: poster, vertical editorial
- 9:16: Reels, Stories, TikTok, phone screenshot, UGC
- 16:9: website hero, video first frame, banner
- 4:3: editorial or traditional photo
- 3:4: vertical product or portrait

## Strong prompt templates

### RAW iPhone realistic photo

```
Create a photorealistic RAW iPhone photo, vertical 9:16, not a professional
photograph. It should look like a real candid frame grabbed from a phone video.

Scene:
[describe the real-life moment]

Main subject:
[person/object/action, clothing, expression, visible details]

Setting:
[real setting, time of day, background details]

Composition:
[distance, angle, crop, imperfect framing]

Lighting:
[practical light source, direction, shadows, reflections]

Camera / realism:
Smartphone back camera, 26mm equivalent lens, natural HDR or low-light grain
depending on the scene, slight motion blur, soft autofocus, imperfect framing,
compression artifacts, realistic skin texture, no glamour retouching.

Constraints:
No text, no watermark, no fake logos, no distorted hands, no plastic skin, no
cinematic color grading, no stock-photo look, no 8k.

Output:
9:16
```

### Realistic documentary photo

```
Create a photorealistic documentary-style photo for [use case].

Main subject:
[subject details]

Scene:
[location, time of day, ordinary background details]

Composition:
Eye-level camera, [35mm or 50mm] lens feel, [close-up / medium shot / wide
shot], subject placed [position], natural crop.

Lighting:
[real light source] coming from [direction], with realistic shadows and natural
contrast.

Camera / realism:
Natural skin texture, visible real-world texture, soft background blur, slight
imperfections in framing, no glamour retouching, no overly polished commercial
look.

Constraints:
No text, no watermark, no fake logos, no plastic skin, no stock-photo look, no
8k.

Output:
[aspect ratio]
```

### Product image

```
Create a photorealistic product image for [use case].

Main product:
[product details]

Composition:
[placement, camera angle, crop, negative space]

Surface / background:
[white background, real table, field, kitchen counter, etc.]

Lighting:
[soft daylight / softbox / window light] from [direction], realistic contact
shadows, believable reflections.

Product accuracy:
Preserve the product shape, label placement, packaging proportions, colors, and
texture. Keep the product physically accurate and not warped.

Constraints:
No fake text, no extra products, no changed labels, no warped packaging, no
melted shapes, no watermark, no 8k, no CGI look.

Output:
[aspect ratio]
```

### Website hero image

```
Create a photorealistic website hero image for [business/use case], 16:9.

Main subject:
[subject details]

Composition:
Place the main subject on the [left/right] third of the image with clean
negative space on the opposite side for website headline overlay. Keep important
details away from the edges so the image crops well on desktop and mobile.

Scene:
[realistic setting]

Lighting:
[real light source and direction]

Camera / realism:
[smartphone/documentary/product camera details], realistic shadows, natural
texture, no overly polished stock-photo look.

Constraints:
No text inside the image, no watermark, no fake logos, no warped products, no
unrealistic shadows, no 8k.

Output:
16:9
```

### Image edit

```
Edit the uploaded image by [specific change].

Preserve [locked elements] exactly, including [product/logo/face/background/
camera angle/composition].

Match the edited area to the original image's lighting direction, perspective,
scale, contact shadows, color temperature, focus, grain, and camera quality.

Do not add text, logos, watermarks, extra products, distorted shapes,
unrealistic shadows, or a CGI look.

Output:
[aspect ratio]
```

## Final output behavior

Default response should be only the prompt in a clean code block.

When multiple versions are useful, separate them with short headers:

```
## RAW iPhone version
[prompt]

## Product hero version
[prompt]

## Video-ready first frame
[prompt]
```

Do not include long explanations unless the user asks.
