---
name: writing-blog-posts
description: Write complete, publish-ready blog posts and long-form articles, such as how-to tutorials, listicles, opinion pieces, case studies, news explainers, comparisons and roundups, with title options, meta description, slug and SEO-aware structure. Use this skill whenever the user asks for a blog post, article, long-form piece, newsletter essay, or a post for Medium, Dev.to, Hashnode, WordPress, Substack or their own site; asks for a blog outline, intro, headline options or an SEO pass; wants a draft rewritten or tightened; or wants a tweet, thread, LinkedIn post, link, video or rough notes turned into a blog, even if they only say "write about X" and the piece is clearly longer than a social post. Not for tweets or threads (use writing-x-posts) or LinkedIn posts (use writing-linkedin-posts).
---

# Blog Post Writer

Write blog posts that a real reader finishes, trusts and can act on. A good post has one clear promise, earns each section, and is honest about what it knows.

This single file contains everything needed:

1. [Core Writing Guide](#part-1-core-writing-guide) - workflow, principles, structure, length, quality rules, output format
2. [Post Types and Structures](#part-2-post-types-and-structures) - skeletons for tutorials, listicles, opinion, case studies, explainers, comparisons, roundups, pillar guides
3. [Titles, Intros and Conclusions](#part-3-titles-intros-and-conclusions) - formulas, patterns, mistakes, before and after
4. [SEO and Publishing Checklist](#part-4-seo-and-publishing-checklist) - search intent, on-page elements, pre-publish checks
5. [Examples](#part-5-examples) - brief, outline, full short post, revision note, delivery block

Numbers, names and claims in Parts 2 to 5 illustrate patterns. Never reuse them as facts, and never invent stats, quotes, benchmarks or results.

**Suggested workflow**: pin down the brief (Part 1) → pick a post type (Part 2) → research if facts matter → outline → draft → write the title and intro (Part 3) → check SEO basics (Part 4) → run the Quick Checklist.

---

# Part 1: Core Writing Guide

## Workflow

### Step 1: Pin down the brief

Work out these seven things. Take what the user already said, infer what is obvious, and ask only for what is missing and would change the post.

| Item | Default if the user does not say |
|------|----------------------------------|
| Topic and the one thing the reader should walk away with | Required. Ask if unclear |
| Reader (who they are, what they already know) | A smart beginner in the topic |
| Goal (teach, persuade, announce, rank on search, build authority) | Teach |
| Post type | Pick from Part 2 (Post Types and Structures) and say which |
| Length | See the length table below |
| Language | The language the user writes in; see "Language and voice" |
| Voice | Plain, direct, first person if the user has experience to share |

Ask at most one short round of questions. If the user has given enough, skip questions, state your assumptions in one line, and write.

### Step 2: Research when facts matter

- Posts about AI news, launches or any current event, and any post that leans on facts, numbers, versions, prices, laws or "latest" claims: search the web and fetch primary sources (official blogs, docs, announcements) before drafting. Check the real current date first so queries are not stale. Use only facts you verified, with their sources.
- Opinion, personal story and lessons-learned posts need the user's own experience more than research. Ask for specifics (what happened, what they tried, what changed) instead of inventing them.
- If research finds nothing reliable, say so and write around the gap. Do not fill it.

### Step 3: Choose the angle and the promise

Finish this sentence before outlining: "After reading, the reader will be able to / will understand / will decide ___."

Then check the angle against what already exists. A post that repeats the top ten search results adds nothing. Find the specific thing this author can add: first-hand experience, a sharper example, a clearer explanation, a contrary view with reasons, fresher facts.

For search-driven posts, name the primary keyword and the search intent behind it (see Part 4 (SEO and Publishing Checklist)).

### Step 4: Outline

Build the outline from the post type's skeleton in Part 2 (Post Types and Structures). Each section should answer one question the reader would ask next.

- Posts over about 1,200 words, or when the user asks for an outline: show the outline first and let them adjust it.
- Shorter posts: outline silently and go to the draft.

### Step 5: Draft

Write the full post, not a summary of one. Follow the principles and structure below. Put the answer or the payoff early; do not make the reader wait through setup.

### Step 6: Edit pass

Reread as a skeptical reader and fix before delivering:

- Cut any sentence that could appear in any blog on any topic.
- Replace vague claims ("many companies", "significantly faster") with a specific fact, or remove them.
- Check that every number, quote and named claim traces to the user or a source you retrieved.
- Remove the AI tells listed in "Writing quality" below.
- Run the checklist at the end of this file.

### Step 7: Deliver

Use the output format below. After the post, offer one or two useful next steps (for example a LinkedIn or X version via the sibling skills), not a menu.

## Core Principles

### One promise per post

A post that tries to cover everything teaches nothing. If the outline has two promises, it is two posts. Say which one you cut and offer it as a follow-up.

### Reader first

Start from the reader's problem, not the writer's topic. "How to cache API responses in Node" beats "My thoughts on caching". Define a term the first time a beginner would trip on it, and skip definitions an expert reader would find insulting.

### Specific beats general

Prefer the exact command, the real number with its source, the named tool, the concrete before and after. Specifics are what make a post feel written by someone who did the thing.

### Earn trust

- Show the work: steps that can be followed, code that runs, sources that can be opened.
- State limits: when something is untested, version-specific or only true in some cases, say so.
- Separate fact from opinion. Opinions are welcome, labelled as the author's view with the reasoning.

### Respect attention

Every section must justify its place. Length should come from substance, never from padding to hit a word count.

## Structure of a Post

### Title

Clear first, clever second. Promise a specific outcome the reader wants. Roughly 50 to 60 characters keeps it intact in search results. Offer three options with different angles, and mark the one you recommend. Formulas and phrases to retire are in Part 3 (Titles, Intros and Conclusions).

### Intro (about 80 to 150 words)

The intro has four jobs: show the reader this is about their problem, state what they will get, give a reason to trust the author, and let them start reading the body. Open with the problem, a concrete moment, or the direct answer. Do not open with a dictionary definition, "In today's fast-paced world", or a history of the internet.

### Body

- One idea per section, with a descriptive heading that makes sense on its own (readers skim headings).
- Short paragraphs, usually 2 to 4 sentences.
- Use a list when items are parallel, a table when comparing across attributes, a code block for anything the reader will copy, and an image or diagram only when it explains something words cannot.
- Use examples early in each section, not after three paragraphs of abstraction.
- Link to sources where claims are made, and to the author's related posts when the user supplies them.

### Conclusion

Land the point. Restate the one takeaway in fresh words, give the next concrete step, and stop. Do not recap every section, and do not end with "I hope you enjoyed this". Optional: one honest question or a pointer to a related post. Patterns are in Part 3 (Titles, Intros and Conclusions).

## Length Guide

Length follows the promise. These ranges are starting points, not targets.

| Post type | Typical length |
|-----------|----------------|
| Opinion or short take | 600 to 1,000 words |
| News explainer | 700 to 1,200 words |
| How-to or tutorial | 1,000 to 2,000 words |
| Listicle or roundup | 900 to 1,800 words |
| Case study or story | 900 to 1,600 words |
| Comparison or review | 1,200 to 2,200 words |
| Pillar or complete guide | 2,500 words and up |

If the user gives a word count, follow it.

## Writing Quality

Write like a person explaining something to a colleague: plain words, active verbs, varied sentence length. Watch for these tells of autopilot writing and rewrite them:

- Stock openers and closers ("In today's digital landscape", "In conclusion", "Let's dive in").
- Inflated words used as filler (leverage, robust, seamless, game-changer, unlock, delve, landscape).
- "Not just X, but Y" contrasts and three-item lists used by reflex.
- Claims of importance without a reason ("This is crucial", "It's no secret that").
- Headings that are labels with no information ("Overview", "Final Thoughts").
- Heavy bold, emoji and em dashes used for rhythm instead of meaning.

If a draft in the user's voice is available, match its vocabulary, sentence length and level of formality instead of the defaults here.

## Language and Voice

- Write in the language the user asks in or writes in. If they write in Hindi or Hinglish, or ask for a Hindi post, write in that language (Devanagari unless they ask for Roman script). Keep established technical terms in English, as a developer would say them aloud.
- Keep slugs, code, commands, file names and meta field names in English and ASCII regardless of the post language.
- Use first person only for experience the user actually has. When the user has not supplied experience, write in second person or neutral voice rather than inventing a story.
- Match the platform's norms: personal and casual on Medium or Substack, precise and code-first on Dev.to or Hashnode, structured and scannable for company or SEO blogs.

## Facts, Sources and Honesty

- Every statistic, quote, date, version number, price and attribution must come from the user or from a source retrieved in this conversation. Link it.
- Paraphrase sources in your own words. Short quotes only, with attribution. Never reproduce long passages, lyrics or poems.
- Do not invent personal anecdotes, customer stories, case-study numbers, testimonials or "I tested this" claims. If the post needs one, ask the user for the real detail or leave a clearly marked placeholder such as `[ADD: your real result here]`.
- For code and commands, only include what you are confident works; mention the version or environment it was written for. If it could not be run, say that.
- For medical, legal and financial topics, stay with well-sourced general information and note when a professional should be consulted.

## Output Format

Default to Markdown, which pastes cleanly into WordPress, Medium, Dev.to, Hashnode, Ghost and Substack. Deliver in this order:

```
**Title options**
1. ... (recommended)
2. ...
3. ...

**Meta description** (140 to 155 characters)
**Slug** (lowercase, hyphens, ASCII)
**Excerpt** (1 to 2 sentences, optional)

---

# [Chosen title]

[Full post in Markdown]

---

**Sources** (links used)
**Placeholders to fill** (only if any)
**Next steps** (internal links to add, image ideas, social versions)
```

- If the user names a platform that uses front matter (Dev.to, Hashnode, Jekyll, Hugo, Astro), add the matching front matter block with title, description, tags and slug filled in. Do not invent fields the platform does not use.
- If the user asks for a file, create it as `.md` (or the format they name) and present it. Otherwise answer in the reply.
- Keep commentary outside the post to a few lines.

## Revising an Existing Draft

When the user supplies a draft, do not rewrite it from scratch unless asked. First say in a few lines what is working and what the three biggest problems are (promise, structure, specificity, intro, length, accuracy). Then apply the fixes while keeping the author's voice and facts. If they asked only for an SEO pass or a proofread, do only that.


## Quick Checklist Before Delivering

1. **Promise**: Can the post's single takeaway be said in one sentence?
2. **Reader**: Is it pitched at the right level, with no unexplained jargon and no insulting basics?
3. **Intro**: Does it reach the point within the first 150 words?
4. **Structure**: Does each heading carry information, and does each section answer the reader's next question?
5. **Specifics**: Are there real examples, steps, numbers or code instead of generalities?
6. **Facts**: Does every claim trace to the user or a linked source? Are placeholders marked?
7. **Style**: Are the autopilot tells gone, and does it sound like a person?
8. **SEO basics**: Title, meta description, slug and headings done without keyword stuffing?
9. **Ending**: Does it land the takeaway and give a next step, then stop?

---

# Part 2: Post Types and Structures

Pick the type that matches the reader's intent, say which one you chose, and use its skeleton as a starting point. Adapt freely; a skeleton is a floor, not a mold.


## 1. How-to / Tutorial

**Use when**: the reader wants to do something specific and will follow along.

**Skeleton**
1. Intro: the problem, the end result, who this is for
2. Prerequisites: tools, versions, knowledge assumed
3. Steps, each with: what to do, the exact command or action, what the reader should see afterwards
4. Troubleshooting: the two or three errors people actually hit
5. Recap and next step

**Rules**
- Number the steps. One action per step.
- Show expected output so the reader knows they are on track.
- State versions and operating systems. Never present untested commands as working.
- Put copyable material in code blocks, and explain why for any step that is not obvious.

**Pitfalls**: skipping a step "everyone knows", changing the example midway, no result shown at the end.

---

## 2. Listicle

**Use when**: the reader wants options, tips or a checklist to scan.

**Skeleton**
1. Intro: why this list, how items were chosen
2. Items, each with a heading, a short explanation, and one concrete example or use
3. Closing: how to choose among them, or the one to start with

**Rules**
- The number in the title must match the number of items.
- Order with intent (by importance, by difficulty, by workflow order) and say which.
- Every item must stand on its own. Cut weak items instead of padding to a round number.
- Each item needs something specific: a how, a when, or a caveat.

**Pitfalls**: items that are one vague sentence each, overlapping items, filler to reach ten.

---

## 3. Opinion / Thought leadership

**Use when**: the author has a view and reasons for it.

**Skeleton**
1. Intro: the claim, stated plainly
2. The common view and why people hold it
3. Why the author sees it differently: reasons, evidence, first-hand experience
4. The strongest objection, answered fairly
5. What the reader should do or think differently

**Rules**
- Argue against ideas, not people.
- Label opinion as opinion and give the reasoning. A bold take with no reasons is just noise.
- Acknowledge what the other side gets right. It makes the argument stronger.
- Only use experience the author really has.

**Pitfalls**: strawman opponents, universal claims ("always", "never"), no stakes.

---

## 4. Case study / Personal story

**Use when**: the author did something real and the lesson is transferable.

**Skeleton**
1. Intro: the situation and the outcome in a line or two
2. Context: who, what constraints, what was at stake
3. What was tried, including what did not work
4. The turning point and what changed
5. Results, with real numbers only if the author supplied them
6. Lessons the reader can apply

**Rules**
- Ask the author for the real details. Never fabricate numbers, names or quotes. Use `[ADD: ...]` placeholders when something is missing.
- Include the failures. They are what makes the story credible.
- Keep the lessons tied to events in the story, not generic advice.

**Pitfalls**: a victory lap with no friction, lessons that could have been written without the story.

---

## 5. News analysis / Explainer

**Use when**: something just happened or changed and the reader wants to know what it means.

**Skeleton**
1. Intro: what happened, in one or two sentences, with the date
2. Key facts, with sources linked
3. Why it matters and to whom
4. What it changes in practice, or what to do now
5. What is still unknown or disputed
6. Short closing view from the author, labelled as such

**Rules**
- Search the web and read primary sources (official announcements, docs, papers) before writing.
- Lead with confirmed facts. Keep speculation separate and labelled.
- Prefer official announcements, documentation, filings and papers over commentary about them.
- Date the post and flag details that may change.

**Pitfalls**: repeating a press release, burying the news, presenting rumours as facts.

---

## 6. Comparison / Review

**Use when**: the reader is choosing between options.

**Skeleton**
1. Intro: who is choosing, the criteria that matter, a short verdict up front
2. Criteria and how each option was evaluated
3. Side-by-side table for the facts
4. Each option: strengths, weaknesses, best for whom
5. Recommendation by reader situation ("choose A if..., choose B if...")

**Rules**
- Say how the comparison was done. If the author did not use the products, say the comparison is based on documentation and public information.
- Verify prices, limits and features at publishing time and date them.
- Disclose affiliate links, sponsorships and any relationship with the vendor.
- Include honest downsides for the option you favour.

**Pitfalls**: invented hands-on claims, stale pricing, a verdict that ignores the stated criteria.

---

## 7. Roundup / Curation

**Use when**: the author gathers the best resources, news or tools on a topic.

**Skeleton**
1. Intro: scope, time period, selection criteria
2. Grouped items, each with a link, a one to three sentence summary in the author's words, and why it matters
3. Closing: the one item to read first, or a pattern across them

**Rules**
- Add value through selection and commentary, not just links.
- Summarize in your own words. Do not copy blurbs or quote at length.
- Check each link opens and says what you claim.

**Pitfalls**: a link dump with no judgement, outdated items.

---

## 8. Pillar / Complete guide

**Use when**: the author wants one definitive resource on a broad topic that other posts can link to.

**Skeleton**
1. Intro and who the guide is for
2. Table of contents with anchor links
3. Foundations: the concepts everything else depends on
4. Main sections ordered from basic to advanced, each linking to a deeper post where one exists
5. Common mistakes
6. FAQ drawn from real questions
7. Summary and where to go next

**Rules**
- Plan the whole structure first and show the outline before drafting.
- Draft in sections and keep terminology consistent throughout.
- Each section should be useful on its own, since readers jump around.

**Pitfalls**: length without depth, repeating the same point under different headings.


---

# Part 3: Titles, Intros and Conclusions

## 1. Titles

### What a good title does

- States a specific outcome or a specific claim
- Uses the words the reader would actually search or say
- Is honest: the post delivers what the title promises
- Stays around 50 to 60 characters so search results do not cut it off (a little longer is fine if it reads well)

### Formulas that work

| Pattern | Template | Use for |
|---------|----------|---------|
| Direct how-to | How to [achieve result] with [tool/method] | Tutorials |
| Outcome plus constraint | [Result] without [common pain] | Tutorials, guides |
| Specific number | [N] [things] for [reader] that [benefit] | Listicles |
| Question the reader has | Should you [choice] or [choice]? | Comparisons |
| Plain claim | [Claim stated directly] | Opinion |
| Lesson from experience | What [specific experience] taught me about [topic] | Stories |
| News plus meaning | [Thing] just changed: what it means for [reader] | Explainers |
| Versus | [A] vs [B]: which to pick for [situation] | Comparisons |

### Titles to retire

- Clickbait that the post does not pay off ("You won't believe...")
- Empty superlatives ("The ultimate guide to everything")
- Vague labels ("Thoughts on AI", "Some tips")
- Fake urgency ("Stop doing this immediately")
- Keyword strings ("Blog writing tips blog writing SEO blog tips")

### Process

Write ten rough titles, discard the vague ones, then offer three with different angles (for example direct, curiosity, claim). Mark one as recommended and say why in a few words.

---

## 2. Intros

### The four jobs

1. **Recognition**: the reader sees their own problem or question
2. **Promise**: what they will get or be able to do
3. **Credibility**: why this author or this post is worth trusting (one line, specific)
4. **Momentum**: a reason to keep reading, with the body starting quickly

Keep it to about 80 to 150 words for most posts. Shorter for opinion pieces, slightly longer for pillar guides.

### Patterns

**Problem first**
Name the situation the reader is in, then the cost of it, then the promise.
> Your build takes eleven minutes and nobody remembers why. This post walks through finding the slow step and cutting it, using only the tools already in your repo.

**Concrete moment**
Open on a specific scene the author actually experienced, then connect it to the reader.
> Use only with a real experience supplied by the user. Do not invent a scene.

**Answer first**
Give the conclusion in the first lines, then explain it. Works for explainers and comparisons.
> Short answer: choose the smaller plan unless you need X. Here is how to tell.

**Contrarian claim**
State a view that cuts against the common one, and promise the reasoning.
> Most advice on this gets the order backwards. Here is the order that worked, and why.

**Surprising fact**
Lead with a verified, sourced fact that reframes the topic. Link the source. If it cannot be verified, do not use this pattern.

### Intro mistakes

- Starting with a definition or a history lesson
- "In today's fast-paced digital world..." or any opener that fits every topic
- Announcing the structure of the post instead of giving a reason to read it
- Apologising or hedging ("I'm no expert, but...")
- Burying the promise below the second paragraph

---

## 3. Conclusions

### Patterns

**Takeaway plus next step**
Restate the single takeaway in new words, then give one concrete action.
> The fix was a single config change. Check your CI cache settings first; if that is already on, move to step three.

**Looking ahead**
For news and trend posts: what to watch next and what would change the view. Keep it grounded in facts.

**Honest limits**
Name what the post did not cover or what remains uncertain, and where the reader can go next.

**Open question**
One real question the author wants answers to. Do not use it as engagement bait.

### Conclusion mistakes

- A full recap of every section
- "I hope you enjoyed this post" or "Thanks for reading!" as the main content
- A call to action unrelated to the post ("Subscribe to my newsletter" with no reason)
- Introducing a new major idea at the end

---

## 4. Before and after

### Intro

**Before**
> In today's fast-paced world, productivity is more important than ever. Many people struggle to manage their time effectively. In this blog post, we will explore some tips that can help you become more productive.

Problems: could open any post, no specific reader, no promise, no author voice.

**After**
> I used to start every day with forty browser tabs and no plan. Two small changes, a written top-three and a fixed shutdown time, fixed most of it. Here is exactly how I set them up, and where they failed before they worked.

Why it works: a specific situation, a specific fix, a promise of both method and failures. (The scene is an illustration; use only what the user really experienced.)

### Heading

**Before**: `Overview`, `Key Considerations`, `Final Thoughts`
**After**: `What the cache actually stores`, `Three settings that change build time`, `When this approach stops working`

Headings should carry information so a skimmer still learns something.


---

# Part 4: SEO and Publishing Checklist

Write for the reader first. SEO is how the right reader finds the post, not a reason to distort it. Use this file when the post is meant to rank, or when the user asks for an SEO pass.

Search engines change. Treat the guidance below as durable basics and avoid promising rankings or quoting exact algorithm rules.


## 1. Search intent

Before writing, decide what the searcher wants. The post type should match.

| Intent | The searcher wants | Best post types |
|--------|--------------------|-----------------|
| Learn | An explanation or answer | Explainer, pillar guide, how-to |
| Do | Steps to complete a task | How-to, tutorial |
| Compare or choose | Help deciding | Comparison, review, listicle |
| Find a specific thing | A particular page or tool | Resource page, roundup |

If the top results for the keyword are all step-by-step tutorials and the draft is an opinion essay, the post will not match. Check what exists (search the keyword) and either match the intent or deliberately offer a different, better angle.

## 2. Keyword use

- Choose one primary keyword (the phrase a reader would type) and a few related phrases and questions.
- Put the primary keyword naturally in: the title, the first 100 words, at least one H2, the slug and the meta description.
- Use related terms and synonyms where they fit the sentence. Never repeat the keyword to hit a count.
- If a sentence reads worse with the keyword, rewrite the sentence or drop the keyword there.
- Do not claim monthly search volumes or difficulty scores unless the user supplies them from a tool.

## 3. On-page elements

| Element | Guidance |
|---------|----------|
| Title tag / H1 | One H1 per post. About 50 to 60 characters. Primary keyword near the front when natural. |
| Meta description | 140 to 155 characters. States the benefit and matches the content. Active voice, no quote marks that get cut off. |
| Slug | Lowercase, hyphen-separated, ASCII, short, without stop words or dates unless needed. Example: `cache-node-api-responses`. |
| Headings | H2 for main sections, H3 for subsections. No skipped levels. Descriptive, and keyword in a few where natural. |
| Alt text | Describe the image for someone who cannot see it. Include a keyword only if it is truthfully relevant. |
| Excerpt | One or two sentences for archive pages and social previews. |

## 4. Structure for scanning and snippets

- Answer the main question near the top in a short, direct paragraph (about 40 to 60 words). This helps readers and can suit featured snippets.
- Use numbered lists for steps, bullet lists for parallel items, and tables for comparisons.
- Add a short table of contents with anchor links on posts over roughly 1,500 words.
- Add an FAQ section only when there are real, distinct questions readers ask. Write each answer in two to four sentences. Do not manufacture questions.
- Keep paragraphs short and use whitespace. Most readers skim on a phone.

## 5. Links and images

- **Internal links**: suggest two to five links to related posts or pages the user has. Use descriptive anchor text ("our guide to JWT refresh tokens"), not "click here". If the user has not given their other posts, list the topics to link to rather than inventing URLs.
- **External links**: link primary sources and documentation. Prefer official pages over aggregators. Do not link to a source you did not read.
- **Images**: suggest what each image should show and where it goes. Prefer original screenshots, diagrams and charts over stock photos. Compress files and set dimensions so the page does not shift while loading.
- Never invent URLs. Use only links the user supplied or that you retrieved.

## 6. Trust and freshness

- Show first-hand experience when the author has it: what they ran, built or saw.
- Add an author line and date. Mark updates ("Updated [date]: what changed") when facts change.
- Cite sources for factual claims, and keep time-sensitive facts (versions, prices, limits, rules) dated.
- Disclose affiliate links, sponsorships and partnerships clearly.
- For health, finance and legal topics, stick to well-sourced information and point to a qualified professional where appropriate.

## 7. Pre-publish checklist

**Content**
- [ ] One clear promise, delivered
- [ ] The answer or payoff appears early
- [ ] Every claim, number and quote is sourced or from the author
- [ ] No invented anecdotes, results or testimonials
- [ ] Code and commands tested or clearly marked untested, with versions

**SEO**
- [ ] Primary keyword in title, intro, one H2, slug, meta description, used naturally
- [ ] Meta description 140 to 155 characters
- [ ] One H1, ordered headings
- [ ] Internal and external links with descriptive anchors
- [ ] Alt text on every image

**Reader experience**
- [ ] Short paragraphs, scannable headings
- [ ] Table of contents on long posts
- [ ] A clear next step at the end
- [ ] Reads well on a phone

**Publishing**
- [ ] Author, date and any affiliate disclosure present
- [ ] Platform front matter or fields filled (tags, category, canonical URL if cross-posting)
- [ ] If republishing elsewhere, set a canonical link to the original


---

# Part 5: Examples

These show the shape and tone the skill aims for. Names, numbers and scenarios are illustrations. Never reuse them as facts in a real post.


## 1. Example brief and assumptions line

**User**: "Write a blog post on how to add a new skill to my Claude Code plugin."

**Assumptions line to show before the draft**
> Assuming: reader is a developer who already uses Claude Code, goal is to teach, post type is a how-to tutorial, about 900 words, English. Tell me if any of that is off.

No clarifying questions are needed: the topic, reader and type are clear enough to start.

---

## 2. Example outline (tutorial)

**Promise**: After reading, the reader can add a working skill to an existing plugin and install it.

1. Intro: the problem (a plugin with skills, and a new task with no skill) and the result
2. What you need: an existing plugin repo, Claude Code installed
3. Step 1: Create the skill folder under `skills/`
4. Step 2: Write `SKILL.md` with a description that says when to trigger
5. Step 3: Add references only if the skill needs them
6. Step 4: Update the README and manifest keywords
7. Step 5: Install locally and test with a real prompt
8. Troubleshooting: the skill never triggers, wrong folder level
9. Next step: tighten the description from what the test showed

Each step ends with what the reader should see.

---

## 3. Example short post (full)

Title options: (1) How to Add a Skill to a Claude Code Plugin (recommended: direct, matches the search) (2) One Folder, One File: Adding a Skill to Your Plugin (3) Add a New Skill to Your Plugin in Five Steps

**Meta description**: Add a new skill to a Claude Code plugin: create the folder, write SKILL.md, test it locally and update your docs. A short step-by-step guide.

**Slug**: `add-skill-to-claude-code-plugin`

---

## 4. Example revision note (draft feedback)

Use this shape when the user supplies a draft.

> **What works**: the opening story is specific, and the code samples are clear.
> **Biggest problems**
> 1. The promise is unclear: the title says "complete guide" but the post covers one technique. Narrow the title or add the missing parts.
> 2. Sections three and five make the same point. Merge them.
> 3. Two numbers have no source. Add links or remove them.
>
> I kept your voice and examples, tightened the intro, merged the two sections and marked the unsourced numbers with `[ADD SOURCE]`.

---

## 5. Example delivery block

```
**Title options**
1. How to Cache API Responses in Node.js (recommended)
2. Stop Hitting Your API Twice: A Practical Caching Guide
3. API Caching in Node.js: What to Cache and for How Long

**Meta description** (151 characters)
Learn how to cache API responses in Node.js: what to store, how long to keep it, and how to avoid stale data, with working code examples.

**Slug** cache-api-responses-nodejs

---

# How to Cache API Responses in Node.js
[post body]

---

**Sources**: [links retrieved in this session]
**Placeholders to fill**: [ADD: your measured speedup]
**Next steps**: link to your Express setup post; add a diagram of the cache flow; I can make an X thread or LinkedIn version.
```
