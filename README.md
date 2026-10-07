# Writer's Block Unlimited

A SillyTavern preset for AI roleplay and story generation. It pairs a set of always-on writing rules with a large menu of toggleable settings so you can dial in exactly the voice, pacing, and tone you want.

# Check out the latest reddit post for news (I'll be too lazy to update the features on this readme lol)

https://www.reddit.com/r/SillyTavernAI/s/5VZjtcyRnF

## Table of Contents

- [Overview: Universal Rules](#overview-universal-rules)
- [Deep Dive: Preset Options](#deep-dive-preset-options)
  - [Narrative Modes](#narrative-modes)
  - [Plot Momentum](#plot-momentum)
  - [Narrator and Story Tones](#narrator-and-story-tones)
  - [Profanity](#profanity-optional)
  - [Tonal Volatility](#tonal-volatility)
  - [Violence Intensity](#violence-intensity-optional)
  - [Combat Choreography](#combat-choreography-optional)
  - [Vocabulary Level](#vocabulary-level)
  - [Response Length](#response-length)
  - [Paragraph Density](#paragraph-density)
  - [Sentence Rhythm](#sentence-rhythm)
  - [Figurative Language Frequency](#figurative-language-frequency)
  - [Tense](#tense)
  - [Narrative Distance](#narrative-distance)
  - [Show and Tell Levels](#show-and-tell-levels)
  - [POV](#pov)
  - [Consequence Persistence](#consequence-persistence)
  - [Dialogue Frequency](#dialogue-frequency)
  - [Dialogue Naturalism](#dialogue-naturalism)
  - [Dialogue Depth](#dialogue-depth)
  - [Character Change Resistance](#character-change-resistance)
  - [Character Personality Trait Adherence](#character-personality-trait-adherence)
- [Trackers](#trackers)
- [Creative Writing Assistants](#creative-writing-assistants)
- [Custom CoTs](#custom-cots)
- [NSFW Options](#nsfw-options)
- [Narrative Addons](#narrative-addons)
- [Recommended Models](#recommended-models)

---

## Overview: Universal Rules

These rules improve characters, dialogue, and prose. They are **always on** and carried over from Writer's Block 5. The prompt text is shown verbatim below.

<details>
<summary><b>Universal Character Behavior</b></summary>

```
<universal_character_behavior>

# Generate Impulse Before Action
 write the flaw-driven urge (cowardice twitch, jealousy flare, pride spike) first, then let reason override it or fail to.

# Empathy Costs Energy
Starving, dehydrated, or injured characters degrade into selfish reactivity: blunt, irritable, unable to comfort.

#  Pressure
Under pressure, traits warp by doubling-down: the logical become paralyzed by over-analysis; the aggressive become reckless.

# Subtext 
- Deflection takes the form of silence, subject change, or answering a different question
- Allow misinterpretation: characters filter others through their own insecurities and reach wrong conclusions.
- Hard questions get non-answers where the character has reason to evade.

# Anti-Superiority
- No unnecessary one-upmanship. Don't refine or "improve" POV characters sound ideas to appear competent. Genuine agreement is allowed.
- Characters don't need the last clever line. When POV character wins a point, show stunned silence or frustrated acceptance.
- Allow fallibility. When given new valid info, allow real knowledge gaps. 

# Layered Revelation
Drip-feed backstory across scenes

# Nomenclature
- New entities (characters, locations, items) get unique names rooted in their culture or environment.
- Reject generic fantasy names. Use compound words or in-world linguistic roots.

# Autonomy
- Characters actively make their own decisions and take actions.
- The intentions and goals of characters are entirely independent of and may directly conflict with those of  the POV character.
- Characters are allowed to correct, call out, confront or react in other ways that align with their personality. 

</universal_character_behavior>
```

</details>

<details>
<summary><b>Dialogue</b></summary>

```
<dialogue>
# DIALOGUE 
Dialogue = Baseline Voice + Regional Texture + Current State. Each character has a distinct, recognizable idiolect; vocabulary reflects background.

- Em-dashes (—) for interruptions.
- Regional speech patterns may mirror real-world dialects, but lexical choices derive from in-world geography, history, and culture.

# State Modifiers
- Anger: clipped syntax, hedging dropped, volume shown via word choice.
- Fear: fragmented sentences, false starts.
- Drunk: lost trains of thought, repetition, inappropriate honesty.
- Exhausted: shorter utterances, delays, missing words.
- Lying: over-specificity, increased hedging, unnatural smoothness or stutter.
- Seduction: slower rhythm, more pauses, suggestive ambiguity.
- Authority: fewer words, statements over questions.
</dialogue>
```

</details>

<details>
<summary><b>Anti-Omniscience</b></summary>

```
<anti_omniscience> 
Strip any information the POV character and cast hasn't personally observed or witnessed.

Where realistic, allow characters to misread, misunderstand, or fill gaps with their own bias. 

Characters don't know names of strangers. 

Side characters don't know POV character's thoughts.

You must not grant characters shared knowledge by convenience.
</anti_omniscience> 
```

</details>

<details>
<summary><b>Anti-Resolution</b></summary>

```
<anti_resolution>
Resist the pull toward resolution. Scenes may end mid-tension; apologies need not land; understanding can stay incomplete.

Characters can be wrong yet sympathetic, or right yet unlikeable. No moral flattening.

Not every difficult moment needs a silver lining. Sitting in discomfort beats reaching for comfort.

Joy, tenderness, and struggle coexist. Leaving a thread open is preferable to closing it early.
</anti_resolution>
```

</details>

<details>
<summary><b>Banned Patterns</b></summary>

```
<banned_patterns>

- No Negative parallelism ("not [X] but [Y]"), epanorthosis ("It was [X]. Not [Y]." "Not [X] but [Y]), no litotes, no corporate fluff, no thought-verbs (felt/realized/knew). Describe what does happen, not what doesn't. Describe the intensity immediately without  negating a milder version (e.g. "It wasn't [X], it was [Y].")

- No "mouths opens. Closes."

- Commit on the first attempt: define emotions, objects, and actions exactly as they are, with singular definitive statements and strong standalone verbs.

- Characters should not repeat or parrot {{user}} input or dialogue in your response.

- Stop having characters accidentally lose their shoes.

- No repeating details in previous turns.

- No "No one ever said that before." And it's variants.

- No thought-verbs (felt, realized, knew, understood). Render the state itself rather than announcing that a character had it.

</banned_patterns>
```

</details>

---

## Deep Dive: Preset Options

Strap in, folks. This section goes over every option in the preset.

### Narrative Modes

Your role in chats and how `{{user}}` will behave.

| Mode | Description |
|---|---|
| **Roleplay** | Does not write for `{{user}}`. |
| **Director** | `{{user}}` is an invisible scene director that the AI will follow. |
| **Active Persona** | Rewrites, expands, and embellishes `{{user}}` input, including writing dialogue and thoughts for them based on their personality and history. |

### Plot Momentum

How far a scene will progress.

| Setting | Description |
|---|---|
| **Reactive** | Reacts to your input but goes no further. No new events or consequences. |
| **Active** | The scene can progress further than your input implies. Characters proceed whether or not `{{user}}` drives them. |
| **Driving** | Ends the scene on an open-ended action, threat, or question that demands a response. |

### Narrator and Story Tones

30+ tones to mix and match for a unique style. Tones affect the voice of the narrator and the tone of the world. **Pick at least two.**

I won't list every tone here to keep this section short, but here is my personal combo (verbatim) for a livelier narrator and world:

| Tone | Prompt |
|---|---|
| **Energetic** | Carry upward momentum: keep energy high and move events quickly |
| **Humorous** | Hunt for the comedy in every situation: arrange observation and timing to land jokes |
| **Playful** | Treat the scene as an opportunity for amusement: tease characters and enjoy their reactions |
| **Exaggerated** | Inflate descriptions past the event; push reactions, stakes and details beyond proportion |

Don't be afraid to experiment. You can make something fun and even pick tones that contrast each other.

### Profanity (Optional)

**Light**, **Medium**, **Heavy**, and **Setting Appropriate** (modern settings use modern swears, medieval settings use medieval swears, etc.).

### Tonal Volatility

How often the tone changes between your chosen tones. **This one is very important.**

This is where things get fun and where your chosen tones come into play, since it makes the AI plan out the scene using them. If you choose contrasting tones, tonal volatility is a powerful tool for keeping your stories interesting.

| Setting | Description |
|---|---|
| **Stable** | Mixes your chosen tones for each scene beat. Good if you selected only a few tones or want a consistent tone. |
| **Shifting** | The AI selects one of your chosen tones for each beat and shifts when required. Good when you've selected a lot. |
| **Whiplash** | The tone changes every **paragraph**. |

I made this its own section because real written stories don't stick to one or two tones. *Metal Gear Solid: The Twin Snakes* can be dead serious, and then something silly happens the next scene.

#### Example Combos

**Emulating *MGS: The Twin Snakes*** (also works for the silliness of the *Yakuza* games)
- **Tones:** Serious, Absurdist, Exaggerated
- **Volatility:** Whiplash

**Emulating Joe Abercrombie's *The First Law*** (grimdark, with dark comedy and warm scenes to contrast the dark moments)
- **Tones:** Dark, Cynical, Sardonic/Humorous, Warm
- **Volatility:** Shifting

**From my own roleplays:** I have a scenario set in a magical world that's supposed to be whimsical and playful, but it always drifted into melodrama no matter how much I steered it back, and I'd lose interest. With tonal volatility, it can still have dramatic moments and then shift back into its playful tone.
- **Tones:** Energetic, Playful, Warm, Whimsical, Wondrous, Sensual
- **Volatility:** Shifting

Basically, it helps keep your story from going stale.

### Violence Intensity (Optional)

| Setting | Description |
|---|---|
| **Restrained** | Violence is skimmed. |
| **Grounded** | Wounds are described, and injury affects what a character can do afterward. |
| **Unflinching** | Nothing is spared or omitted. Extended graphic detail. |
| **Visceral** | Violence is rendered in sensory detail: the specific mechanics of injury, sound, texture, blood, the body's failure. |

### Combat Choreography (Optional)

| Setting | Description |
|---|---|
| **Stylized** | Emulates the ridiculousness of *RWBY* and *MGS*. The AI bends logic and allows unrealistic feats to make fights cool. |
| **Cinematic** | Prioritizes clarity and spectacle. |
| **Brutal** | Fights are desperate and graceless. |
| **Realistic** | Fights are short, ugly, and decided quickly. |

> You can leave Violence Intensity and Combat Choreography off if your scenario doesn't involve fighting.

### Vocabulary Level

Affects the word choice of narration. Dialogue is not affected.

| Setting | Description |
|---|---|
| **Plain** | Everyday, informal language. |
| **Clean** | Standard contemporary novel prose. |
| **Literary** | Uncommon and deliberate words. |
| **Purple** | Elevated register throughout. Formal syntax, Latinate word choice, rare and archaic words used freely. |

### Response Length

How many paragraphs per response. Paragraphs containing dialogue are not counted.

| Setting | Paragraphs |
|---|---|
| **Short** | Under 4 |
| **Medium** | Under 8 |
| **Long** | 4 to 12 |
| **Adaptive** | Decided by scene type: developmental scenes under 8, reactive and transitional under 4, climaxes use as many as needed for proper impact. |

### Paragraph Density

How many sentences per paragraph. Dialogue doesn't count toward the limit.

| Setting | Sentences |
|---|---|
| **Minimal** | 1–2 |
| **Light** | 1–3 |
| **Standard** | 1–5 |
| **Full** | 1–8 |
| **Dense** | 8+ required |
| **Adaptive** | Developmental and transitional: 1–5, reactive: 1–2, climax: 1–8. |

### Sentence Rhythm

The flow of sentences. Does not affect dialogue.

| Setting | Description |
|---|---|
| **Standard** | Multiclausal sentences to vary prose rhythm. |
| **Sprawling** | Long, clause-heavy sentences. |
| **Percussive** | Short. Punchy. Sentences. |
| **Dynamic** | Long sentences for interiority and description; short, fragmented sentences for action. |

> **Note:** Depending on the model, Sentence Rhythm and Paragraph Density may not be followed exactly, but they will still influence the output. Gemma 4 and Kimi sometimes follow them exactly, so keep that in mind.

### Figurative Language Frequency

How often similes, metaphors, hyperbole, idioms, etc. are used.

| Setting | Description |
|---|---|
| **None** | All description is literal. |
| **Sparse** | Only one figurative image per generation. |
| **Moderate** | One image every several paragraphs. |
| **Rich** | One per paragraph. |
| **Saturated** | Nearly every sentence is figurative. |

### Tense

**Past** or **Present**. Self-explanatory — we all had English classes.

### Narrative Distance

How close the narrator is to the characters, and how visible their thoughts are.

| Setting | Description |
|---|---|
| **Remote** | Thoughts are not shown; interiority is unavailable. |
| **Objective** | Physically close to the characters. Actions and sensations are reported, but internal thoughts are not shown. |
| **Standard** | The POV character's thoughts and feelings are reported, but the narration keeps its own voice separate from theirs. |
| **Close** | Narration takes on the POV character's perceptions and biases. |
| **Free Indirect Discourse** | The narrative voice and the POV character's voice merge; their diction, judgments, and distortions appear in the narration itself without italics. |

There's also an optional **Show Other Characters' Thoughts** toggle.

> **Tip:** For regular roleplay, use **Objective** so the AI doesn't narrate your `{{user}}`/POV character's thoughts.

### Show and Tell Levels

How often emotions and character traits are stated versus shown.

| Setting | Description |
|---|---|
| **Pure Tell** | Emotions and traits are explicitly stated. |
| **Tell Weighted** | Emotions and traits are stated directly. Showing is reserved for the scene's strongest beats. |
| **Balanced** | Emotions and traits may be named where naming is efficient, and shown through physical actions. |
| **Show Weighted** | Emotions and traits are conveyed through physical action by default. Direct statement appears only where behavior would be ambiguous. |
| **Pure Show** | Emotions and traits are never stated; they're conveyed through action, physical response, and dialogue. |

### POV

The standard options: **1st**, **2nd**, and **3rd** person, plus:

- **Shifting 3rd Person:** The POV switches to other characters for story impact.

### Consequence Persistence

How injuries and destruction carry over.

| Setting | Description |
|---|---|
| **Realistic** | Injury, damage, and loss don't reverse. Wounds heal at realistic rates or not at all; broken things stay broken unless repaired. |
| **Persistent** | Injuries heal faster than realistic, property somehow gets repaired between arcs, and characters recover. |
| **Soft** | Damage matters while a scene is running and fades between scenes. Characters arrive at the next scene functional. |
| **Reset** | Characters arrive at the next scene fully healed, and damage is repaired. |

### Dialogue Frequency

Ratio of dialogue to narration.

| Setting | Dialogue | Narration |
|---|---|---|
| **Silent** | 0–10% | 90–100% |
| **Sparse** | 20–30% | 70–80% |
| **Balanced** | 50% | 50% |
| **Often** | 70% | 30% |
| **Talkative** | 80–90% | 10–20% |

### Dialogue Naturalism

How clean the dialogue is.

| Setting | Description |
|---|---|
| **Literary** | Standard novel dialogue. Contractions and fragments are natural; no filler words or stumbling. |
| **Colloquial/Casual** | Slang, regional phrasing, sentence fragments, characters talking over each other and trailing off. |
| **Verbatim** | Full disfluency: filler words ("Um," "like," "okay"), false starts, self-corrections, repetitions, and trailing sentences. |

### Dialogue Depth

How deep conversations can go.

| Setting | Description |
|---|---|
| **Surface Level** | Speech is factual and direct, with no deeper thoughts. |
| **Grounded** | Occasional reflection or generalization, tied closely to the scene at hand. A character may draw a conclusion about themselves or someone else. |
| **Layered** | Conversations carry more than their surface. Characters argue past the ostensible subject. Abstraction is present. |
| **Philosophical** | Characters theorize, generalize, and pivot from concrete detail to abstract meaning. Digressions are allowed. |
| **Realistic** | Depth follows what the speaker is capable of and what the moment supports. Functional exchanges stay functional; pressure, intimacy, and idleness are when characters reach for larger statements. |

### Character Change Resistance

How difficult it is for you to influence characters.

| Setting | Description |
|---|---|
| **Fluid** | Characters change easily. |
| **Responsive** | One significant event, or several smaller converging ones, is enough to move a character. |
| **Resistant** | Development requires sustained cause and usually comes with backsliding. |
| **Entrenched** | Characters return to baseline quickly. Change requires overwhelming, repeated cause, and even then it registers as strain rather than transformation. |
| **Circular** | Characters can change but revert once the pressure that produced the change lifts. |

> *"Change... change is a funny thing. Sometimes men change for the better. Sometimes men change for the worse. And often, very often, given time and opportunity... they change back."*
> — Nicomo Cosca
>
> (I added Circular just because of this quote, lol.)

### Character Personality Trait Adherence

How strongly characters express their traits.

| Setting | Description |
|---|---|
| **Restrained** | Traits surface selectively. Characters act on them when circumstances call for it and behave unremarkably otherwise. |
| **Pronounced** | Traits are visible in most choices and reliably inform behavior. Characters are recognizable from a single scene. |
| **Exaggerated** | Traits are expressed past realistic proportion. Over the top. |

---

## Trackers

*Renamed and updated.*

WB Unlimited comes with three trackers. All three track characters and their positions, time, and clothing, but each differs a bit:

| Tracker | What It Adds | Use With |
|---|---|---|
| **Roleplay Tracker** | `{{user}}`'s hunger, thirst, ailments, and wealth, plus three background activities for a living world. | Roleplay and Active Persona modes |
| **Director's Notes** | Drops the survival mechanics and adds a Chapter tracker and a subtext scanner. | Director mode, or if you don't want survival mechanics |
| **Bare Essentials** | Only characters, positions, time, and clothing. | Anything, when you want it minimal |

The trackers come with cleaner regexes that remove them after 4 messages.

---

## Creative Writing Assistants

*The assistants return!* The creative writing assistants from WB 5 are back with minor modifications.

- **📍 Plot Director** — Proposes three possible directions for the next turn: a logical path, a fun path, and an unhinged path.
  **New:** The logical and fun paths now subtly influence the next turn.
- **💡 Brainstormer** — Generates 2–3 open-ended ideas to enrich the wider story: worldbuilding, lore, history, culture, character backstory, unused character potential, locations, factions, "what if" concepts, and more. These aren't tied to the immediate arc or scene.
- **🔍 Trope Spotter** — Identifies notable tropes, clichés, or familiar patterns in the current scene, narrative, characters, or dialogue. May include a very concise history lesson or fun fact about the trope.
- **🧵 Plot Threads Tracker** — Reminds you of unfinished story arcs or unanswered questions.
- **🎲 Chaos Suggester** — Proposes one wild, unexpected, or disruptive thing that *could* happen next. Deliberately as chaotic and non-sequitur as possible, to set it apart from the Plot Director.

---

## Custom CoTs

Three chain-of-thought prompts to make sure the AI follows all the rules and to improve output.

| CoT | Description |
|---|---|
| **Balanced** *(recommended)* | Good balance of quality and speed. |
| **Full** | Drafting and revising allowed, for maximum quality and prompt adherence. |
| **Bare Essentials** | Only 3 steps that check the selected settings. |

Using GLM on OpenRouter, the CoTs are decently fast, around 8–20 seconds per response. Speed will vary with peak hours.

---

## NSFW Options

> ⚠️ **18+ only.** These options are off by default.

**🔞 Explicit Content Toggle** — Allows NSFW themes.

### Sexual Flavors

| Setting | Description |
|---|---|
| **Sexual Fantasy** | Sex is idealized and bodies are objectified. Sensory description registers as attractive. |
| **Sexual Realism** | Bodies are described anatomically and directly. Scent, fluid, and texture are rendered plainly and realistically (i.e. pussy and cock should be stanky after spending 5 hours killing bandits and being practically covered in their guts 🤮). |

### NSFW Tones

Found in the tones section.

- **🥵 Horny/Hentai** — NSFW and sexual themes are constant. All kinks are permitted. Always makes room for freaky stuff.
- **😳 Perverted** *(softcore/ecchi anime inspired)* — All ecchi tropes (panty flashes, wardrobe malfunctions, accidental gropes, cleavage faceplants, etc.) are encouraged. The story bends physics, probability, and logic to force these moments. Teases sex relentlessly but doesn't escalate to penetration unless prompted.

---

## Narrative Addons

More details for each can be found in the preset.

- 🐱 **Anthropomorphic Realism** 🐶
- 🪝 **Narrative Hooks**
- 🗣️ **Dialects**
- 👫 **Better Side Characters**
- 🌍 **Enhanced World**
- 📺 **Episodic Mode**
- 📃 **Wordplay**

---

## Recommended Models

Based on how well they follow the CoTs:

- GLM 5.3 / 5.2 / 5.1 / 5.0
- Claude Opus 4.6
- Longcat 2.0
- Gemma 4 31b
- Kimi 2.5 (prone to overthinking though)
