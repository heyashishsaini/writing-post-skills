---
name: writing-blog-posts
description: Write complete, publish-ready blog posts and long-form articles, such as how-to tutorials, listicles, opinion pieces, case studies, news explainers, comparisons and roundups, with title options, meta description, slug and SEO-aware structure. Use this skill whenever the user asks for a blog post, article, long-form piece, newsletter essay, or a post for Medium, Dev.to, Hashnode, WordPress, Substack or their own site; asks for a blog outline, intro, headline options or an SEO pass; wants a draft rewritten or tightened; or wants a tweet, thread, LinkedIn post, link, video or rough notes turned into a blog, even if they only say "write about X" and the piece is clearly longer than a social post. Not for tweets or threads (use writing-x-posts) or LinkedIn posts (use writing-linkedin-posts).
---

# Writing Blog Posts

Write blog posts that a real reader finishes, trusts and can act on. A good post has one clear promise, earns each section, and is honest about what it knows.

## How to Use This Skill

This file is the workflow and the rules. Load a reference only when the step needs it:

- **Choosing a structure for the post type** -> `references/post-types.md`
- **Title, intro and conclusion wording** -> `references/headlines-and-intros.md`
- **Search visibility, meta fields, publishing checks** -> `references/seo-checklist.md`
- **Seeing the standard in practice** -> `references/examples.md`

Numbers, names and claims inside the reference files illustrate patterns. Never reuse them as facts, and never invent stats, quotes, benchmarks or results.

## Workflow

### Step 1: Pin down the brief

Work out these seven things. Take what the user already said, infer what is obvious, and ask only for what is missing and would change the post.

| Item | Default if the user does not say |
|------|----------------------------------|
| Topic and the one thing the reader should walk away with | Required. Ask if unclear |
| Reader (who they are, what they already know) | A smart beginner in the topic |
| Goal (teach, persuade, announce, rank on search, build authority) | Teach |
| Post type | Pick from `references/post-types.md` and say which |
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

For search-driven posts, name the primary keyword and the search intent behind it (see `references/seo-checklist.md`).

### Step 4: Outline

Build the outline from the post type's skeleton in `references/post-types.md`. Each section should answer one question the reader would ask next.

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

Clear first, clever second. Promise a specific outcome the reader wants. Roughly 50 to 60 characters keeps it intact in search results. Offer three options with different angles, and mark the one you recommend. Formulas and phrases to retire are in `references/headlines-and-intros.md`.

### Intro (about 80 to 150 words)

The intro has four jobs: show the reader this is about their problem, state what they will get, give a reason to trust the author, and let them start reading the body. Open with the problem, a concrete moment, or the direct answer. Do not open with a dictionary definition, "In today's fast-paced world", or a history of the internet.

### Body

- One idea per section, with a descriptive heading that makes sense on its own (readers skim headings).
- Short paragraphs, usually 2 to 4 sentences.
- Use a list when items are parallel, a table when comparing across attributes, a code block for anything the reader will copy, and an image or diagram only when it explains something words cannot.
- Use examples early in each section, not after three paragraphs of abstraction.
- Link to sources where claims are made, and to the author's related posts when the user supplies them.

### Conclusion

Land the point. Restate the one takeaway in fresh words, give the next concrete step, and stop. Do not recap every section, and do not end with "I hope you enjoyed this". Optional: one honest question or a pointer to a related post. Patterns are in `references/headlines-and-intros.md`.

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

## Repurposing

A finished blog post is good source material. When asked, or when it clearly helps, offer to turn it into an X thread (`writing-x-posts`) or a LinkedIn post (`writing-linkedin-posts`). Adapt for each platform; do not paste the same text. In the other direction, when turning a tweet or LinkedIn post into a blog, expand with evidence, steps and examples rather than stretching the original sentences.

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
