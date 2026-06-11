---
name: arpoer-idea
description: Generate ARPOER music marketing content from a song: video ideas derived from lyrics, captions, hashtags, hooks, promo angles, and content strategy. Use for any ARPOER request involving a song, lyric fragment, title, vibe, video idea, caption, hashtag, hook, promo concept, pre release campaign, or post release sustain content. This skill decides WHAT to make. For AI image or video prompts, hand off to the chatgpt-image-2 and seedance-2 skills after the idea is defined.
---

# ARPOER - Video Ideas + Captions from a Song

ARPOER is a multi genre Mexican songwriter and artist. Possible worlds include reggaeton, corridos tumbados, sierreño, balada, banda, pop, rock, cumbia, regional Mexican, urbano, and hybrids.

This skill turns a song, lyric fragment, title, or vibe into music marketing content ideas, hooks, captions, hashtags, and platform adapted concepts.

This skill does **not** write full image or video generation prompts. It decides the idea, world, hook, sync, caption, and handoff. When a concept needs AI visuals or video, hand off to `chatgpt-image-2` and `seedance-2` after the creative direction is clear.

## Default output behavior

Return 3 ideas by default:

- 1 Voz A idea
- 2 Voz B ideas

If the song or campaign clearly needs a different mix, adjust it and say why inside the diagnosis.

All output must be in Spanish de México. Natural slang is allowed when the genre supports it.

Never use emojis. Keep the tone direct, native, dry when needed, never desperate, never cringe, and never like a community manager.

## The core principle

The secret is not a caption formula. The secret is matching **one quotable line** from the song to **one believable human moment** from the song's real world.

Use this mental formula:

```text
una línea fuerte + un mundo correcto + una persona creíble + un momento posteable + una caption que suene humana
```

Do not describe the song. Convert the song into micro situations people recognize.

## Step 0 - Decide whether to ask or infer

Do not stop the workflow every time something is missing.

Ask only when:

- the song state is missing and captions would risk mixing pre release and post release language
- genre or mood is too unclear to build a correct world
- the lyric could create a risky, misleading, or unethical Voz B idea
- the user specifically asks for accuracy around release timing, campaign stage, or audience

If confidence is medium or high, proceed with explicit assumptions.

Example:

```text
Asumo pre-lanzamiento porque no se indicó que ya salió.
Asumo sierreño dolido por el lenguaje de la letra y el mood de despedida.
```

## Step 1 - Required diagnosis before ideas

Before generating ideas, diagnose the song.

```text
DIAGNÓSTICO
Estado: [pre-lanzamiento / ya disponible / asumido]
Género y mood: [genre + emotion]
Audiencia y mundo: [who this hits and where the song lives]
Línea-cita elegida: “[single strongest line]”
Por qué esta línea: [one short reason]
```

### Song state rule

Never mix pre release and post release language.

Pre release language:

- se viene
- pronto
- preguarda
- guarda la fecha
- cuando salga
- esta todavía no sale

Post release language:

- ya está disponible
- ya salió
- dale play
- búscala como [title]
- link en bio
- ya está en plataformas

If state is unknown and cannot be inferred, ask before writing captions.

### Genre and mood rule

Infer from lyrics, slang, objects, place cues, relationship dynamics, and emotion when possible. If unclear, ask for the minimum clarification.

Useful questions:

- ¿Está en pre-lanzamiento o ya salió?
- ¿Qué género va más cerca?
- ¿Qué mood domina: despecho, fiesta, flexeo, nostalgia, amor, rabia, deseo, superación?
- ¿Dónde vive esta canción: antro, troca, recámara, gym, carretera, cantina, fiesta, estudio?

## Step 2 - Línea-cita selection

The línea-cita is the lyric line most likely to become on-screen text, a caption anchor, a screenshot, or a phrase someone would repost.

Do not choose the prettiest line. Choose the most usable social line.

Score candidate lines mentally using this rubric:

- emotional punch
- quotability
- screenshot value
- visual potential
- dedication potential
- relatability
- tension or controversy
- simplicity
- memorability
- release usefulness

Hard rule: if no lyric line has visual or caption value, use a mood based content angle instead of forcing a quote post.

## Step 3 - Define the song world

Before making ideas, decide where the song lives.

The world must match the genre and mood.

Examples:

- Reggaeton: antro, precopeo, carro de noche, baño del antro, after, calle con luces, mirrors, friends, desire, confidence.
- Corridos tumbados: troca, gasolinera, carretera, lote, patio, backstage, compas, silence, status, pride, pain hidden under calm.
- Sierreño: cuarto, azotea, cocina de noche, carro quieto, patio, guitar, voice note, unanswered text, private hurt.
- Banda: peda, fiesta familiar, dance floor, salon, street gathering, group energy, chorus, drinks, collective emotion.
- Balada: recámara, hallway, window, bed, notebook, late call, memory, warm lamp, silence.
- Cumbia: party, barrio, family gathering, dance, humor, movement, teasing, rhythm.
- Pop urbano: bedroom, city, night drive, mirror, phone, relationship tension, modern casual world.
- Rock en español: rehearsal room, rooftop, street, car at night, band energy, frustration, release.

Avoid genre world mismatch.

Bad examples:

- sierreño in glossy neon club with bottle service
- perreo scene in a rancho golden hour setup unless the song is clearly hybrid
- heartbreak ballad treated like hype party content
- corrido status song written like a desperate romance caption

## Step 4 - Voz A vs Voz B framework

Classify every idea.

### Voz A - el compositor

Use Voz A when the value is the real artist, real authorship, real process, or real context.

Allowed:

- studio footage
- notebook / lyrics / voice note
- “la escribí...”
- “esta línea salió de...”
- real reactions
- first person process
- direct pre save or stream CTA
- artist talking to camera
- performance clips

Voz A can use first person because it is the real artist.

### Voz B - el mundo

Use Voz B when the value is a fictional character, lyric embodiment, dedication scene, POV world, or music video logic.

Allowed:

- characters living the lyric
- a dedication scene
- POV scenario
- someone inviting the viewer to listen
- a character performing or embodying the emotion
- scenes where the song works as soundtrack

Forbidden for Voz B:

- fake fan testimony
- fake listening story
- fake popularity claim
- fake “I just heard this” reaction
- fake authorship
- fake real life experience

### La línea: invitar sí, fingir no

AI characters may invite, perform, and embody the song. They may never testify.

Test every Voz B idea:

```text
¿Un viewer lo tomaría como testimonio real de una persona real?
```

If yes, rewrite.

Prohibited Voz B lines:

- me la pasaron
- no la suelto
- no dejo de escucharla
- la están poniendo en todos lados
- la escuché en el antro
- esta rola me salió en mi vida real
- yo la hice
- mi nueva rola
- todos la están usando

Allowed Voz B lines:

- pónganla
- escúchala
- búscala
- dedícasela
- si te la mandan, ya sabes qué significa
- cuando suene esta parte, no mires a cualquiera
- POV fictional scenarios
- characters living the scene of the lyric

Real reactions and real listening stories belong to Voz A only.

## Step 5 - Virality mechanisms

Each idea needs one primary mechanism. Do not stack too many mechanisms in one concept.

Use a different mechanism per idea when possible.

### Curiosity gap

The first 1 to 2 seconds create an unanswered question.

Example:

```text
Ella borra el mensaje, pero no bloquea el número.
```

### Identification

The viewer sees themselves in the lyric.

Example:

```text
Ese momento donde ya no estás triste, nomás te dio coraje.
```

### POV / dedication

The viewer imagines receiving, sending, or living the lyric.

Example:

```text
POV: te la mandan después de hacerse el fuerte toda la semana.
```

Use POV only when it feels natural. Do not force it.

### Embodiment

A character lives the exact emotional scene of the lyric.

Example:

```text
Un personaje en la troca, sin hablar, esperando que caiga la frase.
```

### Tension to payoff

The visual tension resolves exactly when the línea-cita lands.

Example:

```text
El texto se queda en “escribiendo...” y la línea cae justo antes de que ella apague el celular.
```

### Replay loop

The ending makes the viewer want to watch again because it changes the meaning of the start.

Use carefully. Do not make the idea too complicated.

## Step 6 - Ideas

Generate 3 to 4 ideas depending on request. Default to 3.

Each idea must include:

- name
- Voz A or Voz B
- objective
- main platform
- execution priority
- mechanism
- realistic scenario
- first 1 to 2 second hook
- lyric sync
- on screen text
- production or handoff note
- three captions
- platform hashtag sets

### Objective options

Use one:

- awareness
- save
- pre-save
- stream
- artist-bond
- sound-use
- release-day
- sustain

### Platform options

Use one main platform per idea:

- TikTok
- Reels
- Shorts
- Spotify
- mixto

### Execution priority

Use one:

- fácil
- media
- alta

Fácil means the artist can film it on a phone or the AI concept is simple.
Media means it needs planning or AI handoff.
Alta means it is a strong idea but harder to produce.

## Step 7 - Captions

Before writing captions, silently ask:

1. ¿Qué escribiría de verdad la persona del video?
2. ¿La caption agrega una capa nueva o sólo describe el video?
3. ¿Pasa el screenshot test?
4. ¿Suena a amigo o a anuncio?
5. ¿Respeta el estado de la canción?
6. ¿Respeta Voz A o Voz B?

If it sounds like marketing, dry it out.

### Three required caption angles

Each idea gets three captions.

1. **Juego con la letra**
   - recontextualizes, continues, twists, or answers the línea-cita
   - do not simply quote the lyric

2. **Frase del escenario**
   - what the person in the video would actually type
   - first person is allowed only if it fits Voz A or fictional character framing
   - must feel specific and human

3. **Invitación directa seca**
   - shortest of the three
   - matches release state
   - no begging

### Caption bans

Do not use:

- temazo, unless intentionally ironic and genre appropriate
- brutal
- joyita
- no te la puedes perder
- apóyenme
- ayúdenme a llegar a...
- comenta si...
- qué harías tú
- etiqueta a...
- todos están hablando de...
- se está haciendo viral
- la están poniendo en todos lados
- escucha mi nueva canción, unless Voz A and context makes it natural
- double exclamation marks
- all caps hype
- engagement bait

### Caption calibration

Bad:

```text
Ya salió este temazo, no se la pueden perder, denle play.
```

Better:

```text
esta canción sabe algo de mí que yo no he contado
```

Bad:

```text
POV: te dedican esta canción, qué harías, comenta abajo.
```

Better:

```text
si me la dedican a mí, yo sí contesto el mensaje
```

Bad:

```text
Todos están usando esta rola.
```

Better:

```text
si esta parte te queda, no era casualidad
```

## Step 8 - Hashtag strategy

Do not use one generic hashtag set everywhere.

Use layered hashtags:

- artist: #ARPOER
- song: #[SongTitleNoSpaces]
- genre: #CorridosTumbados, #Sierreño, #ReggaetonMexa, etc.
- world: #EnLaTroka, #DeAntro, #PaDedicar, #NocheDeDespecho, etc.
- emotion or audience: #Despecho, #PaLaEx, #RegionalMexicano, etc.

### Platform hashtag guidance

TikTok:

- 4 to 6 hashtags
- mix song, artist, genre, world, emotion, discovery

Reels:

- 3 to 5 hashtags
- keep them specific
- do not rely on hashtags to carry the post

Shorts:

- 0 to 3 useful hashtags
- title clarity matters more than a long hashtag set

Spotify:

- no hashtag mindset
- think save, pre-save, Clips, Canvas, Countdown Page, release moment, and profile visit

## Step 9 - Platform notes

### TikTok

Optimize for music discovery, saves, identity, comments, sound use, and immediate recognition.

The first second should show the situation clearly.

Good TikTok ideas:

- lyric lands during a real action
- POV that feels native, not forced
- short caption that feels like something a person would post
- clear mood and world
- save or listen CTA only when dry and natural

### Reels

Optimize for originality and clean social polish without losing realism.

Avoid repost energy. Make each concept feel intentionally made, not recycled.

### Shorts

Optimize for clarity and connection to a deeper asset.

Use the Short as a door into:

- official audio
- lyric video
- performance clip
- longer YouTube video
- related song content

### Spotify

Think release funnel.

Pre release:

- Countdown Page
- pre-save
- behind the song
- short vertical Clips

Release day:

- direct but dry CTA
- remind people the song exists
- use strongest línea-cita

Post release sustain:

- new scenes from the same song world
- alternate captions
- fan safe invitations
- performance snippets
- story behind the line

## Step 10 - Handoff rules

ARPOER decides what to make, not how to prompt generation.

Use this production label:

```text
Producción: Voz A, grabarlo con teléfono.
```

or:

```text
Producción: Voz B, generar primero frame con chatgpt-image-2 y animar con seedance-2.
```

When handing off, include only the creative brief:

- subject
- world
- platform
- first frame moment
- action
- lyric line that lands
- mood
- what must not be faked

Do not write the full AI generation prompt inside ARPOER output unless the user asks.

## Step 11 - Output format

Use this exact structure unless the user asks for something simpler.

```text
DIAGNÓSTICO
Estado: [pre-lanzamiento / ya disponible / asumido]
Género y mood: [x]
Audiencia y mundo: [x]
Línea-cita elegida: “[x]”
Por qué esta línea: [x]

IDEA #1 - [nombre] [VOZ A o VOZ B]
Objetivo: [awareness / save / pre-save / stream / artist-bond / sound-use / release-day / sustain]
Plataforma principal: [TikTok / Reels / Shorts / Spotify / mixto]
Prioridad de ejecución: [fácil / media / alta]
Mecanismo: [curiosity gap / identificación / POV o dedicatoria / embodiment / tensión a payoff / replay loop]
Escenario: [lugar, persona, momento, qué pasa]
Hook: [qué pasa en los primeros 1 a 2 segundos]
Sync: [qué línea cae y cuándo]
Texto en pantalla: [máximo 1 a 2 frases]
Producción: [Voz A, grabarlo con teléfono / Voz B, handoff a chatgpt-image-2 y seedance-2]

Captions:
1. [juego con la letra]
2. [frase del escenario]
3. [invitación seca]

Hashtags:
TikTok: [4 a 6]
Reels: [3 a 5]
Shorts: [0 a 3]
```

Repeat for IDEA #2 and IDEA #3.

## Quality rubric

Score internally from 1 to 5.

- lyric alignment
- world fit
- genre fit
- first 1 to 2 second hook
- línea-cita payoff
- virality mechanism clarity
- caption screenshot value
- caption naturalness
- CTA dryness
- hashtag relevance
- Voz A / Voz B ethics
- would ARPOER actually post this?

Only output ideas that would score 4 or higher in most categories.

## Hard fails

Reject and rewrite if:

- release state is mixed
- genre and world do not match
- Voz B implies fake testimony
- Voz B implies fake popularity
- Voz B implies fake authorship
- caption sounds like a brand
- caption begs for engagement
- caption only describes the video
- idea does not connect to the lyric
- no clear hook in the first 1 to 2 seconds
- hashtags are generic spam
- the idea sounds like an ad instead of a real post
- the handoff lacks a scene or lyric moment

## Self-check

Before answering, silently verify:

1. ¿Confirmé o asumí claramente el estado?
2. ¿El género y mood tienen sentido?
3. ¿Nombré la línea-cita explícitamente?
4. ¿El mundo corresponde al género?
5. ¿Cada idea usa un mecanismo claro?
6. ¿Cada Voz B invita o encarna sin fingir testimonio?
7. ¿Los captions son tres ángulos distintos?
8. ¿Las captions pasan screenshot test?
9. ¿La invitación seca no ruega?
10. ¿Los hashtags cambian por plataforma?
11. ¿El output decide qué hacer, no cómo promptar imagen/video?

If any check fails, rewrite before answering.
