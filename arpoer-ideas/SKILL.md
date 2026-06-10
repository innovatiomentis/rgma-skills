---
name: arpoer
description: Generate ARPOER music-marketing content from a song — video ideas derived from the lyrics plus social captions. Use for any ARPOER request: video ideas, hooks, content for a song or lyric, captions, hashtags, or promo concepts. Input is a song (lyrics, fragment, title, or vibe). Output is video ideas (Voz A or Voz B) and 3 caption variations per idea. For AI generation prompts, hand off to the chatgpt-image-2 and seedance-2 skills — this skill decides WHAT to make, not how to prompt it.
---
# ARPOER — Video Ideas + Captions from a Song

ARPOER is a multi-genre Mexican songwriter/artist (reggaeton, corridos tumbados, sierreño, balada, banda, pop, rock, cumbia...). This skill turns a song into content ideas and captions. It does NOT write image/video generation prompts — when a Voz B idea needs them, use the `chatgpt-image-2` and `seedance-2` skills.

ALL output in Spanish (Mexico). Natural slang allowed. NEVER use emojis. Direct tone, never desperate, never cringe. Funny only if the lyric or genre supports it.

## Step 0 — Two checks before anything

1. **Song state.** Pre-lanzamiento or ya disponible? If not stated, ASK before writing any caption. Pre: "se viene", "pronto", "preguarda", "guarda la fecha". Post: "ya está en todas las plataformas", "dale play", "link en bio". Never mix.
2. **Genre + mood.** Never assume. Infer from lyrics/vocabulary/instrumentation if clear; if unclear or hybrid, ASK: genre? reference artists? where does this song naturally play? who's the typical listener? dominant emotion (fiesta, despecho, flexeo, nostalgia, amor, rabia)?

## La línea: invitar sí, fingir no (REGLA DURA para Voz B)

AI characters may **invite, perform, and embody** the song. They may **never testify** — never present a fabricated personal experience as real.

Test for every Voz B line and concept: *¿Un viewer lo tomaría como testimonio real de una persona real?* If yes → prohibited. If it reads as creative fiction or open invitation → allowed.

- **PROHIBIDO (testimonio falso):** "me la pasaron", "no la suelto", "no dejo de escucharla", "la están poniendo en todos lados", "la escuché en el antro", fake first-listen reactions framed as real, any fake fan review or popularity claim — and, as always, any authorship claim ("yo la hice", "mi nueva rola").
- **PERMITIDO (invitación / ficción legible):** "pónganla", "escúchala", "búscala", "dedícasela", POV scenarios, dedications, characters living a scene the lyric describes, scenes where the song plays as soundtrack — music-video logic, clearly creative.
- Real reactions and real listening stories belong to **Voz A only** (the real user). A Voz B character can vibe to the song in a scene; it cannot claim the experience was real.

## Step 1 — Think through the song (in order, before any ideas)

1. **Mood:** what feeling, what context, what audience does this hit?
2. **Línea-cita:** which single lyric line is the most quotable/shareable — the one people would put on screen or screenshot? Name it explicitly.
3. **World:** where does this song LIVE? Concrete places the listener would actually play it (antro, troca, recámara, gym, carretera, cantina, fiesta familiar). Lighting/color of that world. Who's in it, what they wear, what objects surround them. The world must match the genre — antro neón is not sierreño; rancho golden hour is not perreo.

## Step 2 — Generate ideas (think, don't template)

Produce 3–4 ideas. Each must be a REALISTIC scenario from the song's world — something that could genuinely happen and get filmed on a phone, not an ad. Drive each idea with a different virality mechanism:

- Curiosity gap (you must keep watching to resolve it)
- Identification ("esa soy yo" / "ese soy yo" — the lyric describes the viewer)
- POV / dedication (viewer imagines receiving or living the song)
- Embodiment (a character lives the exact scene of the lyric)
- Tension→payoff landing exactly on the línea-cita or the hardest verse moment

Hook in the first 1–2 seconds, always. The payoff syncs to the exact lyric fragment — state which lines play when. Every Voz B idea must pass la línea before it's proposed.

**Voz A vs Voz B — classify every idea.** Test: does the format imply authorship or real experience?
- **Voz A (el compositor):** the real user on camera — studio, notebook, "yo escribí", real reactions, first-person process. User films it himself; give phone-recording instructions. Strong CTAs allowed.
- **Voz B (el mundo):** AI fictional characters inviting or embodying. Credit always to ARPOER, never the character.

Default mix when user doesn't specify: 1 Voz A + 2–3 Voz B.

## Step 3 — Captions (proceso anti-cringe — think first, write after)

Before writing any caption, answer these for THIS idea:

1. ¿Qué escribiría de verdad la persona del video? Not a brand, not a community manager — the person.
2. ¿La caption agrega una capa nueva (segundo remate, contexto, continuación de la letra) o solo describe el video? Describing = rewrite.
3. **Screenshot test:** does the line stand alone as something worth reading without the video?
4. ¿Suena a amigo o a anuncio? If it sells, dry it out.

Three variations per idea, each a structurally different angle:

1. **Juego con la letra** — the línea-cita recontextualized, continued, or twisted. Not just quoted.
2. **La frase del escenario** — what the person in the video would actually type. First person, dry, specific.
3. **Invitación directa seca** — matching song state, zero begging, shortest of the three.

**Prohibido en captions:** hype genérico ("temazo", "brutal", "no te la puedes perder"), súplicas ("apóyenme", "ayúdenme a llegar a X"), explicar el chiste, signos de exclamación dobles, mayúsculas sostenidas, more than one sentence when one will do. If it needs two sentences, cut one.

5 hashtags per variation: mix ARPOER + song + genre + context + discovery. Vary across ideas — never one generic set.

## Output format (per idea)

```
IDEA #X — [name] [VOZ A o VOZ B]
Mecanismo: [which virality mechanism and why it fits this song]
Escenario: [the realistic scene — place, person, moment, what happens]
Sync: [which lyric fragment plays at which moment; where the línea-cita lands]
Texto en pantalla: [short on-screen phrases]
[Voz A → how the user films it. Voz B → "Prompts: generar con chatgpt-image-2 + seedance-2."]

Captions:
1. [juego con la letra] #x #x #x #x #x
2. [frase del escenario] #x #x #x #x #x
3. [invitación seca] #x #x #x #x #x
```

When in doubt about anything — ask before generating.

## Calibración de captions (contraste, no plantilla)

MAL: "Ya salió este temazo, no se la pueden perder, denle play"
BIEN: "esta canción sabe algo de mí que yo no he contado"
Por qué: el malo es hype de community manager; el bueno pasa el screenshot test y crea curiosity gap.

MAL: "POV: te dedican esta canción ¿qué harías? comenta abajo"
BIEN: "si me la dedican a mí, yo sí contesto el mensaje"
Por qué: el malo explica el chiste y mendiga interacción; el bueno es la frase que la persona del video escribiría.

## Self-check (silent, before answering)

1. ¿Pregunté o confirmé el estado de la canción?
2. ¿Pregunté o confirmé género/mundo?
3. ¿Nombré la línea-cita explícitamente?
4. ¿Cada línea de Voz B pasa la línea (invitar/encarnar, nunca testificar)?
5. ¿Cada idea usa un mecanismo de viralidad distinto?
6. ¿Las 3 captions son ángulos distintos y pasan el screenshot test, sin patrones prohibidos?
7. ¿Los hashtags varían entre ideas?

If any check fails, fix it before answering.
