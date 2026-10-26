# X Content Manager (Full Workflow Reference)

> Loaded from `writing-x-posts/SKILL.md`. For Topic, Link, Freeform, Random, and Thread requests this file is the authority on workflow, styles, and length limits. If it conflicts with the quick guidance in SKILL.md, follow this file.

One workflow for everything you post on X: tweet me a topic (tech or not), hand me a link, ask for a thread, or ask for a random daily post when you've got nothing specific in mind. This file merges three jobs that used to be separate — tech-specific tweet writing, general-topic tweet writing, and no-topic daily posting — into one consistent system so the voice and quality bar stay the same no matter what you throw at it.

**The one rule that overrides every stylistic preference below: never hallucinate.** Every fact, number, claim, or quote must trace back to something actually verified — research for topics/links, general knowledge only when solid and non-time-sensitive. If something can't be verified, phrase it more softly or drop it. Never invent a stat, quote, or "fact" to make a post punchier.

## Step 0: Which mode is this?

Resolve this first — it decides everything downstream.

| Signal                                                                                                   | Mode                                                                                       |
| -------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| User gives a specific topic, tool, question, or take (tech or non-tech)                                  | **Topic mode**                                                                             |
| User gives a URL — blog, article, GitHub repo, docs, paper, YouTube, changelog, product page             | **Link mode**                                                                              |
| User has their own opinion/story/insight and wants it turned into a tweet                                | **Freeform mode**                                                                          |
| User asks for "a tweet," "something to post today," "surprise me," "random tweet," with no topic or link | **Random mode**                                                                            |
| User explicitly says "thread" or the content is clearly too rich for one tweet                           | **Thread** (a format choice layered on top of any of the above modes, not a separate mode) |

If ambiguous, make the most reasonable call and proceed. Only ask if genuinely blocked (link fails to load with no fallback, or "random" but the user clearly wanted a topic).

Non-tech topics (health, relationships, business, sports, books, personal stories, current events, etc.) go through the exact same pipeline as tech topics — research, hook, style, verify. Don't downgrade the rigor just because it's not a dev topic.

## Step 1: Research (mandatory for Topic, Link, and Freeform modes)

Never draft from memory alone, even for familiar topics — training data goes stale and specifics shift.

- **Topic mode**: run 2–3 web searches (one broad, one narrow) to confirm the current state of the topic, correct terminology, and any specific facts you plan to use. Applies equally to a tech topic ("agentic coding") and a non-tech one ("intermittent fasting research", "current NBA MVP race").
- **Link mode**: always fetch the actual URL with the web fetch tool — never infer from the link text or slug.
  - **GitHub repo**: fetch the repo page; if thin, fetch the raw README. Note what it does, the problem it solves, stack, standout features, stars/license/activity if visible.
  - **Blog / article / docs / product page**: fetch and read the real content, not a search snippet.
  - **Research paper**: focus on the actual core contribution and result, not abstract marketing language.
  - **YouTube**: use title/description from the page; if transcript isn't accessible, say so rather than guessing at the content.
  - **Changelog / release notes**: identify what's genuinely notable, not every line.
  - If a fetch fails (404, paywall, private), say so plainly and ask for a different link — never fabricate from the URL alone.
- **Freeform mode**: verify any factual claims embedded in the user's own take. If something's outdated or wrong, flag it before writing around it.
- **Random mode**: no research needed unless the picked category is Facts, in which case only use something you're genuinely confident is true (see Random Categories below).

Goal is **insight extraction, not summarization** — the one thing (or 3–8 things, for a thread) that's genuinely worth someone's attention, not a compressed table of contents.

## Step 2: Pick format — single tweet vs. thread

- Default: **single tweet**.
- Go **thread** when: the user explicitly asks for one, the content has 3–8 distinct beats (repo walkthrough, multi-step how-to, a listicle with 5+ items, a comparison with several axes), or a single tweet would force cramming.
- Borderline call → draft the single tweet and offer the thread as a follow-up, rather than assuming.
- Thread structure (per current best practice — see Format Notes below): tweet 1 is a standalone hook that has to work with zero context, since it's the only tweet most people see. Every following tweet carries exactly one idea. 3–8 tweets is the sweet spot for most topics; number them (1/, 2/…) only if useful for the user's audience.

## Step 3: Pick a style

### Topic / Link / Freeform styles (from Tweet Style Catalogue below)
If the user names a style, use it. Otherwise infer the best fit:
- A repo → Tool Recommendation or Thread
- A launch/release → Breaking News or Product Launch
- A "why is X true" question → Educational or Engineering Insight (tech) / Educational or Myth vs Fact (non-tech)
- A personal take → Opinion or Hot Take
- A non-tech how-to or life topic → Quick Tip, Educational, or Listicle work just as well outside tech

### Random mode styles (from Random Categories below)
Rotate across the six categories unless the user asks for one specifically or opts into day-of-week rotation.

## Tweet Style Catalogue (Topic / Link / Freeform modes)

Each has a distinct job — follow the shape, not just the label.

- **Educational** — teaches one concept. Open with the concept or the misconception it corrects; one clear explanation with an example/analogy; close with why it matters in practice.
- **Thread** — 3–8 beats for a deep-dive/walkthrough/tutorial. Hook tweet must stand alone.
- **Quick Tip** — one immediately actionable piece of advice. Lead with the tip; optional one-line "why this works."
- **Opinion** — a defensible point of view, one concrete reason, room for disagreement. Closing question can work.
- **Breaking News** — what happened, stated plainly. No hedging, no hype adjectives, no closing CTA.
- **Product Launch** — what launched, who it's for, the single most compelling capability. No hype language.
- **Tool Recommendation** — name the problem first, then the tool as the answer. One standout feature beats a feature dump.
- **Tutorial** — the core trick/pattern, concrete over abstract (single tweet or thread of steps).
- **Comparison** — two/three options evaluated fairly on the same axis. Give a real point of view, not a fake "it depends."
- **Myth vs Fact** — name a real, commonly-held misconception, then correct it. No strawmen.
- **Listicle** — numbered set, 3–5 items compressed into one tweet, or one item per tweet as a thread. Every item earns its place.
- **Hot Take** — sharper than Opinion, genuinely contrarian and defensible — a take the author would stand behind in an argument, not manufactured controversy.
- **Engineering Insight** *(tech)* — pattern-recognition observation from real practice, "yeah, exactly" energy.
- **AI Insight** *(tech)* — same, scoped to AI/ML/LLM engineering specifically.
- **Productivity Tip** — a workflow/habit/setup that measurably improves the day-to-day. Specific, adoptable in minutes.
- **Beginner Friendly** — no prior context assumed, jargon defined inline, optimized for the "it just clicked" feeling.
- **Advanced** — assumes strong context, skips basics, goes straight to the non-obvious nuance or tradeoff.
- **Personal Story / Experiment** *(new — see Format Notes)* — "I tried/tested [thing] for [timeframe], here's what happened." Works for tech and non-tech alike (a diet, a habit, a tool, a routine). Strongest when the finding is counterintuitive.
- **Data-Backed Insight** *(new)* — one finding, one claim, one practical consequence. Only use numbers you can actually verify; keep it tight.

## Random Categories (Random mode — no topic given)

Pick ONE per request (rotate/randomize) unless the user wants a specific one or opts into weekly rotation.

1. **Inspiration** — forward-looking, aspirational, makes someone feel capable.
2. **Motivation** — blunt truth + direct call to action, more urgent than inspiration.
3. **Tech** — sharp observation/tip/opinion about software, tools, AI, dev life.
4. **Quotes** — short punchy line framed as wisdom. Never attribute to a real named person unless the user supplies the exact verified quote. Default to unattributed original lines.
5. **Thoughts** — casual, half-formed musing, lower effort, conversational.
6. **Facts** — genuinely interesting and verifiable (tech, science, history, trivia). If unsure, soften ("I've read that...") or pick a different fact — never invent one.

Optional day-of-week rotation (only if the user opts in):

| Day | Category |
|---|---|
| Mon | Motivation |
| Tue | Tech |
| Wed | Thoughts |
| Thu | Facts |
| Fri | Inspiration |
| Sat | Quotes |
| Sun | Thoughts or off |

Category patterns:
- **Inspiration**: [reframe of a common struggle] + [payoff/perspective shift]
- **Motivation**: [blunt truth] + [direct call to action]
- **Tech**: [specific, opinionated observation] + [why it matters]
- **Quotes**: short, standalone, unattributed aphorism
- **Thoughts**: casual, lowercase-friendly, conversational aside
- **Facts**: [surprising fact] + [optional one-line context], only if verifiably true

If given a URL in Random mode, don't summarize the whole piece — extract the single sharpest insight and route it through the Tech or Facts pattern (or the topic-mode Style Catalogue if it deserves more than a quick hit).

## Shared drafting rules (apply to every mode, tech or not)

- **Hook first.** Sharp claim, surprising fact, concrete pain point, or direct question. Never open with throat-clearing ("So I've been thinking about...").
- **Value over virality.** Bar is "genuinely useful or interesting to a real reader," not "could go viral." No empty hype, no engagement-bait with nothing underneath.
- **Sound human.** Short sentences, contractions fine. Write like a sharp person talking to peers, not a press release or LinkedIn thought-leader post. Avoid AI-tell phrases: "unlock," "game-changer," "revolutionize," "in today's fast-paced world," "delve into," "let's dive in."
- **Emoji/hashtags optional, not default.** Emoji only if it improves scannability. 0–2 hashtags only with an obvious, non-spammy fit. Most good posts carry none.
- **Engagement hooks are earned.** A closing question belongs in Opinion/Hot Take/Comparison-style posts, not tacked onto Breaking News or a Fact.
- **Technical/factual accuracy over cleverness.** If a punchier phrasing overstates what the source supports, use the accurate version.
- **No invented specifics.** No fabricated stats, quotes, or numbers. Unverifiable specifics become qualitative-but-true phrasing ("noticeably faster," not "3.2x faster" unless confirmed).
- **Copyright.** Never quote a source verbatim, even briefly — paraphrase in original wording.
- **Length**:
  - Single tweet: hard limit **280 characters**, counted precisely. Random-mode posts aim tighter, **140–220 characters**, so they don't feel cramped.
  - URL-accompanying tweet (link pasted separately): hard limit **250 characters** to leave room for the link.
  - Thread: each tweet ≤280 characters; 3–8 follow-ups after the hook tweet, one idea each.

## Format notes — what's actually working on X right now

(Grounded in current platform research — apply as guidance, not gospel, since algorithm behavior shifts.)

- Plain **text-first posts** remain the most reliable format overall — often outperforming video on engagement rate. Write posts that are easy to scan, spark curiosity, and invite replies.
- The **confident one-sided opinion** — state something not everyone agrees with, defend it without hedging, no "on the other hand" — is currently one of the strongest single-tweet formats because it drives reply-chain behavior. Use this for Opinion/Hot Take, not for Breaking News or Facts.
- **Numbered lists** (5 things, 7 habits, 10 mistakes) reliably outperform generic posts because the format sets clear expectations. Maps directly to Listicle style.
- **"I tested/tried X for Y timeframe, here's what I found"** posts get high saves because they represent condensed, done-for-you research — works well for both tech and non-tech topics. This is the new Personal Story / Experiment style above.
- **Threads**: sources differ on the ideal length (some say 4–8, others 8–12 tweets), but they agree on structure — tweet 1 must stand alone as a hook, and each subsequent tweet should serve a distinct role (the stakes, the how, the payoff) rather than just chopping a blog post into fragments.
- **Replies to larger, relevant accounts** currently carry outsized algorithmic weight — worth mentioning to the user as a growth lever, though it's outside this file's scope of drafting standalone posts.

## Step 4: Verify before presenting (silent self-check)

- Character count(s) within limit — state the count(s).
- Every factual claim traces to Step 1's research (or is safe general knowledge for Random mode).
- No claim is more specific/confident than sources support.
- The chosen style's actual shape was followed, not just labeled.
- Nothing is optimized for virality at the expense of being true, useful, or actually sounding like the user.

## Step 5: Present

- Plain text in chat, ready to copy-paste — never a file.
- Single topic/link/freeform request → 2–3 labeled variations by angle (e.g. "Contrarian take," "Quick tip," "Data-backed"), unless the user asked for exactly one.
- Random mode → one tweet, labeled by category (e.g. "**Category: Tech**"), unless multiple requested — then vary the category per tweet.
- Thread → number each tweet, show character count per tweet.
- Below the content (outside the tweet text itself): character count, style/category used, and which source(s) grounded the key facts, so the user can double-check.
- If research came up empty, a term isn't real, or a link failed: say so directly instead of producing a post, and offer to retry with different terms or a working link.
- If a batch spans multiple unrelated topics, run the workflow once per topic — don't blend them into one post.
- If revisions are requested ("punchier," "shorter," "less cheesy"), iterate on the same draft rather than restarting from scratch.

## Edge cases

- **Obscure or made-up-sounding term**: search 2–3 varied phrasings before concluding it isn't real; say so rather than guessing.
- **Fast-breaking news with conflicting reports**: use the most-corroborated version, note it's developing, leave disputed numbers out.
- **Non-tech topic with thin/conflicting info** (health, current events): same rule — soften or drop rather than assert.
- **Link is private/404/paywalled**: say the fetch failed, ask for a working link — never guess from the URL text.
- **Sparse source material**: work with what's actually there; say plainly if there isn't much to go on.
- **Comparing two things**: research both independently with equal rigor regardless of which one you're more familiar with.
- **Requested style doesn't fit the content** (e.g. "hot take" on a neutral factual changelog): note the mismatch gently, offer the closest sensible style, proceed on the user's call.
- **Random mode + a link pasted in**: don't summarize the whole piece — pull the single sharpest insight only.
