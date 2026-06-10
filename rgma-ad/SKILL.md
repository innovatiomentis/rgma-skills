---
name: rgma-ad
description: "Generate Rio Grande Marketing Agency ad content — a fresh video concept derived from an offering or customer pain point, plus the script and captions. Use for any RGMA request — ad ideas, UGC video concepts, scripts, hooks, social content selling websites or website management, client launch posts. Input is a seed (offering, pain point, client launch, or vibe) or nothing. Output is 2–3 concepts with scripts and 3 caption variations. For AI generation prompts, hand off to the chatgpt-image-2 and seedance-2 skills; this skill decides WHAT to make, not how to prompt it."
---

# RGMA — Ad Concepts + Scripts from an Offering

Rio Grande Marketing Agency builds clean, professional websites for local businesses in Las Cruces, NM — $29/month management, local support, real ownership. This skill turns an offering, pain point, or client launch into video concepts, scripts, and captions. It does NOT write generation prompts — when a concept needs them, use `chatgpt-image-2` and `seedance-2`.

English by default; bilingual English/Spanish code-switching is on-brand for the Las Cruces market when the concept fits. Tone: direct, local, helpful, confident — never corporate, never desperate.

## Step 0 — One check before anything

**What's the seed?** An offering (e.g. monthly management), a pain point (e.g. slow site losing customers), a client launch (real client, real site), or nothing. If nothing, pick ONE offering and ONE pain that pairs with it — never sell everything in one ad.

## La línea: presentar sí, testificar no (HARD RULE)

AI characters may **present, demonstrate, and dramatize**. They may **never testify** — never pose as a real client with a fabricated business result.

- **PROHIBITED:** AI characters claiming client experience — "they built my site", "my bookings doubled", fake before/after results for a fake business, fake reviews.
- **ALLOWED:** a presenter speaking for the agency (reads as an ad — honest), characters dramatizing the PAIN (owner fighting a broken site at midnight — legible fiction), demonstrations, motion bumpers with real stats.
- **Client launches are the real-testimonial lane:** real client, real site, real link (like the Alma Artesanal post). Never invent one.

Test for every character line: *would a viewer take this as a real customer's real experience?* If yes → cut it.

## Step 1 — Think through the sale (in order, before any concepts)

1. **Who exactly:** which local business owner? (restaurant, salon, contractor, clinic...) Specific — "local businesses" is nobody.
2. **The moment of pain:** when do they FEEL it? (customer says "I couldn't find your hours", the 1am DIY session, the competitor's site looks better, the 8-second load that loses the sale.)
3. **The one promise:** which single RGMA value answers it — not stressing you out / not stuck alone / real ownership / local support / $29 affordability. One per ad.
4. **The virality lever:** what makes this spread or pull engagement, not just play? Pick one per concept:
   - Question hook that demands a self-answer ("Be honest — when did you last look at your own website?")
   - Shock-specific number ("Took eight seconds to load. They left.")
   - Free-value engagement bait ("Send me your link — I'll tell you what's killing it for free." → drives comments/DMs)
   - Deadpan gag (background chaos, presenter never breaks — the suppressed smile IS the joke)
   - Recognition/shareability (the owner tags their friend: "this is you")
   - Real transformation (client launch: the actual story, the actual site)

## Step 2 — Generate concepts (think, don't template)

Produce 2–3 concepts, each a genuinely different TYPE with a different lever. Each must be a realistic phone-filmable scenario.

**Script format (mandatory — this is what seedance-2 receives):**
```
Second X–Y: [Emotion + facial/body anatomy — "Playful, knowing — one eyebrow lifts on the question." / "Smile drops slightly, leveling with the viewer."]
Line: "[exact dialogue]"
```
Dialogue logic: **hook → value → detail → CTA.** Hook names a consequence or asks a question the viewer must answer — never a category claim. CTAs can vary by lever: "Get your website started today." / "Send me your link — free audit." Background gags get their own beat descriptions (candid, harmless, the presenter never turns).

## Step 3 — Captions (3 variations — RGMA voice, think first)

RGMA captions are multi-line with emojis as **visual punctuation at line ends** — not decoration spam. Structure:

```
[Hook line — echoes or extends the video's opening] [emoji]
[1–3 short value lines, emoji landing each beat 🌐 📍 💬 🙌]
[Tagline when it fits: Affordable websites. Local support. Real ownership.]
📞 (575) 496 6852
🔗 riograndema.com
[CTA line] 🚀
```

The contact block (📞 + 🔗) appears in EVERY caption. Mention $29/mo when price is the angle. Three variations, each a different angle:
1. **Hook extended** — the video's opening question/claim continued or twisted (👀 works here).
2. **Education/ownership angle** — teach one thing ("with builders you're essentially renting it"), then resolve with RGMA.
3. **Direct offer** — the $29/mo + what they get, calm and concrete.

For client launches: celebrate the client first (their story, their craft, their town), credit RGMA second, link THEIR site before yours.

Before writing, check: would the owner actually read it? does each line add (not describe the video)? friend-or-ad balance — warm is good, begging is not.
Prohibited: agency-speak ("elevate your brand", "next level"), "game-changer", begging ("please share"), explaining the joke.

## Brand DNA (constant, passed along when generating)

- Presenter wardrobe: clean white embroidered RGMA polo, red-and-teal logo on left chest. Logo is RENDERED in the chatgpt-image-2 first frame; the seedance-2 prompt locks it ("maintain exact polo and logo from input frame") — video never re-draws it.
- Brand colors for post/bumpers: teal #00665e dominant, gold #fdc95e accent, red #b52d04 punctuation. Font Garet — post only.
- Believability: realistic iPhone UGC, vertical 9:16, natural light, single continuous take for presenter concepts, subtle handheld. No on-screen text, no fake business names, no readable signs in generation — overlays in post.
- Las Cruces locality (adobe, Organ Mountains, desert light) available, not required.
- Constants: 📞 (575) 496 6852 · 🔗 riograndema.com · $29/mo · "Affordable websites. Local support. Real ownership." · "Get your website started today."

## Output format (per concept)

```
CONCEPT #X — [name] [lever]
Who + pain: [the specific owner and the moment]
Promise: [the one RGMA value this sells]
Scene: [realistic scenario — place, person, background action if any]
Script:
Second 0–2: [emotion/anatomy note]
Line: "..."
[continue beats through CTA]
On-screen (post): [overlay phrases for CapCut/AE]
Prompts: generar con chatgpt-image-2 + seedance-2.

Captions:
1. [hook extended]
2. [education/ownership]
3. [direct offer]
```

## Caption calibration (real posted captions — match this voice)

GOOD: "Your website might not really be yours 👀 / With Wix, GoDaddy, Squarespace, and other builders, you're essentially renting it. / At Rio Grande Marketing Agency, we build websites that your business can actually own 🌐 / No random support chat. No confusing process. Just a local team helping you build something that belongs to your business 📍"
Why it works: teaches one surprising thing, resolves with RGMA, emojis land beats — they don't decorate.

GOOD: "Need a website for your business? 🌐 / At Rio Grande Marketing Agency, we build professional websites and help manage them for only $29/month 🙌 / You also get someone actually local helping you, not a random support chat 💬"
Why it works: direct offer, concrete price, the local-vs-random-chat contrast does the selling.

BAD: "We build amazing websites! 🚀🔥💯 Elevate your brand to the next level! Game-changer alert!"
Why it fails: emoji spam with no beats, agency-speak, claims with no specifics.

## Self-check (silent, before answering)

1. Did I confirm or pick ONE offering + ONE pain (or a real client launch)?
2. Does each concept use a different type AND a different virality lever?
3. Does every AI-character line pass la línea? Is any testimonial-style content tied to a REAL client only?
4. Does each script use emotion/anatomy notes per beat and hook → value → detail → CTA?
5. Do all 3 captions follow the structure with the contact block, emojis as beats, distinct angles?
6. Is everything needing text overlays marked for post, not generation?

If any check fails, fix it before answering.
