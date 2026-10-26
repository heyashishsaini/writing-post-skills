---
name: x-content-manager
description: "Complete X/Twitter content manager — one standalone skill for everything posted on X. Handles ANY topic (tech or non-tech), any link (blog, article, GitHub repo, docs, paper, YouTube, changelog), the user's own freeform take, random/daily posts, and AI-industry news research. Produces single tweets, threads, hooks, and daily posts across a full style + category catalogue. Use whenever the user says 'tweet about X', 'write a thread on X', 'turn this link into a tweet', 'give me a random tweet', 'daily tweet', 'post idea for today', 'surprise me', 'AI news', 'what's new in AI', 'latest AI updates', asks for X/Twitter content, hooks, viral posts, or X engagement strategy, or pastes a topic/URL with or without instructions. Use it even if the user only says 'make this a tweet' or 'post idea'. It does not hand off elsewhere."
---

# X Content Manager

One workflow for everything you post on X: give a topic (tech or not), hand over a link, ask for a thread, ask for a random daily post, or ask for a roundup of AI news turned into posts. This single file contains the whole system — modes, research rules, styles, hook library, thread frameworks, examples, and the AI-news research workflow — so nothing needs to be loaded separately.

**The one rule that overrides every stylistic preference below: never hallucinate.** Every fact, number, claim, or quote must trace back to something actually verified — research for topics/links, general knowledge only when solid and non-time-sensitive. If something can't be verified, phrase it more softly or drop it. Never invent a stat, quote, or "fact" to make a post punchier.

## Contents

1. [Step 0 — Which mode is this?](#step-0-which-mode-is-this)
2. [Step 1 — Research](#step-1-research-mandatory-for-topic-link-freeform-and-news-modes)
3. [Step 2 — Single tweet vs. thread](#step-2-pick-format--single-tweet-vs-thread)
4. [Step 3 — Pick a style](#step-3-pick-a-style)
5. [Tweet Style Catalogue](#tweet-style-catalogue-topic--link--freeform-modes)
6. [Random Categories](#random-categories-random-mode--no-topic-given)
7. [Core principles & post anatomy](#core-principles--post-anatomy)
8. [Shared drafting rules](#shared-drafting-rules-apply-to-every-mode-tech-or-not)
9. [Hook library](#hook-library)
10. [Thread frameworks & techniques](#thread-frameworks--techniques)
11. [Format notes & engagement mechanics](#format-notes--engagement-mechanics)
12. [Step 4 — Verify](#step-4-verify-before-presenting-silent-self-check)
13. [Step 5 — Present](#step-5-present)
14. [Edge cases](#edge-cases)
15. [Appendix A — Examples](#appendix-a--full-examples)
16. [Appendix B — AI News Research workflow](#appendix-b--ai-news-research-workflow)

---

## Step 0: Which mode is this?

Resolve this first — it decides everything downstream.

| Signal | Mode |
| --- | --- |
| User gives a specific topic, tool, question, or take (tech or non-tech) | **Topic mode** |
| User gives a URL — blog, article, GitHub repo, docs, paper, YouTube, changelog, product page | **Link mode** |
| User has their own opinion/story/insight and wants it turned into a tweet | **Freeform mode** |
| User asks for "a tweet," "something to post today," "surprise me," "random tweet," with no topic or link | **Random mode** |
| User asks for AI news, "what's new in AI," company updates (OpenAI, Anthropic, Google, etc.), or posts based on the latest AI developments | **News mode** (run Appendix B, then write posts from the findings) |
| User explicitly says "thread" or the content is clearly too rich for one tweet | **Thread** (a format choice layered on top of any of the above modes, not a separate mode) |

If ambiguous, make the most reasonable call and proceed. Only ask if genuinely blocked (link fails to load with no fallback, or "random" but the user clearly wanted a topic).

Non-tech topics (health, relationships, business, sports, books, personal stories, current events, etc.) go through the exact same pipeline as tech topics — research, hook, style, verify. Don't downgrade the rigor just because it's not a dev topic.

## Step 1: Research (mandatory for Topic, Link, Freeform, and News modes)

Never draft from memory alone, even for familiar topics — training data goes stale and specifics shift.

- **Topic mode**: run 2–3 searches (one broad, one narrow) to confirm the current state of the topic, correct terminology, and any specific facts you plan to use. Applies equally to a tech topic ("agentic coding") and a non-tech one ("intermittent fasting research", "current NBA MVP race").
- **Link mode**: always fetch the actual URL — never infer from the link text or slug.
  - **GitHub repo**: fetch the repo page; if thin, fetch the raw README. Note what it does, the problem it solves, stack, standout features, stars/license/activity if visible.
  - **Blog / article / docs / product page**: fetch and read the real content, not a search snippet.
  - **Research paper**: focus on the actual core contribution and result, not abstract marketing language.
  - **YouTube**: use title/description from the page; if transcript isn't accessible, say so rather than guessing at the content.
  - **Changelog / release notes**: identify what's genuinely notable, not every line.
  - If a fetch fails (404, paywall, private), say so plainly and ask for a different link — never fabricate from the URL alone.
- **Freeform mode**: verify any factual claims embedded in the user's own take. If something's outdated or wrong, flag it before writing around it.
- **News mode**: follow Appendix B (search, recency filter, dedupe, verify, prioritize), then pick the one or few stories worth posting about.
- **Random mode**: no research needed unless the picked category is Facts, in which case only use something you're genuinely confident is true (see Random Categories below).

Goal is **insight extraction, not summarization** — the one thing (or 3–8 things, for a thread) that's genuinely worth someone's attention, not a compressed table of contents.

## Step 2: Pick format — single tweet vs. thread

- Default: **single tweet**.
- Go **thread** when: the user explicitly asks for one, the content has 3–8 distinct beats (repo walkthrough, multi-step how-to, a listicle with 5+ items, a comparison with several axes), or a single tweet would force cramming.
- Borderline call → draft the single tweet and offer the thread as a follow-up, rather than assuming.
- Thread structure: tweet 1 is a standalone hook that has to work with zero context, since it's the only tweet most people see. Every following tweet carries exactly one idea. **3–8 tweets is the default sweet spot**; go up to ~10 only for genuinely rich storytelling or tutorial content. Number them (1/, 2/…) only if useful for the user's audience.
- Thread frameworks to shape the beats are in [Thread frameworks & techniques](#thread-frameworks--techniques).

## Step 3: Pick a style

### Topic / Link / Freeform / News styles (from the Tweet Style Catalogue below)
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
- **Personal Story / Experiment** — "I tried/tested [thing] for [timeframe], here's what happened." Works for tech and non-tech alike (a diet, a habit, a tool, a routine). Strongest when the finding is counterintuitive. Only write this from facts the user actually provides — never invent the experience.
- **Data-Backed Insight** — one finding, one claim, one practical consequence. Only use numbers you can actually verify; keep it tight.

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
| --- | --- |
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

---

## Core principles & post anatomy

### Brevity is power
X rewards concise, punchy content. Every word must earn its place. If you can say it in fewer words, do it.

### One idea per tweet
Single tweets contain one complete thought. Threads expand on ideas, but each tweet should still stand alone.

### Hook or die
You have about one second to stop the scroll. The first line determines engagement, reach, and whether anyone reads the rest.

### Content formats at a glance

| Format | Length | Purpose | Best for |
| --- | --- | --- | --- |
| Single post | Under 280 characters (under 200 is better) | One sharp insight, observation, or take | Hot takes, quick tips, observations, quotes |
| Thread | 3–8 tweets default (up to ~10 for rich stories; 7 is a common sweet spot) | Deep dives, stories, frameworks, lists | Tutorials, stories, breakdowns, listicles |

### Post anatomy

**The Hook (tweet 1)** has one job: make someone stop scrolling. Hook formula — combine one or more of:
1. **Bold statement** — surprise, shock, or make a claim
2. **Tension** — highlight a struggle or pain point
3. **Twist** — flip expectations
4. **Open loop** — tease what's coming

The full pattern library is in [Hook library](#hook-library).

**The Body (tweets 2–6)**
- Keep each tweet under 250 characters
- Use cliffhangers every 1–2 tweets
- Add visual breaks every 3–4 tweets
- White space and short sentences aid scanning

**The Close (final tweets)**
- **Punchy lesson**: crystallize the main takeaway
- **Soft CTA**: invite engagement naturally
- **Final CTA**: direct ask (follow, repost, reply) — only when earned

### Tone
- Conversational, not formal
- Confident, not arrogant
- Slightly provocative (when appropriate)
- Authentic, not performative

### Formatting
- Short sentences, generous white space, line breaks for emphasis
- 0–2 hashtags max (most posts carry none)
- Emojis sparingly

### What to avoid
- Corporate speak
- Excessive hashtags
- Links in the main tweet (can reduce reach — put them in a reply or follow-up tweet when possible)
- Asking for engagement without providing value
- Walls of text

---

## Shared drafting rules (apply to every mode, tech or not)

- **Hook first.** Sharp claim, surprising fact, concrete pain point, or direct question. Never open with throat-clearing ("So I've been thinking about...").
- **Value over virality.** Bar is "genuinely useful or interesting to a real reader," not "could go viral." No empty hype, no engagement-bait with nothing underneath.
- **Sound human.** Short sentences, contractions fine. Write like a sharp person talking to peers, not a press release or LinkedIn thought-leader post. Avoid AI-tell phrases: "unlock," "game-changer," "revolutionize," "in today's fast-paced world," "delve into," "let's dive in."
- **Emoji/hashtags optional, not default.** Emoji only if it improves scannability. 0–2 hashtags only with an obvious, non-spammy fit.
- **Engagement hooks are earned.** A closing question belongs in Opinion/Hot Take/Comparison-style posts, not tacked onto Breaking News or a Fact.
- **Technical/factual accuracy over cleverness.** If a punchier phrasing overstates what the source supports, use the accurate version.
- **No invented specifics.** No fabricated stats, quotes, or numbers. Unverifiable specifics become qualitative-but-true phrasing ("noticeably faster," not "3.2x faster" unless confirmed).
- **Copyright.** Never quote a source verbatim, even briefly — paraphrase in original wording.
- **Length**:
  - Single tweet: hard limit **280 characters**, counted precisely. Random-mode posts aim tighter, **140–220 characters**, so they don't feel cramped.
  - URL-accompanying tweet (link pasted separately): hard limit **250 characters** to leave room for the link.
  - Thread: each tweet ≤280 characters (aim ≤250); one idea each, hook tweet standalone.

---

## Hook library

The hook is everything on X. These patterns are proven to capture attention. **All example lines below are illustrative templates of shape and rhythm only — never reuse their numbers or claims as real facts. When writing for the user, replace placeholders with facts that are verified or that the user actually supplied.**

### Bold Claim Hooks
Make a statement so bold readers must understand how it's true.
**Pattern**: "[Surprising claim that seems too good/bad to be true]"
- "I went from 0 to 10,000 followers in 57 days without posting a single thread."
- "One cold email changed my entire career."
- "I made more in 30 days than I did in a year at my job."
- "The best marketing strategy costs $0."
- "I built a $100K business with a skill I learned in a weekend."

**Why it works**: The gap between the claim and believability forces readers to seek explanation.

### Transformation Hooks
Show dramatic before/after contrast.
**Pattern**: "[Past state] → [Current state] + [Timeframe or method tease]"
- "6 months ago I was broke. Today I turned down a $200K offer. Here's what changed:"
- "From rejected by 50 companies to 3 competing offers in 8 weeks."
- "I went from anxious mess to calm leader. This framework saved me:"
- "0 followers → 50K in 6 months. No ads. No luck. Just this:"
- "Burned out employee → thriving founder. The pivot that changed everything:"

**Why it works**: Transformation stories are inherently compelling. Readers want the roadmap.

### Contrarian Hooks
Challenge what everyone believes.
**Pattern**: "[Popular belief] is wrong/dead/overrated. Here's why:"
- "Unpopular opinion: Networking events are useless."
- "Stop setting goals. Seriously. Here's what to do instead:"
- "The 'rise and grind' mentality is destroying your career."
- "Your resume doesn't matter anymore. Here's what does:"
- "Most productivity advice is garbage. Here's what actually works:"

**Why it works**: Challenges create cognitive dissonance. Readers need resolution.

### Curiosity Gap Hooks
Tease information without revealing it.
**Pattern**: "[Intriguing setup] + [Incomplete information]"
- "The CEO said 3 words that changed how I think about leadership forever."
- "I asked 100 millionaires one question. The answers shocked me."
- "There's one thing every successful person does that nobody talks about."
- "I made one change to my morning routine. Everything improved."
- "My mentor's advice sounded crazy at first. Then I tried it."

**Why it works**: The brain craves closure. Incomplete information compels clicks.

### List Promise Hooks
Promise specific, valuable information.
**Pattern**: "[Number] [things/tips/lessons/mistakes] + [outcome/topic]"
- "7 lessons from building a $1M business (that I wish I knew at 25):"
- "5 habits that seem lazy but actually make you more productive:"
- "10 things I'd tell my younger self about career growth:"
- "8 books that changed how I think about money:"
- "6 mistakes I made hiring my first 10 employees:"

**Why it works**: Numbers create specificity. Lists promise organized, digestible value.

### Question Hooks
Open with a provocative question.
**Pattern**: "[Question that challenges or resonates deeply]?"
- "Why do smart people make terrible decisions?"
- "What's the one skill nobody talks about but everyone needs?"
- "Are you building a career or just collecting paychecks?"
- "What if everything you know about success is wrong?"
- "Why are the busiest people often the least productive?"

**Why it works**: Questions activate different brain patterns. Readers naturally seek to answer.

### Story Hooks
Start in the middle of action.
**Pattern**: "[Dramatic moment or dialogue that drops reader into a scene]"
- "The investor looked at me and said, 'This will never work.'"
- "I was 30 seconds from quitting when everything changed."
- "My phone rang at 3am. It was the call that changed everything."
- "I stared at my bank account: $47. I had a decision to make."
- "'You're fired.' Two words. One moment. Everything shifted."

**Why it works**: Stories create immediate emotional engagement. Readers need to know what happens.

### Data Hooks
Lead with surprising statistics or results.
**Pattern**: "[Specific number/stat] + [unexpected context]"
- "I analyzed 1,000 viral threads. 90% follow this exact pattern:"
- "After 500 cold emails, I learned one thing that 10x'd my response rate."
- "I tracked my time for 30 days. The results were embarrassing."
- "87% of people make this mistake in negotiations. Here's the fix:"
- "I interviewed 50 founders. They all said the same thing about failure:"

**Why it works**: Specific numbers create credibility. Data implies proven insights. (Only use real, verified numbers when writing for the user.)

### Hook testing framework
Before presenting a hook, verify it:
1. **Scroll-stop**: Would you stop scrolling for this?
2. **Specificity**: Is it concrete or vague?
3. **Promise**: Is the value proposition clear?
4. **Curiosity**: Does it create an information gap?
5. **Believability**: Bold enough to intrigue, believable enough to trust?

**Weak**: "Here's some advice on growing on Twitter."
**Strong**: "I grew from 0 to 25K followers in 90 days. Here's the exact playbook (no fluff):" *(template shape — only use real numbers)*

---

## Thread frameworks & techniques

### Storytelling Framework
Best for: personal experiences, case studies.
```
1/ [Hook - outcome or surprising moment]
2/ [Set the scene - context]
3/ [The challenge/conflict]
4/ [The journey - what happened]
5/ [The turning point]
6/ [The lesson]
7/ [CTA - question or follow prompt]
```

### Listicle Framework
Best for: tips, tools, resources.
```
1/ [Hook - promise of value]
2/ [Item 1 - with brief explanation]
3/ [Item 2]
4/ [Item 3]
5/ [Item 4]
6/ [Item 5]
7/ [Summary + CTA]
```

### Problem-Solution Framework
Best for: educational content, how-tos.
```
1/ [Hook - the problem everyone faces]
2/ [Agitate - why it's painful]
3/ [Solution intro]
4/ [Step 1]
5/ [Step 2]
6/ [Step 3]
7/ [Results + CTA]
```

### Contrarian Framework
Best for: thought leadership, hot takes.
```
1/ [Bold contrarian statement]
2/ [What everyone believes]
3/ [Why they're wrong]
4/ [Your counter-argument]
5/ [Evidence/experience]
6/ [The nuanced truth]
7/ [Engagement question]
```

### Thread-specific techniques

**The Open Loop** — end tweet 1 with incomplete information resolved in tweet 2:
- "Here's what happened next:"
- "But here's the thing nobody tells you:"
- "The real story is more interesting:"

**The Cliffhanger** — use at the end of tweets 2–5 to maintain momentum:
- "And then it got worse."
- "But that wasn't the real lesson."
- "Here's where it gets interesting:"

**The Pattern Interrupt** — break expected flow to recapture attention:
- "Stop."
- "Read that again."
- "This is the part most people skip."

Each follow-up tweet should serve a distinct role (the stakes, the how, the payoff) rather than just chopping a blog post into fragments.

---

## Format notes & engagement mechanics

(Guidance, not gospel — algorithm behavior shifts.)

- Plain **text-first posts** remain the most reliable format overall — often outperforming video on engagement rate. Write posts that are easy to scan, spark curiosity, and invite replies.
- The **confident one-sided opinion** — state something not everyone agrees with, defend it without hedging, no "on the other hand" — is one of the strongest single-tweet formats because it drives reply-chain behavior. Use it for Opinion/Hot Take, not for Breaking News or Facts.
- **Numbered lists** (5 things, 7 habits, 10 mistakes) reliably outperform generic posts because the format sets clear expectations. Maps directly to Listicle style.
- **"I tested/tried X for Y timeframe, here's what I found"** posts get high saves because they represent condensed, done-for-you research — works for tech and non-tech. This is the Personal Story / Experiment style.
- **Threads**: sources differ on ideal length (some say 4–8, others 8–12), but they agree on structure — tweet 1 must stand alone as a hook, and each subsequent tweet should serve a distinct role.
- **Replies to larger, relevant accounts** currently carry outsized algorithmic weight — worth mentioning to the user as a growth lever, though outside this skill's scope of drafting standalone posts.

### Algorithm signals (commonly reported)
- Time-on-post (longer = better)
- Quick engagement in the first hour
- Replies and quote tweets
- Saves and shares

### Posting cadence & timing (optional advice, only if the user asks)
- Commonly cited best windows: Tuesday–Thursday, 9–11am and 1–3pm EST (adjust to the user's actual audience time zone)
- Consistency matters more than perfect timing
- 2–3 quality threads per week beats daily mediocrity

---

## Step 4: Verify before presenting (silent self-check)

- Character count(s) within limit — state the count(s).
- Every factual claim traces to Step 1's research (or is safe general knowledge for Random mode).
- No claim is more specific/confident than sources support.
- The chosen style's actual shape was followed, not just labeled.
- Nothing is optimized for virality at the expense of being true, useful, or actually sounding like the user.
- Quick checklist: Does the hook stop the scroll? Can each tweet stand alone? Is there a clear payoff for reading? Is the engagement ask earned? Zero corporate speak?

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
- **User asks for a "viral" story/experience post with no real facts**: don't invent the story, numbers, or results; ask for the real details or switch to a style that doesn't need personal claims.

---

## Appendix A — Full examples

These show structure, rhythm, and formatting. **The people, numbers, and results inside them are fictional illustrations of shape — do not reuse them as facts, and never present invented personal stories or stats as the user's real experience.**

### Single posts

#### Hot Take Post
```
Unpopular opinion:

The best time to start was 10 years ago.

The second best time is NOT today.

It's after you've actually thought through what you're starting and why.

"Just start" is lazy advice.
```
**Why it works**: Contrarian hook, challenges popular wisdom, makes reader think.

#### Observation Post
```
I've noticed something about successful people:

They don't manage time. They manage energy.

They know when they're sharp and protect those hours ruthlessly.

Everything else gets the scraps.
```
**Why it works**: Simple observation, feels insightful, actionable implication.

#### Quick Win Post
```
A negotiation trick that's worked every time:

When they make an offer, stay silent for 10 seconds.

Most people can't handle the pause.

They'll often improve the offer just to fill the silence.
```
**Why it works**: Specific technique, easy to try, immediate value.

#### Reframe Post
```
Reframe:

You're not "bad at networking."

You're bad at pretending to care about people you don't care about.

Solution: Stop going to networking events. Start helping people you actually like.
```
**Why it works**: Validates reader's struggle, offers new perspective, actionable advice.

### Thread examples

#### Storytelling Thread
```
1/ I got fired on my birthday.

No warning. No severance. Just a box and a security escort.

Here's what happened next (and how it became the best thing for my career):

2/ Some context:

I'd been at the company for 3 years.
Good reviews. Promotions. Everything seemed fine.

Then new leadership came in and cleaned house.

I was out.

3/ The first week was brutal.

I applied to 50 jobs. Got 2 responses.
Both rejections.

I started questioning everything about my career.

4/ Then I did something different.

Instead of applying to more jobs, I reached out to 10 people I admired and asked one question:

"If you were starting over today, what would you do differently?"

5/ The responses changed everything.

8 out of 10 said some version of:

"I would have bet on myself sooner."

They'd all spent years building someone else's dream before building their own.

6/ That's when it clicked.

Getting fired wasn't a setback.
It was a forced decision I'd been too scared to make myself.

I had nothing to lose now.

7/ I started freelancing that month.

First client: $500.
By month 6: $10K/month.
By year 2: More than my old salary.

Getting fired gave me permission to try.

8/ The lesson:

Sometimes the worst thing that happens to you is actually the best thing.

You just can't see it yet.

If you're going through something hard right now—keep going.

What's a setback that turned into your biggest breakthrough?
```
**Why it works**:
- Hook creates immediate curiosity
- Story has a clear arc (setup → conflict → resolution)
- Each tweet stands alone but builds the narrative
- Universal lesson at the end
- Ends with an engagement question

#### Listicle Thread
```
1/ 7 harsh truths about career growth that nobody wants to hear:

(Save this—you'll need it)

2/ 1. Your work doesn't speak for itself.

Never has. Never will.

The people who get promoted are the ones who make their work visible.

Stop waiting to be discovered.

3/ 2. Your manager doesn't owe you mentorship.

They have their own job to do.

If you want mentorship, make it easy for them. Come with specific questions, not vague requests.

4/ 3. Being busy isn't the same as being valuable.

Nobody cares how many hours you worked.

They care about results.

Work less. Deliver more.

5/ 4. Your degree matters less every year you're out of school.

By year 5, nobody cares where you went to college.

They care what you've done since.

6/ 5. The best opportunities aren't posted.

They're created through relationships.

If you're only applying to job postings, you're competing with 500 other people.

7/ 6. Nobody is coming to save your career.

Not HR. Not your manager. Not the company.

You are the CEO of your own career.

Act like it.

8/ 7. Your "dream job" is probably a fantasy.

Every job has boring parts.

Stop looking for perfect. Start looking for growth.

Which one hit hardest? Reply with the number.
```
**Why it works**:
- Clear promise in the hook
- Each tweet is a standalone insight
- Consistent structure throughout
- "Save this" CTA early
- Engagement prompt at the end

#### Problem-Solution Thread
```
1/ Most people are terrible at cold emails.

Here's the exact template that got me a 40% response rate:

(Including the psychology behind why it works)

2/ First, why most cold emails fail:

- Too long
- Too much about you
- No clear ask
- Generic flattery

The reader thinks: "What do they want and why should I care?"

3/ The template (steal this):

Subject: [Specific thing you noticed about them]

[One sentence about what impressed you - be specific]

[One sentence about why you're reaching out]

[One clear, small ask]

[Your name]

That's it. 4-5 sentences max.

4/ Let's break down each part:

SUBJECT LINE:
Make it specific to them.

Bad: "Quick question"
Good: "Your thread on pricing strategy"

Specificity = they know you actually did your homework.

5/ THE OPENER:

One genuine, specific compliment.

Bad: "I love your content"
Good: "Your breakdown of the Amazon flywheel is the clearest explanation I've seen"

Specific > Generic. Always.

6/ THE REASON:

Why are you reaching out? Make it about THEM, not you.

Bad: "I'd love to pick your brain"
Good: "I'm working on a similar problem and think you might have insight"

7/ THE ASK:

Make it small and easy to say yes to.

Bad: "Can we hop on a 30-min call?"
Good: "Would you be open to a 2-question email exchange?"

Lower barrier = higher response rate.

8/ Real example that worked:

Subject: Your pricing experiment

Hey [Name],

Your thread on testing price elasticity was exactly what I needed. The spreadsheet framework was genius.

I'm running similar tests and hit a wall with sample size.

Would you be open to a quick email exchange? Just 2 questions.

Thanks,
[Me]

Response rate: 40%+

9/ Why this works:

1. Shows you paid attention (specific reference)
2. Shows you're doing the work (not just asking for free advice)
3. Makes saying yes easy (2 questions via email)

Respect their time. Be specific. Make it easy.

Save this for your next cold outreach.
```
**Why it works**:
- Specific promise with social proof
- Teaches the "why," not just the "what"
- Includes a real example
- Each tweet adds new value
- Actionable and immediately usable

*(Note: this example runs 9 tweets, above the 3–8 default — acceptable only because it is a step-by-step tutorial where every tweet adds a distinct piece.)*

### Formatting reminders from the examples
- **Short sentences**: easier to scan
- **White space**: line breaks between thoughts
- **Numbered threads**: 1/, 2/, 3/ format
- **Cliffhangers**: keep readers moving forward
- **Engagement ask**: end with a question or save prompt (when earned)
- **No hashtag clutter**: 0–2 max, at the end if used

---

## Appendix B — AI News Research workflow

Use this in **News mode**, or any time the user asks "what's new in AI," wants updates on a specific AI company, or wants posts based on the latest AI developments. It compiles verified news first; posts are then written from the findings using the main workflow above.

### Companies to track

**Frontier labs**: OpenAI · Anthropic · Google DeepMind / Google AI · Meta AI / FAIR · xAI

**Tech giants**: Microsoft AI · Amazon AWS AI / Bedrock · Nvidia · Apple (Apple Intelligence) · Salesforce (Einstein AI) · IBM (watsonx)

**AI startups & specialists**: Mistral AI · Cohere · Stability AI · Runway · Hugging Face · Perplexity AI · other emerging labs

### Topics to cover
1. **Product launches & updates** — new models, features, API changes
2. **Research breakthroughs** — papers, benchmarks, capabilities
3. **Regulations & policy** — government actions, safety initiatives, legal developments
4. **Industry trends** — funding, partnerships, acquisitions, market moves
5. **Enterprise AI adoption** — real-world implementations, case studies, ROI reports

### Step B1: Run searches

Use the built-in **web search** tool for finding stories and **web fetch** to open the actual article or official announcement page (search snippets are often too thin). Run several targeted searches rather than one broad one, and use extended/deeper search for hard-to-find or very recent items.

Always put the **current month and year** (from the actual current date, not a stale one) in queries for better recency. Run company searches in parallel where possible, using the template:

```
Company news (run in parallel):
- "OpenAI announcement news [Month Year]"
- "Anthropic Claude news [Month Year]"
- "Google Gemini AI news [Month Year]"
- "Microsoft AI Copilot news [Month Year]"
- "Meta Llama AI news [Month Year]"
- "Nvidia AI news [Month Year]"
- "xAI Grok news [Month Year]"
- "Amazon AWS Bedrock AI news [Month Year]"
- "Mistral AI news [Month Year]"
- "Apple Intelligence news [Month Year]"

Industry topics (run in parallel):
- "AI regulation policy news [Month Year]"
- "AI research breakthrough news [Month Year]"
- "AI startup funding investment news [Month Year]"
- "enterprise AI deployment case study [Year]"
```

For deeper analysis, run a broader multi-search pass with a query like:
> "What are the most significant AI industry developments in the last 48 hours? Include product launches, research breakthroughs, regulatory changes, and major funding announcements. Focus on verified announcements from official sources."

**Search tips**
- Use company + product names for precision (exact current model/product names, not remembered old ones)
- Include current month/year in queries
- Run company searches in parallel for efficiency
- Use deep research for synthesizing trends across multiple sources
- Preserve citations in the output

### Step B2: Filter for recency
Include stories from the last 24–48 hours. Use 24 hours for daily briefings; extend to 48 hours on Mondays or slow news days to capture weekend developments.

### Step B3: Deduplicate
- Identify stories appearing across multiple searches
- Consolidate duplicates into a single entry
- Use the most authoritative source (official blog > news outlet > aggregator)
- Note if multiple sources cover the same story (signals higher significance)

### Step B4: Verify major claims
- Cross-reference against official company blogs, press releases, or verified accounts
- Check whether multiple reputable sources confirm the story
- Flag unverified or single-source stories as "Developing" or "Unconfirmed"

### Step B5: Compile results
Format as bullet points with source links:

```markdown
## AI News - [Date]

### Company Updates
- **[Company]**: [Brief summary of news] ([Source](url))

### Product Launches
- [Product/feature description] ([Source](url))

### Research & Breakthroughs
- [Research summary] ([Source](url))

### Regulation & Policy
- [Policy development] ([Source](url))

### Enterprise Adoption
- [Company/industry implementation story] ([Source](url))

### Industry Trends
- [Trend/funding/partnership] ([Source](url))
```

### Step B6: Prioritize
Order stories by significance:
1. Major model releases or capabilities
2. Significant policy/regulatory changes
3. Large funding rounds or acquisitions
4. Research breakthroughs
5. Enterprise adoption stories with measurable outcomes
6. Product updates and features

### Output guidelines for the news roundup
- Keep summaries to 1–2 sentences per story
- Always include source links
- Group related stories together
- Note if a category has no news ("No significant updates")
- Flag breaking/developing stories with a "[DEVELOPING]" prefix
- Flag unverified stories with an "[UNCONFIRMED]" prefix
- Prefer official sources over secondary coverage

### From news to posts
After compiling, the news roundup itself is shown as a normal chat answer (the one exception to "tweets only" below). If the user wants posts, pick the top 1–3 stories, then go through Step 2 → Step 5 of the main workflow for each — typically **Breaking News** or **Product Launch** style, no hype adjectives, no CTA, only facts confirmed in Step B4, and no [UNCONFIRMED] item turned into an assertive tweet.
