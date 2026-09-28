---
name: ai-street-interview
description: Generate a complete Seedance 2.5 prompt for a hyper-realistic AI street-interview ad — the "stop a stranger, they complain about what they use now, product reveal, reaction, verdict" structure. Use when the user wants a street interview video, a man-on-the-street ad, a Seedance/AI UGC interview prompt, or says "make a street interview for [product]". Interviews the user for product details first, then outputs a single 30-second one-take prompt plus the timed dialogue script.
---

# AI Street Interview — Seedance 2.5 Prompt Builder

Single-file skill. Drop it at `~/.claude/skills/ai-street-interview/SKILL.md` (or a project's
`.claude/skills/…`) and it works as-is.

**Contents**
- [Part 1 — Operating Instructions](#part-1--operating-instructions)
- [Part 2 — Beat Structure](#part-2--beat-structure)
- [Part 3 — Realism Template](#part-3--realism-template)
- [Part 4 — Worked Example](#part-4--worked-example)

---

# Part 1 — Operating Instructions
Produces a **single 30-second, one-take Seedance 2.5 prompt** plus a **timed dialogue script**.

Output is the video prompt and script only. Captions and colour grading are post-production and are
deliberately out of scope — the prompt actively forbids the model from adding them.

## How to run this skill

1. **Intake** — ask the six questions in **Intake** below. Ask nothing else, ever.
2. **Derive the flip axis** — the single most important step. See **The flip axis**.
3. **Write the script** — plainest words first; see **Writing the dialogue**. Five beats to the timings in **Part 2 — Beat Structure**. Budget: **~95 words** — but write natural lines FIRST and cut whole lines to fit. Never compress.
4. **Assemble the prompt** — fill **Part 3 — Realism Template**. Copy the mandatory blocks verbatim.
5. **Self-check** — run **Final checks** before showing anything.
6. **Deliver** — the full prompt in one copyable code block, then the dialogue script.

Read **Part 4 — Worked Example** in full before writing your first one.

## Intake

Ask exactly these six questions. Nothing else.

1. **Product Name**
2. **Product description** — a brief description of your product including key benefits and features *(optional)*
3. **Main product benefit** — what makes your product special/different from the rest
4. **Main pain point it solves**
5. **Age/Gender/Ethnicity of the person being interviewed**
6. **Where can you buy the product + are you running any discounts on it**

**The product image has two audiences. Keep them separate.**

**To the user, in chat: never mention it.** Not in the questions, not in your notes, not as a helpful
reminder. Do not ask for it, do not tell them to upload one, do not explain what Seedance does with
it. They already know. Raising it only clutters the intake.

**To Seedance, inside the prompt: one line, no explanation.** PRODUCT CONTINUITY opens with
`[Product = the uploaded reference image.]` and that is all. Do not add "match it exactly", do not
explain what to do with it, do not justify why the packaging isn't described. Seedance takes the
reference image; it does not need to be told how.

Silent in the conversation, explicit in the prompt.

### How to use the optional description (Q2)

It is extra context, not extra claims. Read it for anything that makes a line land harder — a second
benefit, a use case, a phrase in the brand's own voice — and use it **only where it genuinely fits**.

> Q4 pain: "energy on the go". Q2 description mentions "all day energy". The subject can reasonably
> say *"that'd see me through the whole afternoon"* — because the description supports it.

**It does not license invention.** Everything still has to trace back to something the user wrote. If
the description adds nothing useful, ignore it — a forced extra benefit is worse than none.

### Then write the video. Do not ask anything else.

**Never ask a follow-up question.** Not about the street, the wardrobe, the weather, the packaging,
the tone of voice, what the person does with the product, or how they react. Every one of those is
yours to decide. The user answered the questions; the next thing they see is the finished prompt.

If an answer is vague, pick the most obvious reading and go. If a detail is missing, invent one that
fits. A confident guess you state in your notes is always better than a question.

**Decide these yourself, silently:** the street and city, the time of day and weather, the subject's
hair, skin, clothing and bag, the interviewer's voice, the wording of every line, the gestures and
micro-expressions, and what the subject physically does with the product.

**Pick the city yourself, and vary it.** Choose somewhere that fits the product and who buys it — a
US product gets a US street, a running product gets a park path or a riverside route. Never default to
the same place every time; if nothing about the brief points anywhere, pick a different major city
than you would have last time. Do not write "UK high street" unless the brief is British.

**Overcast is the one thing to keep.** It is not a style choice — flat diffused daylight kills the
specular highlights that make AI faces read as plastic. Hard sun is the fastest way to get rubbery
skin. Everything else about the location is yours to vary.
Refer to the product by a plain noun derived from question 1 — "the bottle", "the packet", "the tin".
Never describe its label, colour or logo in the prompt — a text description of packaging makes the
label garble.

## The flip axis

This is the engine of the format. One specific complaint gets inverted on one axis:

> "tastes like a lawn" → "tastes like candy"

**Q4 (pain point) is the failure. Q3 (benefit) is the inversion.** The pain beat comes from Q4 and nowhere else.

### First: invert the pain point into a failure

**Q4 usually arrives phrased as a benefit, not a pain.** Users write the thing their product delivers,
not the thing that hurts. You must flip it before you can write the pain beat — the failure is the
*absence* of what they wrote.

| Q4 as written | The failure it implies |
|---|---|
| "Fast energy on the go" | You're out, you're flagging, and there's nothing on you |
| "Keeps hair clean 3 full days" | It's greasy by day two and you're washing it every morning |
| "Saves you time in the morning" | You're doing it every day and it takes twenty minutes |

**Do not invent a different pain because it makes a neater flip.** If Q4 says "fast energy on the go",
the pain beat is about being caught out with no energy — *not* about energy gels tasting bad, however
much better that mirrors the reference video. Inventing a pain is the same failure as inventing a
benefit: the ad ends up selling something the user never claimed.

### Then

- The **pain beat** voices that failure in plain speech, unprompted, as something that happens to them.
- The **reaction beat** inverts *that exact axis* and nothing else. No praise for price, ingredients,
  or convenience — one axis, inverted once.
- The **verdict beat** restates the flip as resolved.
- The **hook** must set up the same axis, so the payoff can answer it back.

If Q3 gives you several benefits, pick the one that inverts Q4 and drop the rest. A script that lists
three benefits kills this format.

**The subject must never sound like they know the brand.** They complain about a *category*, and the
product happens to solve it. The instant the subject sounds informed, it reads as an ad.

## Writing the dialogue

**This is the part that decides whether the video works.** Everything else is scaffolding.

### Say the true thing plainly. Do not write jokes.

The reference video lives on five words: **"it tastes like a lawn."**

That is not a joke. It is the literal truth said casually — greens powder genuinely tastes like grass.
It lands *because* it is true and flatly stated, not because it is clever. And look at what follows it:
**"Like actual grass."** She says it, then says it again more plainly. That repetition is the sound of
a real person, and it is doing more work than any constructed line could.

**Never manufacture a metaphor.** The moment you reach for a clever image you get lines like *"by day
two you could fry an egg on it"* — which is not how anyone speaks and does not even make sense, since
frying needs heat, not grease. A forced joke is worse than a flat statement.

Method: name what literally happens, in the plainest words the person would use, then let them restate
it once.

| Copywriter | Person |
|---|---|
| "By day two you could fry an egg on it" | "It's greasy by day two. Like, wet-looking." |
| "It tastes unpleasantly vegetal" | "It tastes like a lawn. Like actual grass." |
| "Two washes and it's a crop top" | "It shrunk. Like, properly shrunk." |
| "I've aged waiting for it" | "It takes forty minutes. Every time." |

**The test is not "is this a good line."** It is: *would this person say this to a friend?* If it
sounds written, cut it.

### Underplay the performance, not the words

**The distinction that matters: dialogue can be warm, direction must be restrained.**

Enthusiastic *words* are fine and often right — *"Oh wow, these taste amazing"*, *"Amazing! Going to
order a few of these tonight."* People do talk like that when something surprises them. What makes a
generation read as fake is the **physical performance**: the model over-acting the line.

**Restrain the direction, leave the words alone:**

| Overplayed direction | Real |
|---|---|
| "eyebrows shoot up" | "eyebrows lift slightly" |
| "a big surprised laugh" | "a short breath out through the nose" |
| "grinning broadly" | "one corner of the mouth goes up" |
| "nodding enthusiastically" | "a single nod" |
| "gestures excitedly with both arms" | "lifts the packet slightly, then lowers it" |

**Rules:**

- **Gestures stay small and close to the body.** Never above shoulder height, never both arms wide.
- **One physical action and one micro-expression per beat.** Not per sentence, not per word.
- **Never write "delighted", "thrilled", "animated", "excited", "can't believe it"** into the ENERGY
  block or the beat direction. Those words are what the model over-acts.
- **The words carry the emotion; the body should not also carry it.** If the line is *"Oh wow, these
  taste amazing"*, the direction is *"eyebrows lift, he looks down at the packet"* — not a whole
  performance on top.

### Every line must earn its three seconds

You have ~95 words to sell a product. **Each line must do one of exactly four jobs:**

1. **Hook** — make them stop scrolling
2. **Pain** — make the viewer recognise themselves
3. **Sell** — name the product and what it does
4. **Act** — where to get it

**If a line does none of those four, cut it.** No exceptions, and especially not because the reference
video had something there.

| Cut it | Why |
|---|---|
| *"Oh, they're just sweets."* | Sells nothing. "Just" actively undersells the product |
| *"Can I keep these?" → "No chance."* | A joke from the reference. Funny there because she'd been converted; here it burns 6 words at the exact moment you should be closing |
| *"I'd get a lie-in every morning"* | About their life, not the product |
| *"Oh that's lovely. Really fresh."* | A reaction that reacts to nothing the viewer can verify |

**Do not import a beat from the reference because it was in the reference.** The keep-it joke, the
either/or, the taste test — each one has to earn its seconds on *this* product or it does not go in.

### Combine the reaction, verdict and payoff into ONE line

30 seconds does not have room for a separate reaction, a verdict and a payoff. Three short lines are
always weaker than one line doing all three jobs:

> *"Oh, that's actually nice. Yeah, I'd keep a pack in my bag — that's my three o'clock sorted."*

Reaction (*"that's actually nice"*), commitment (*"I'd keep a pack in my bag"*), payoff answering the
hook (*"my three o'clock sorted"*). One breath, one line, no filler between them.

### The close is the second most important line in the video

**"Amazon." is not a close.** A bare retailer name ends the ad on nothing — no product name, no
reason to act, no energy. The last three seconds are what the viewer leaves with.

**The close does three things, in this order:**

1. **Product name, said again.** Twice in 30s is the minimum — once at the sell, once at the close.
   The viewer must be able to type it into a search bar.
2. **Where, plus the offer if there is one.** With conversational padding: *"they're on Amazon"*,
   *"there's twenty percent off at the minute"* — not *"Amazon. Twenty percent off."*
3. **The subject's purchase intent, as the final line.** This is the close. The viewer's last input is
   a real person deciding to buy.

**The CTA is a spoken line like every other line. Pad it.** This is where compression creeps back in
worst, because it feels like information to deliver rather than something a person says. It is not.
She is answering a mate who just said they'd use the thing.

| Robot | Human |
|---|---|
| "SaltStick. They're on Amazon." | "Yeah, you can get them on Amazon — just search SaltStick." |
| "Amazon. Twenty percent off." | "They're on Amazon, and there's twenty percent off at the minute." |
| "That's Grüns." | "They're called Grüns, they're on Amazon." |

"Yeah", "you can", "just search", "they're called", "at the minute" — these are the words that make it
speech. Full-stop-separated fragments are how a machine reads out a product listing.

**Never end on a pleasantry.** *"Ah, cheers"*, *"thank you"*, *"amazing"* — these close the
conversation, not the sale. End on the subject committing to buy, delivered as they turn to walk off
holding the product.

### Resolve the product before they leave

**The subject must hand the product back as they go.** They were given it to try; it is the
interviewer's. Walking off with it leaves the prop unresolved and — more importantly — breaks the
logic of the close: *"I'm going to order some tonight"* makes no sense while carrying a packet they
just took.

**The handback IS the reason the closing line works.** He gives it back, so he has to buy his own.
Play it on the last line:

> *(hands the packet back as he turns)* "Amazing. Going to order a few tonight."

Then he walks past camera and out of frame, empty-handed.

**The only exception** is when the brief says the product is being given away — then the interviewer
says so out loud (*"keep that one"*) and the subject leaves holding it. Never leave it ambiguous: the
product either goes back or is explicitly given.

**The handback is a second handoff, so it carries the same continuity risk as the first.** It is
covered in PRODUCT CONTINUITY — the packet must stay visible and intact through the whole exchange.

### Never compress a line to hit the word budget

**This is the most common way this skill fails.** The budget tempts you to strip out "I", "it's",
"yeah", "and", "honestly" — and those words are exactly what makes speech sound spoken. A compressed
line is a written line.

| Compressed (written) | Padded (spoken) |
|---|---|
| "Bought a whole box. Can't get it down." | "Yeah, I've tried the gels. I can't get them down." |
| "Greasy by day two. Tried the oily ones, nothing." | "It's greasy by day two. I've tried the ones that say oily hair, they don't do anything." |

**Look at the reference.** The Grüns pain beat is **33 words** — longer than anything you will write:

> *"Oh I've tried them. I bought the big tub, did the whole shaker thing. It tastes like a lawn. Like
> actual grass. I used it maybe four times and it's just been sitting there."*

It sounds real *because* it rambles. "Oh", "I bought", "did the whole", "and it's just been". If you
copy its four-part structure but halve the words to fit the budget, you get telegraphic writing —
four clauses with the humanity squeezed out. **Take the rambling OR the brevity. Never a compressed
imitation of the ramble.**

**When you are over budget, delete a whole line. Never squeeze the words out of a line that stays.**
Two natural clauses beat four clipped ones. Cutting the interviewer's second setup question, or a
reaction line, costs you nothing; making every line 20% terser costs you the whole video.

Write each line the way the person would actually say it. Count afterwards. If it is over, find a line
to cut entirely and leave the rest alone.

### The reveal has to actually sell the product — using ONLY what the user gave you

**Every product claim in the script must come from the user's answers. Never invent one.** Not an ingredient, not a benefit, not a duration, not an objection-handler. If the user did not
say it, it does not go in the video. Inventing *"and it won't dry your scalp out"* is fabricating a
claim about a real product being advertised — it is not a stylistic liberty.

If their answers are thin, use fewer words. Never pad with invented benefits.

**The formula:**

> `"Have you tried [PRODUCT NAME]? It contains [INGREDIENT] that [BENEFIT — their words]."`

Worked from a real brief:

| Their answer | |
|---|---|
| Q1 name | Tea Tree Special Shampoo |
| Q3 benefit | Organic tea tree oil from Australia, gets rid of oily hair, keeps hair non-greasy |
| Q4 pain | Keeps hair clean and fresh up to 3 full days |

> *"Have you tried Tea Tree Special? It contains organic tea tree oil that keeps your hair non-greasy
> for up to three days."*

Every word of that is theirs. Nothing added.

**Name the product first.** *"This one keeps it clean"* wastes the most important line in the video on
a pronoun. The viewer must leave knowing what it is called.

**Bind the ingredient to the benefit in the same clause.** `contains X that does Y`. A stranded
ingredient — *"Australian tea tree oil."* as its own sentence — means nothing to a viewer, because
nobody buys oil. The same words work when the benefit is attached to them.

| Stranded, means nothing | Bound to the benefit |
|---|---|
| "Australian tea tree oil." | "…contains organic tea tree oil that keeps your hair non-greasy." |
| "Contains hyaluronic acid." | "…contains hyaluronic acid so it stops going tight after you wash it." |

**Then every line after it must promote or react to the product.** No lifestyle asides.

### The ending depends on whether she actually used it

**"Can I keep this?" → "No." only works if she has used and loved the product.** In the reference she
has eaten the gummy — wanting to keep it is an endorsement earned on camera, and the refusal is funny
because she means it.

If she has only been *told* a claim, that exchange is unearned and lands as nothing. **Default ending
for anything she can't test on the street: the interviewer gives it to her.**

> *"Where do I get it?"* → *"Amazon. There's twenty percent off at the minute."* → *"Keep that one."*
> → *"Oh amazing — thank you!"*

She walks away pleased, holding the product. That is a warmer close than the joke and it earns itself.

**They keep walking the way they were already going.** At the hook they were walking toward the
camera; at the close they carry on past it and out of frame, the way anyone does after being stopped
for thirty seconds. They do **not** turn around and head back the way they came — that is the single
clearest tell that the scene was staged, because nobody does it in real life.

Practically: he steps past the lens and exits frame left or right, passing close to camera as he goes.
The frame holds on the empty street for a beat. Hard stop.

**Give the CTA conversational padding.** *"Amazon. Twenty percent off."* is a price tag read aloud.
*"Amazon. There's twenty percent off at the minute."* is a person answering a question. The words
"there's", "at the minute", "right now" are what make it speech.

### Never force the template onto a product it doesn't fit

**The "but" needs a real surprise.** `"These are your daily greens — but they're gummies"` works
because greens-as-candy is genuinely unexpected. `"That's a shampoo — but it lasts three days"` is
nonsense; shampoo-as-shampoo is not a twist. **If the product isn't a format flip, drop the "but" and
just state the claim:** *"Try this one. It's meant to last three days."*

**The either/or needs two real things — but the verdict beat itself is never optional.** This beat is
the endorsement: the moment the subject commits on camera. It is the most valuable thing in the ad.
Never cut it. Only the framing changes:

| Situation | Ask |
|---|---|
| Two distinct objects to compare | `"Powder or these?"` |
| No object comparison (shampoo, mattress, service) | Ask for a commitment — `"Would you switch?"` / `"Would you actually buy that?"` |

`"Yours or this?"` — a bottle against an unnamed bottle — is the failure case. If you cannot name both
sides, ask for the commitment instead. Do not drop the beat.

**The verdict must be decisive, and concrete beats hypothetical.** The reference lands *"These. Not
even close."* — flat, certain, no hedging. A conditional verdict is a weak verdict.

| Weak | Strong |
|---|---|
| "Yeah, I'd probably try it" | "100%." |
| "I'd not be washing it every day then, would I" | "Every day down to twice a week — I'd take that." |
| "That would be good" | "Not even close." |

**Numbers are the strongest form.** *"Every day down to twice a week"* states the change as a
measurable before-and-after, which is both a stronger endorsement and a clearer product claim than any
adjective. Where the hook question involved a number or a frequency, make the payoff answer it with a
number.

**Then the payoff line closes back to the hook question.** This is the strongest line in the format:
the subject diagnoses themselves using the product.

> Hook: *"Did you eat any vegetables yesterday?"* → Payoff: *"If vegetables tasted like this I wouldn't
> have this problem."*
> Hook: *"How often do you wash your hair?"* → Payoff: *"I'd not be washing it every day then, would I."*

Write the hook and the payoff as a pair. If the payoff does not answer the opening question, it is a
lifestyle aside and it is wrong — *"I'd get a lie-in every morning"* is about her bed, not the product.

**The CTA has to be motivated, not announced.** Nobody says *"That's Tea Tree Special — Amazon,
twenty percent off"* out of nowhere; that is an ad read. But the subject does not need to ask for it
either — that costs five words you do not have.

**The trigger is their expressed interest.** The moment they say they would use it, the interviewer
answers with where to get it. It reads as a natural reply rather than a plug:

> *"I'd keep a pack in my bag."* → *"SaltStick. They're on Amazon."* → *"Awesome, I'm going to order
> some today."*

A "Where do I get it?" line is only worth its seconds if nothing before it has signalled interest.
If the reaction beat already contains a commitment, cut the question.

### How people actually talk

- **Short.** Most lines are three to eight words.
- **Fragments, not sentences.** *"Every day. I have to."*
- **They restate.** *"It's greasy. Like, wet-looking."* — the second half is plainer than the first.
- **"Like" and "just" and "actually"** carry the rhythm. Real speech is padded.
- **They repeat the surprising number back.** *"Three days?"*
- **Nobody explains the product.** No benefit phrases, no brand names, no "formula", no "strips it".
  They say what happens to them.
- **Read every line out loud.** If you would not say it to a stranger who stopped you, rewrite it.

### Direction: less than you think

Give each beat **one** physical action and **one** micro-expression. That is the whole budget.

Do not choreograph every word. A paragraph of per-syllable gesture notes competes with the dialogue
and the camera for the model's attention, and in a 30-second two-hander it tends to come back twitchy
and over-animated. Direct the moments that carry meaning — the pause before the reaction, the hand
going to her own hair, the turn away at the end — and let the model handle the rest.

*(Deliberate deviation from the source template's "one gesture and one micro-expression per sentence",
which was written for a seated single-speaker piece where one person talks for the whole runtime.
Applied per-sentence across two speakers here, it over-drives the take.)*

## Structure

Follow **Part 2 — Beat Structure**. Summary of the 30s spine:

| Time | Beat | Job |
|---|---|---|
| 0.0–3.5 | Hook | A yes/no question the subject loses. Sets up the axis the payoff will answer |
| 3.5–13.0 | Pain | One rambling answer: admits it, then the Q4 failure as something that happens to them |
| 13.0–18.0 | Sell | Product NAMED + benefit, built only from the user's answers |
| 18.0–24.5 | Reaction + verdict + payoff | ONE line: reacts, commits, answers the hook |
| 24.5–30.0 | Close | Product NAMED again + where + offer. Ends on their purchase intent, product handed back, walking PAST camera out of frame |

**Five beats, not seven.** Thirty seconds cannot hold more. The reference runs 46s and multi-cut —
if you try to fit its full beat list into one 30s take, every beat comes out too short to land and
the whole thing says nothing. Merge before you compress.

**Name the product at the reveal.** Say it by name the moment it enters frame, and again at the CTA.
This is an ad — the viewer has to leave knowing what it is called. Never write "this one", "this",
or "these" where the product name belongs; a pronoun at the reveal wastes the most important line in
the video.

The *subject* still never uses the brand name before it is handed to her — she has never heard of it.
Only the interviewer names it.

## Assembly

Fill every `[BRACKET]` in **Part 3 — Realism Template**. Then:

- Copy **ANTI-GLITCH**, **PRODUCT CONTINUITY**, and **ABSOLUTE NOs** verbatim. Never edit or trim them.
- Scale blinks to length: **6–10 blinks** across 30 seconds.
- **One** physical action and **one** micro-expression PER BEAT — not per line, not per word. Say where
  the hand lands afterward. Over-direction fights the model; see **Direction: less than you think**.
- The take is continuous. No cuts, no zooms, no reframing anywhere in the prompt.

## Final checks

Do not deliver until all pass:

- [ ] You asked no question beyond the six, and never mentioned the product image TO THE USER
- [ ] The PROMPT does state the reference image, in the PRODUCT CONTINUITY block, verbatim
- [ ] The complaint is plain and literally true, then restated once — no manufactured metaphor
- [ ] No line sounds written. Read them out loud
- [ ] Every line does one of: hook / pain / sell / act. Anything else is cut
- [ ] The close names the product AGAIN and ends on the subject saying they will buy it
- [ ] The product is handed BACK on the closing line (or explicitly gifted) — never walked off with
- [ ] The video does NOT end on "cheers" / "thank you" / any pleasantry
- [ ] Reaction, verdict and payoff are ONE line, not three
- [ ] No beat included merely because the reference video had it
- [ ] No line was compressed to fit the budget — "I", "it's", "yeah" left in. Over budget means DELETE A LINE
- [ ] EVERY product claim traces back to an answer the user gave — nothing invented
- [ ] The PAIN BEAT is the inversion of Q4 (the pain point) — not a different pain you preferred
- [ ] Reveal follows "Have you tried [NAME]? It contains [X] that [BENEFIT]" — ingredient bound to benefit
- [ ] The verdict is decisive and ideally numeric — no "probably", no conditionals
- [ ] Every line after the reveal promotes or reacts to the product; no lifestyle asides
- [ ] The verdict beat is present — subject commits on camera. Never cut, only reframed
- [ ] The payoff line answers the hook question back
- [ ] "Can I keep it?" used ONLY if she physically used the product; otherwise the interviewer gives it to her
- [ ] No forced "but", no fake either/or. CTA is motivated by expressed interest, not announced
- [ ] Every line reads out loud like something a stranger would actually say
- [ ] One action + one micro-expression per beat, no per-word choreography
- [ ] Direction is restrained — no "shoots up", no grinning, no big gestures. Warm WORDS are fine
- [ ] One flip axis, stated, inverted once, never diluted with other benefits
- [ ] Dialogue ≈ 95 words total (85–95 is the target band), and you have counted them (script only, excluding stage directions)
- [ ] Product NAMED at the reveal and again at the CTA — never "this one" or "this"
- [ ] Subject never says the brand before it is handed to her
- [ ] Both speakers labelled — `INTERVIEWER (off-camera)` / `SUBJECT (on-camera)`
- [ ] Packaging NOT described — product referred to only by a neutral noun, no label text in the prompt
- [ ] The three mandatory blocks present and unmodified
- [ ] Prompt says: no captions, no music, no cuts, no grading
- [ ] Applying the FINAL TEST in the template, it would PASS

## Delivery

Output in this order, nothing else:

1. **The Seedance prompt** — one fenced block, ready to paste.
2. **The dialogue script** — a table of time, speaker, line, word count.
3. **Notes** — max 3 bullets: the flip axis you used and any assumption you made on the user's behalf.
   Never mention the product image to the user (it still appears inside the prompt).

---

# Part 2 — Beat Structure

Derived from frame, audio and colour analysis of the Grüns reference (46s, 9:16, 1080x1920).
Compressed to 30s for a single Seedance 2.5 take.

### Why 30s works

The reference runs 46s and carries ~120 words. Cutting the interviewer's redundant second setup and
one repeated reaction line fits the five beats into **~95 words**. With a required ~1.5s silence at
the reaction, that's ~3.1 words/sec of actual speech — the upper end of normal conversation, which is
right for someone talking fast because they've been stopped in the street.

**Aim for 85–95 words.** Past that the pauses get squeezed out, and the pauses are what sell it.

### The beats

#### 0.0–3.5s — HOOK
**Interviewer, off-camera.** A yes/no question the subject is going to lose. The subject is walking
toward camera and stops when addressed.

**Do not use the same opener every time.** "Excuse me — quick question, be honest…" is one shape, not
the shape. If every video you make opens identically, your variants are competing with each other for
the same three seconds. Vary it:

| Shape | Example |
|---|---|
| Permission to fail | "Be honest — did you [do the thing you should have]?" |
| Straight frequency | "How often do you [X]?" |
| Assumed yes | "You crash in the afternoon, right?" |
| Confession bait | "When did you last [X]? Actual answer." |
| Direct challenge | "Bet you can't remember the last time you [X]." |

What matters is not the wording — it is that the question is closed, the subject loses it, and the
payoff can answer it back. Pick a different shape each time.
Camera holds wide as they approach, settles to medium as they stop.

#### 3.5–8.0s — ADMISSION
**Subject.** Loses immediately, with a laugh or a wince. Then the interviewer sets up the category
with a second question.

Formula: `"[Beat.] Honestly? No. Like — genuinely no."` → `"Have you ever tried [OLD THING]?"` — or, if the old thing is one they already own: `"Is that one of the ones that [FAILURE]?"`

Here the interviewer names the *category* only — the brand arrives at the reveal.

#### 8.0–14.0s — PAIN  ← the longest beat, and the reason the ad works
**Subject.** Volunteers a story about buying the old thing and abandoning it. Must contain:
1. **Proof of purchase** — they bought it, so they're not a hater ("I bought the big tub")
2. **The ritual** — the effort it demanded ("did the whole shaker thing")
3. **The physical failure** — sensory, specific ("it tastes like a lawn. Like actual grass")
4. **The abandonment** — the guilt-object still sitting there ("used it maybe four times")

This is the most physically animated stretch. Gestures big, exasperated, hands wide.

> In the reference, this beat is **graded near-greyscale** — measured saturation drops from ~7.5 to
> ~1.4 between 12.8s and 19.3s, then spikes to ~17 at the reveal. That is a post effect. Do **not**
> ask Seedance for it; the prompt forbids grading. Note it for the user's editor if they want it.

#### 14.0–18.0s — REVEAL
**Interviewer's hand enters frame** holding the product, offers it. One line that gestures at the
difference without naming the brand.

Formula depends on whether the product is a genuine format surprise:
- **Real twist** (greens → gummies): `"So these are your [CATEGORY] — but they're [TWIST]. Try them."`
- **No twist** (shampoo → shampoo): drop the "but" and just state the claim — `"Try this one. It's
  meant to [USP]."` Forcing a "but" onto a product that isn't a twist produces a nonsense line.

**The more ordinary the product, the fewer words here.** A pitch line on a parity product is exactly
what makes it read as an ad. Hand it over and let the next beat do the work.

The package fills roughly a third of the frame, front toward camera, in focus, held still long enough
to read. Hardest thing in the take for the model to render — see PRODUCT CONTINUITY.

Subject takes it and examines it. Do not rush this.

#### 18.0–22.5s — REACTION
The subject reacts. **Two ways to play it. Pick one yourself — never ask.**

**Verbal — the default, and right for most products.** They react to the claim they were just told,
while holding the product. Nobody washes their hair, tests a mattress, or installs software on a
pavement, and a real street interview never asks them to. The reaction is to the *information*.

> Shampoo: *"Three days? Mine's greasy by day two."*
> Mattress: *"That's the one off the adverts? And it just… rolls up?"*

**Physical — only when the product genuinely works in four seconds on a street.** Food, drink, a
texture, a smell, something you hold or stretch. Then they use it and react to what they got.

> Gummies: they eat one, pause, *"that tastes like sweets."*
> A t-shirt: they stretch the collar, *"that's actually thick."*

**If in doubt, go verbal.** A forced demo is the fastest way to make this look staged. The format is
carried by the conversation, not by a product demonstration.

Whichever mode: **a real pause before the line lands.** Eyes going somewhere else while they process,
then the read. The reference leaves ~1.5s of near-silence here and it is the most convincing moment
in the video.

Formula: `"Wait — [pause] that's actually [FLIP]."` — the flip inverts the Q3 pain point and nothing
else. No praise for price, ingredients, or convenience.

#### 22.5–27.0s — VERDICT
**Interviewer forces a binary.** No open questions — a choice.

Formula: `"So, real talk: [OLD THING] or these?"` → `"These. Not even close. If [CATEGORY] [FLIPPED
QUALITY], I wouldn't have this problem."`

**This beat is never cut — it is the endorsement.** Only the framing changes. With two distinct
objects, ask the either/or: *"Powder or these?"* With no object comparison, ask for a commitment:
*"Would you switch?"* → *"Yeah. Honestly, yeah."*

**The payoff line must answer the hook question back.** That loop closing is the strongest line in the
format — the subject diagnoses themselves. *"How often do you wash your hair?"* → *"I'd not be washing
it every day then, would I."* A payoff that does not answer the hook is a lifestyle aside and is wrong.

That last clause closes the loop back to the hook question. It is the strongest line in the format —
the subject diagnoses themselves.

#### 27.0–30.0s — BUTTON + BRAND + CTA
Comedy beat, then the brand, where to get it, and the discount if there is one — the first and only
time any of it is said.

Formula depends on whether she physically used the product.

**She used it** (food, drink, texture — she has a real verdict): the keep-it joke is earned.
`"Where do I get it?"` → `"[WHERE]. [DISCOUNT] at the minute."` → `"Can I keep this?"` → `"Absolutely not."`

**She only heard the claim** (shampoo, mattress, software — the common case): drop the joke, because
wanting to keep something she has not tried is unearned. The interviewer gives it to her instead.
`"Where do I get it?"` → `"[WHERE]. [DISCOUNT] at the minute."` → `"Keep that one."` → `"Oh amazing — thank you!"`

She walks away pleased, product in hand. Warmer than the joke, and it earns itself.

**They keep walking the way they were already going.** At the hook they were walking toward the
camera; at the close they carry on past it and out of frame, the way anyone does after being stopped
for thirty seconds. They do **not** turn around and head back the way they came — that is the single
clearest tell that the scene was staged, because nobody does it in real life.

Practically: he steps past the lens and exits frame left or right, passing close to camera as he goes.
The frame holds on the empty street for a beat. Hard stop.

Give the CTA conversational padding — *"there's twenty percent off at the minute"*, not *"twenty
percent off"*. The first is a person answering; the second is a price tag read aloud. If there is no
discount, drop it. This works because she asked for it.

### Camera arc across the single take

No cuts. The operator's own movement does the work:

- **0.0–3.5** — wide, subject approaching down the street, full body
- **3.5–14.0** — settles to medium, chest-up to waist-up, handheld drift
- **14.0–18.0** — operator's free hand enters frame with the product; slight lean in, package close
- **18.0–27.0** — medium, product in subject's hands and visible in frame throughout
- **27.0–30.0** — subject continues PAST the camera and exits frame; operator holds on the empty street

The walk-in / walk-past bookend closes the loop and gives a clean end frame. He never doubles back.

### Roles

Two voices, one body on camera. The interviewer is **voice and one hand only** — never framed, never
described as a visible person. The camera is their point of view.

---

# Part 3 — Realism Template

Adapted from the source UGC realism template (built for seated indoor selfie UGC) for outdoor
two-person street interviews. Deviations from the source are marked **[ADAPTED]** with the reason.
All unmarked rules are carried over unchanged and must not be edited.

Replace every `[BRACKET]`. Delete nothing.

---

### HEADER

**Format:** 9:16 vertical
**Length:** 30 seconds, ONE CONTINUOUS TAKE — no cuts
**Capture Device:** a recent phone's **rear** camera, handheld by a person standing about 1.5m from
the subject `[name a specific current phone; vary it, don't use the same one every time]` **[ADAPTED — source assumes front/selfie camera; a street interview is shot by an operator]**
**Style:** Authentic street-interview UGC (NOT influencer content, NOT an ad)
**Location:** `[STREET — city, street type, what's behind the subject]`
**Time:** `[TIME OF DAY + LIGHT — default: overcast midday, flat diffused daylight, no direct sun]`

---

### CAMERA & RECORDING STYLE (CRITICAL)

Camera is at the operator's chest height, angled very slightly upward at the subject, tilted a degree
or two off level. Handheld, never tripod-perfect.

`[FRAMING — default: medium, chest-up to waist-up, subject slightly off-centre [left/right]. The
street recedes behind them with real depth — traffic, shopfronts, passersby walking through the
background at their own pace.]` **[ADAPTED — source specifies waist-up over a table with foreground
clutter; outdoors, depth comes from the street behind, not objects in front]**

The subject's eyeline is on the **interviewer standing just beside the lens** — not into the lens
itself. Natural, sustained, with quick glances away when searching for a word, then back.
**[ADAPTED — source calls for dead-centre FaceTime eye contact; in a real street interview the
subject looks at the person, and locking to the lens is the single biggest tell that it's staged]**

Constant handheld micro-shake from the operator breathing and shifting weight. Small natural drift
and re-centring as the subject moves. **No stabilisation. No zooms. No reframing. No cuts.**

The camera is the operator's point of view — it does not exist as a visible object in the scene.

---

### LIGHTING (NON-NEGOTIABLE)

`[PRIMARY LIGHT — default: flat overcast daylight from directly above, no visible sun, no hard
shadows. Soft downward shadow under the brow and jaw. One side of the face marginally brighter from
skylight bouncing off the building on that side.]`

No glow. No warmth filter. No beauty lighting. Visible skin texture. Slight iPhone sensor grain in the
shadow areas of the face and in the darker parts of the street.

Overcast is the default deliberately: hard sunlight produces specular highlights on skin that AI video
renders as plastic. If the user wants sun, use late-afternoon backlight with the face in open shade.

---

### SETTING

`[3–5 specific, unglamorous details that belong to THIS city — not a generic street. Fire escapes and
a hydrant read as US; scaffolding and a bus stop read as British; awnings and scooters read as
southern European. Pick details that match the location you chose, and use different ones each time.]`

**No one walks past during the take.** Background figures are stationary and far off — seated outside
a cafe, standing at a corner, waiting at a bus stop. Nobody crosses the frame, nobody walks behind the
subject, nobody enters or exits shot. Moving background people are the single most common source of
warped faces and duplicated bodies in a 30s generation, and they add nothing.

This should feel like: "`[VIBE CHECK — e.g. 'someone stopped a stranger on a Tuesday lunchtime and
she genuinely stopped to answer']`"

**No readable text anywhere in the background** — no legible shop signs, number plates, posters or
screens. Background text must be present but out of focus and unresolvable.
**Exception: the product packaging, which must be sharp and legible.** See PRODUCT CONTINUITY.
**[ADAPTED — source bans all readable text; the reveal requires the label to read, so the ban is
scoped to background only]**

---

### THE PERSON (subject, on camera)

`[AGE + GENDER + ETHNICITY]`. `[HAIR — length, colour, texture, current state. Include flyaways, frizz, roots,
wind movement.]`

`[SKIN — real texture. Pores, wind flush on the cheeks and nose, under-eye shadow, marks, freckles.
Not ugly — just unfiltered.]`

`[OUTFIT — specific, casual, weather-appropriate, not styled. Fabric types, visible jewellery, a bag
strap across the body. Describe what's visible in a chest-up to waist-up frame.]`

`[CHARACTER ENERGY — one sentence. e.g. "She was walking somewhere and got stopped, and she's giving
this about ninety seconds before she carries on."]`

---

### THE INTERVIEWER (off camera)

Voice, one hand, and a microphone. `[VOICE — age, gender, tone. Match them to the product and the
subject, and vary it between videos: a gym product can have a blokey male interviewer, a beauty
product a younger woman. Whoever it is, unpolished — a real person, not a presenter. Do not default
to the same interviewer every time.]`

**The microphone is visible for the whole take.** A small handheld interview mic — the short stick
type used by street interviewers, plain black or plain silver, no logo flag, no oversized foam
windscreen, no boom. It enters frame from the `[left/right]` edge at chest height, held in the
interviewer's hand, angled up toward the subject and about 25–30cm from their mouth. It drifts
slightly toward whoever is speaking and settles back. It never touches the subject's face or clothing.

Only the **hand and forearm** holding it are ever in shot. No body, no face, no shoulder, no upper
arm, no second person.

**The product is offered with the interviewer's other hand, entering from the opposite edge.** The mic
hand keeps holding the mic throughout — it does not vanish, swap sides, or put the mic down to pass
the product. Two hands, two edges of frame, two jobs.

---

### ENERGY & DELIVERY (THIS IS WHAT MAKES IT REAL)

`[EMOTIONAL ARC — NARROW. The state changes, but every state is a mild version of itself. Default:
mildly amused and sceptical at the hook → matter-of-fact at the admission → a bit fed up through the
pain story → unconvinced at the reveal → mildly surprised at the reaction → flatly decisive at the
verdict. Never "delighted", "thrilled", "animated" or "can't believe it" — enthusiasm reads as acting.]`

`[HOW THEY TALK — default: like they're answering a stranger who caught them off guard. Trails off,
restarts, uses "like" and "honestly", overlaps slightly with the interviewer.]`

Hands move, but small and close to the body — never above shoulder height, never both arms wide. Not
every sentence needs a gesture. Hands rise, make one point, and drop back to their sides or the bag
strap. From 14s onward the hands are
occupied with the product, which changes the gesture vocabulary: smaller, closer to the body,
gesturing *with* the package.

Weight shifts between feet. The subject is standing on a pavement, not posed — they rock slightly,
step back once, turn their shoulders.

---

### SCRIPT (SECOND-BY-SECOND DELIVERY)

Dialogue starts immediately. No settling in, no greeting beyond the hook.

Format each beat as:

> **(X.X–X.Xs) `[SPEAKER]`** — `[physical action before/during the line]`
>
> "`[Dialogue]`"
>
> `[Micro-expression: blink timing, eyebrow, lip behaviour, nose scrunch, swallow. Where the eyes go.
> Where the hand lands when the gesture finishes.]`

**Rules for every beat:**
- **One** physical action and **one** micro-expression per beat — not per sentence, not per word
- Direct only what carries meaning; let the model handle the rest
- Say where the hand lands when a gesture finishes, so it doesn't freeze mid-air
- One weight shift or turn somewhere in the take, not on every line
- Mark silences explicitly — the pause at the reaction beat is required, not optional
- End on the subject continuing PAST the camera and out of frame — never turning back the way they came. Hard stop, no fade, no wave

`[SCRIPT BEATS HERE — follow beat-structure.md]`

---

### AUDIO

Raw iPhone mic outdoors. Two voices: the subject at conversational distance, the interviewer closer
and slightly louder because they're next to the mic. **[ADAPTED — source is single-voice]**

Street ambience throughout: `[2–3 specific sounds — traffic passing, a bus pulling away, footsteps on
paving, distant chatter, wind brushing the mic]`. Occasional wind buffet on the mic. No music. No
room tone. Voices sound close and slightly compressed — phone mic quality, not a lav.

---

### ANTI-GLITCH & REALISM RULES (MANDATORY)

*Copy verbatim into every prompt. Do not modify or remove any line.*

- Natural blinking only — 6–10 blinks across the full 30 seconds
- No face warping during any expression — head shakes, scrunches, smirks, eyebrow raises
- Five fingers on each hand at all times — especially during gestures and during the product handoff. No extras, no merging, no disappearing fingers mid-movement
- Hands remain anatomically correct during every gesture — wrist rotation, finger separation, palm orientation all physically accurate
- Lips sync naturally with every syllable — no drift, no delay
- Hair shifts with head movement, flyaways move independently, wind moves it
- Earrings/jewellery swing subtly with head movement and gestures, don't clip through hair or skin
- Necklace/chain stays in place on collarbones even when hand touches near it
- Clothing fabric responds naturally to arm and hand movements — sleeves shift, fabric pulls when gesturing
- NO pedestrians walk past, cross frame, or move through the shot at any point. Background figures are stationary and distant only — sitting outside a cafe, standing at a corner, waiting at a stop. Every moving person is a chance for the model to warp a face or duplicate a body
- Vehicles in the background move consistently and do not deform
- The subject's face and clothing remain identical from first frame to last
- No beauty smoothing, no glow, no HDR sheen
- No captions, no music, no jump cuts

---

### PRODUCT CONTINUITY (MANDATORY)

*Copy verbatim.*

**[Product = the uploaded reference image.]**

**Do not describe the packaging in the prompt.** No colour, no logo, no material, and above all no
front-of-pack wording — a text description competes with the reference image and garbles the label.
Refer to the product only by a neutral physical noun: "the pouch", "the tin", "the bottle".

The rules below govern how the product behaves over time rather than how it looks in any one frame:

- The package is continuously visible during the handoff — it does not disappear between hands, pass through fingers, or pop between positions
- Both hands are fully rendered throughout the handoff, five fingers each
- The package does not warp, bend, ripple, or change proportions when handled
- The package stays the same size relative to the hand throughout
- The package is held steady and in sharp focus at the reveal, long enough to read
- The package remains identical from the frame it enters to the last frame — no drift in appearance
- The product itself is consistent in colour, size, and count wherever it is visible
- The handback at the close is a second handoff with the same rules — the package stays continuously visible, both hands fully rendered, no teleporting between hands
- No duplicate packages appear in frame at any time

### MICROPHONE CONTINUITY (MANDATORY)

*Copy verbatim. The mic is on screen for the whole take, so it is a continuity risk for the whole take.*

- The microphone is a small plain handheld interview mic — no logo flag, no large foam windscreen, no boom pole, no stand
- It stays the same shape, size, colour and length in every frame
- It stays in the same hand, entering from the same edge of frame, for the entire take
- The hand holding it is fully rendered with five fingers and a natural grip — no merging with the mic body, no fingers passing through it
- The mic never touches the subject's face, hair, or clothing
- It moves only slightly, tracking whoever is speaking — no swinging, no jabbing at the subject
- Only the hand and forearm are visible. No body, no shoulder, no second arm attached to the mic hand
- When the product is offered, it comes from the OPPOSITE edge of frame in the other hand. The mic stays put
- No cable, no visible receiver pack, no second microphone

### ABSOLUTE NOs

*Copy verbatim. Do not modify or remove any line.*

- No cinematic lighting
- No smooth gimbal movement
- No influencer pacing or cadence
- No acting toward camera
- No beauty filter
- No aesthetic grading, no colour grade, no desaturation, no black and white
- No static posture — the subject must be physically active throughout
- No phone, camera, selfie stick, or recording device visible as a prop (the interview microphone IS visible — see MICROPHONE CONTINUITY)
- No boom pole, mic stand, logo flag on the mic, or oversized windscreen
- No readable text on signs, screens, number plates or posters in the background
- No shallow depth-of-field bokeh blur on the subject
- No cuts, no zooms, no speed changes, no slow motion
- No captions or on-screen text of any kind
- No music or score
- No interviewer's face, body, or shoulder in frame at any point
- No crowd reacting, no bystanders looking at camera
- No pedestrians walking past, crossing frame, or entering/exiting shot at any point
- No turning around and walking back the way they came — the subject continues past the camera and exits frame

---

### FINAL TEST

If it feels like an ad → FAIL
If it feels like polished UGC → FAIL
If it feels like someone reading a script → FAIL
If the subject sounds like they already know the brand → FAIL
If the packaging changes or warps in any frame → FAIL

If it feels like `[PASS CONDITION — e.g. "a woman genuinely stopped on a high street who did not
expect the gummies to taste good and is a bit annoyed about it"]` → PASS

---

# Part 4 — Worked Example

The quality bar. Every rule in this document is satisfied here — use it as the shape to copy.

**Brief:** SaltStick Energy Gummies · fast acting energy and electrolytes · fast energy on the go ·
male, white, thirties · Amazon, no discount

**Flip axis:** `no energy available when you're out` → `fast energy you keep in your pocket`

---

### Dialogue script (91 words, 3.19 w/s)

| Time | Speaker | Line | Words |
|---|---|---|---|
| 0.0–3.5 | INTERVIEWER | "Quick question — be honest: do you crash in the afternoon?" | 10 |
| 3.5–11.0 | SUBJECT | "Yeah. Every day, right around three. And I never have anything on me — I end up walking to the shop for a coffee." | 23 |
| 11.0–17.5 | INTERVIEWER | "Have you tried SaltStick Energy Gummies? It's fast energy and electrolytes you keep in your pocket. You can try one right now." | 22 |
| 17.5–24.0 | SUBJECT | *(chews, ~1.5s pause)* "Oh wow, these taste great. If they keep me going through the afternoon, definitely picking up more." | 17 |
| 24.0–27.5 | INTERVIEWER | "You can find them on Amazon — just search for SaltStick Energy Gummies." | 12 |
| 27.5–30.0 | SUBJECT | "Amazing. Going to order a few tonight." | 7 |

Note the shape: the pain beat is one rambling 23-word answer, the sell is the longest interviewer line
at 22, and the reaction carries reaction + condition + purchase intent in a single breath. Five beats.
No keep-it joke, no "where do I get it" question — his interest is the cue for the CTA.

---

### The assembled prompt

```
SEEDANCE 2.5 — STREET INTERVIEW, 9:16 VERTICAL, 30 SECONDS, ONE CONTINUOUS TAKE, NO CUTS

CAPTURE: iPhone 15 Pro rear camera, handheld by a person standing ~1.5m from the subject. Chest
height, angled very slightly up, a degree or two off level. Constant handheld micro-shake from
breathing and weight shifts. Natural drift and re-centring. No stabilisation, no zooms, no reframing,
no cuts. The camera is the operator's point of view and never exists as a visible object in the scene.

LOCATION: A wide city high street, mid-week late morning. Overcast, flat diffused daylight from directly
above, no visible sun, no hard shadows. Soft downward shadow under the brow and jaw, one side of his
face marginally brighter from skylight bouncing off the building on that side. Damp paving, yellow
road markings, scaffolding on a building further down, a courier van parked with hazards on.

NOBODY WALKS PAST DURING THE TAKE. Background figures are stationary and distant only — two people
seated outside a cafe, one person standing at the corner. Nobody crosses frame, nobody walks behind
the subject, nobody enters or exits shot. Traffic moves on the far side of the road only.

No readable text anywhere in the background — signs, posters and number plates are present but out of
focus and unresolvable. Slight iPhone sensor grain in the shadow areas of his face and in the darker
parts of the street. No glow, no warmth filter, no beauty lighting. Visible skin texture throughout.

FRAMING ARC (one take, operator movement only):
0–3.5s wide, subject walking toward camera down the pavement, full body, slows and stops when addressed.
3.5–11s settles to medium, chest-up to waist-up, subject slightly left of centre.
11–17.5s operator's free hand enters frame from the left holding the packet; slight lean in.
17.5–27.5s medium, packet in his hands and visible throughout.
27.5–30s he carries on past the camera in the direction he was already walking, passing close to the
lens and exiting frame right. Frame holds on the empty street. Hard stop.

SUBJECT: White man, mid-thirties. Short dark hair, damp at the temples, a few days of stubble. Real
skin texture — visible pores across the nose and cheeks, flush across the cheekbones, faint under-eye
shadow. Not ugly, just unfiltered. A grey marl hoodie half-unzipped over a navy training top, black
joggers, running trainers, a black holdall over one shoulder. His eyeline is on the interviewer
standing just beside the lens, not into the lens itself.

INTERVIEWER: Off camera — voice, one hand, and a microphone. Woman, late twenties, warm, quick,
friendly, unpolished. A small plain black handheld interview mic is visible in frame for the whole
take, entering from the right at chest height, angled up toward him about 25–30cm from his mouth,
drifting slightly toward whoever is speaking. Only her hand and forearm are ever in shot. The packet
is offered with her OTHER hand from the left at 11s — the mic hand keeps holding the mic and never
puts it down. No body, no face, no shoulder.

ENERGY: His state changes but the range is narrow — mildly amused at the question, matter-of-fact
admitting it, a bit fed up describing the crash, unconvinced at the reveal, genuinely surprised when
he eats one, warm at the close. Never delighted, never animated. He talks like someone answering a
stranger who caught him off guard. Hands move small and close to the body, never above shoulder
height. Not every sentence gets a gesture.

SCRIPT:

(0.0–3.5s) INTERVIEWER, off camera. He is walking toward the camera, looking past it, then registers
being spoken to and slows.
"Quick question — be honest: do you crash in the afternoon?"
He stops, eyebrows lift slightly, a short breath out through the nose.

(3.5–11.0s) SUBJECT. One hand comes off the holdall strap and turns palm-up as he talks, then drops
back to his side.
"Yeah. Every day, right around three. And I never have anything on me — I end up walking to the shop
for a coffee."
Mouth pulls to one side — resigned. He shifts his weight to the other foot. Two blinks.

(11.0–17.5s) INTERVIEWER, off camera. Her free hand enters frame from the left holding the packet,
front toward camera, held steady and in sharp focus, filling about a third of the frame. The mic stays
where it is on the right.
"Have you tried SaltStick Energy Gummies? It's fast energy and electrolytes you keep in your pocket.
You can try one right now."
His eyes drop to the packet. Eyebrows pull together — sceptical. He takes it, pinches the top open and
takes one out between finger and thumb.

(17.5–24.0s) SUBJECT. He puts it in his mouth and chews. Silence — no dialogue for roughly one and a
half seconds. His eyes go off to the side, unfocused.
"Oh wow, these taste great. If they keep me going through the afternoon, definitely picking up more."
Eyebrows lift, he looks back at the interviewer. He holds the packet against his chest.

(24.0–27.5s) INTERVIEWER, off camera. Answering his interest, not pitching.
"You can find them on Amazon — just search for SaltStick Energy Gummies."

(27.5–30.0s) SUBJECT. He holds the packet out and hands it back to the interviewer's hand as he starts
to turn. Warmer here than anywhere else in the take — he has decided.
"Amazing. Going to order a few tonight."
Empty-handed now, he carries on walking the way he was already headed — past the camera, close to the
lens, and out of frame right. He does not turn back the way he came. The frame holds on the empty street. Hard stop.
No fade, no wave, no look back.

AUDIO: Raw iPhone mic outdoors. Two voices — his at conversational distance, the interviewer's closer
and slightly louder because she's next to the mic. Street ambience: traffic on the far side of the
road, distant chatter, occasional wind buffet on the mic. Voices close and slightly compressed, phone
mic quality, not a lav. No music. No room tone.

ANTI-GLITCH & REALISM RULES (MANDATORY):
- Natural blinking only — 6–10 blinks across the full 30 seconds
- No face warping during any expression — head shakes, scrunches, smirks, eyebrow raises
- Five fingers on each hand at all times — especially during gestures and during the product handoff. No extras, no merging, no disappearing fingers mid-movement
- Hands remain anatomically correct during every gesture — wrist rotation, finger separation, palm orientation all physically accurate
- Lips sync naturally with every syllable — no drift, no delay
- Hair shifts with head movement, flyaways move independently, wind moves it
- Earrings/jewellery swing subtly with head movement and gestures, don't clip through hair or skin
- Necklace/chain stays in place on collarbones even when hand touches near it
- Clothing fabric responds naturally to arm and hand movements — sleeves shift, fabric pulls when gesturing
- NO pedestrians walk past, cross frame, or move through the shot at any point. Background figures are stationary and distant only — sitting outside a cafe, standing at a corner, waiting at a stop. Every moving person is a chance for the model to warp a face or duplicate a body
- Vehicles in the background move consistently and do not deform
- The subject's face and clothing remain identical from first frame to last
- No beauty smoothing, no glow, no HDR sheen
- No captions, no music, no jump cuts

PRODUCT CONTINUITY (MANDATORY):
[Product = the uploaded reference image.]
**Do not describe the packaging in the prompt.** No colour, no logo, no material, and above all no
The rules below govern how the product behaves over time rather than how it looks in any one frame:
- The package is continuously visible during the handoff — it does not disappear between hands, pass through fingers, or pop between positions
- Both hands are fully rendered throughout the handoff, five fingers each
- The package does not warp, bend, ripple, or change proportions when handled
- The package stays the same size relative to the hand throughout
- The package is held steady and in sharp focus at the reveal, long enough to read
- The package remains identical from the frame it enters to the last frame — no drift in appearance
- The product itself is consistent in colour, size, and count wherever it is visible
- The handback at the close is a second handoff with the same rules — the package stays continuously visible, both hands fully rendered, no teleporting between hands
- No duplicate packages appear in frame at any time

MICROPHONE CONTINUITY (MANDATORY):
- The microphone is a small plain handheld interview mic — no logo flag, no large foam windscreen, no boom pole, no stand
- It stays the same shape, size, colour and length in every frame
- It stays in the same hand, entering from the same edge of frame, for the entire take
- The hand holding it is fully rendered with five fingers and a natural grip — no merging with the mic body, no fingers passing through it
- The mic never touches the subject's face, hair, or clothing
- It moves only slightly, tracking whoever is speaking — no swinging, no jabbing at the subject
- Only the hand and forearm are visible. No body, no shoulder, no second arm attached to the mic hand
- When the product is offered, it comes from the OPPOSITE edge of frame in the other hand. The mic stays put
- No cable, no visible receiver pack, no second microphone

ABSOLUTE NOs:
- No cinematic lighting
- No smooth gimbal movement
- No influencer pacing or cadence
- No acting toward camera
- No beauty filter
- No aesthetic grading, no colour grade, no desaturation, no black and white
- No static posture — the subject must be physically active throughout
- No phone, camera, selfie stick, or recording device visible as a prop (the interview microphone IS visible — see MICROPHONE CONTINUITY)
- No boom pole, mic stand, logo flag on the mic, or oversized windscreen
- No readable text on signs, screens, number plates or posters in the background
- No shallow depth-of-field bokeh blur on the subject
- No cuts, no zooms, no speed changes, no slow motion
- No captions or on-screen text of any kind
- No music or score
- No interviewer's face, body, or shoulder in frame at any point
- No crowd reacting, no bystanders looking at camera
- No pedestrians walking past, crossing frame, or entering/exiting shot at any point
- No turning around and walking back the way they came — the subject continues past the camera and exits frame

FINAL TEST:
If it feels like an ad → FAIL
If it feels like polished UGC → FAIL
If it feels like someone reading a script → FAIL
If he sounds like he already knows the brand → FAIL
If the packaging changes or warps in any frame → FAIL
If anyone walks past in the background → FAIL
If he turns around and walks back the way he came → FAIL
If he walks off still holding the packet → FAIL
If it feels like a bloke stopped on his way somewhere who did not expect the gummies to be any good
→ PASS
```
