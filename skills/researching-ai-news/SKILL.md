---
name: researching-ai-news
description: Research and compile the latest AI news from across the industry using web search. Use this skill when asked to find AI news, get AI updates, research what's happening in AI, check for AI announcements, or gather intelligence on AI companies. Triggers include requests for "AI news", "latest AI developments", "what's new in AI", "AI industry updates", or news about specific AI companies (OpenAI, Anthropic, Google, Microsoft, Meta, Amazon, Nvidia, xAI, Mistral, Cohere, Apple, Salesforce). Also use it to ground LinkedIn or X posts about AI in verified, current facts.
allowed-tools: WebSearch, WebFetch
---

# Researching AI News

Research and compile AI news from across the industry using the built-in web search and web fetch tools. No external search MCP is required.

## References

- `references/companies.md` - Companies to track, with official blog/newsroom URLs for verification
- `references/output-format.md` - Full output template, section rules, and flag conventions

## Topics to Cover

1. **Product launches & updates** - New models, features, API changes
2. **Research breakthroughs** - Papers, benchmarks, capabilities
3. **Regulation & policy** - Government actions, safety initiatives, legal developments
4. **Industry trends** - Funding, partnerships, acquisitions, market moves
5. **Enterprise AI adoption** - Real-world implementations, case studies, ROI reports

Companies are grouped in `references/companies.md` (frontier labs, tech giants, startups).

## Research Workflow

### Step 0: Anchor to today's date

Never hardcode a month or year. Check today's date first and use the real current month and year in every query. Stale dates in queries are the most common cause of stale results.

### Step 1: Run Web Searches

Use `WebSearch` for discovery and `WebFetch` for reading primary sources.

- Run company searches in parallel (one query per company; never combine several companies into one query, since that returns shallow results for all of them).
- Keep queries short and specific (2-6 words) plus the current month/year.
- Start broad, then narrow with product names ("Claude", "GPT", "Gemini", "Llama", "Grok").
- Use the `allowed_domains` parameter of `WebSearch` to pin a search to official sources when verifying (see `references/companies.md`).
- Rewrite a query rather than repeating it if results are thin or stale.

**Company queries (run in parallel):**

```
- "OpenAI announcement [Month Year]"
- "Anthropic Claude news [Month Year]"
- "Google Gemini DeepMind news [Month Year]"
- "Microsoft AI Copilot news [Month Year]"
- "Meta Llama AI news [Month Year]"
- "Nvidia AI news [Month Year]"
- "xAI Grok news [Month Year]"
- "Amazon AWS Bedrock AI news [Month Year]"
- "Mistral AI news [Month Year]"
- "Apple Intelligence news [Month Year]"
```

**Industry topic queries (run in parallel):**

```
- "AI regulation policy news [Month Year]"
- "AI research breakthrough [Month Year]"
- "AI startup funding round [Month Year]"
- "enterprise AI deployment case study [Month Year]"
```

**Deep dives (replaces a separate "deep research" tool):** for a complex topic such as a regulatory development or an industry trend, run 3-5 narrower searches from different angles, then `WebFetch` the 2-4 most authoritative pages and synthesize them yourself. Do not rely on search snippets for anything you will state as a fact.

### Step 2: Filter for Recency

Include stories from the last 24-48 hours. Use 24 hours for daily briefings; extend to 48 hours on Mondays or slow news days to capture weekend developments. If the user asks for a different window (week, month), follow that instead.

### Step 3: Deduplicate Results

Before compiling output:
- Identify stories appearing across multiple searches
- Consolidate duplicates into a single entry
- Use the most authoritative source (official blog > reputable news outlet > aggregator)
- Note when several sources cover the same story (a signal of higher significance)

### Step 4: Verify Major Claims

For significant announcements:
- `WebFetch` the official company blog, press release, or documentation page and confirm the details there
- Check that at least two reputable outlets confirm the story
- Flag unverified or single-source stories as `[UNCONFIRMED]`; flag breaking stories as `[DEVELOPING]`
- If official pages cannot be reached, say so rather than guessing

### Step 5: Compile Results

Use the template in `references/output-format.md`. In short: bullet points grouped by category, 1-2 sentence summaries, and a source link on every story.

### Step 6: Prioritize

Order stories by significance:
1. Major model releases or capabilities
2. Significant policy/regulatory changes
3. Large funding rounds or acquisitions
4. Research breakthroughs
5. Enterprise adoption stories with measurable outcomes
6. Product updates and features

## Output Guidelines

- Keep summaries to 1-2 sentences per story, written in your own words (paraphrase; do not copy article text)
- Always include source links
- Group related stories together
- Note if a category has no news ("No significant updates")
- Flag breaking/developing stories with a `[DEVELOPING]` prefix
- Flag unverified stories with an `[UNCONFIRMED]` prefix
- Prefer official sources over secondary coverage
- Never invent figures, dates, or quotes; if a detail is not in a source you read, leave it out

## Tool Reference

| Tool | Use Case |
|------|----------|
| `WebSearch` | Discovery: company news, targeted queries, finding the primary source |
| `WebFetch` | Reading a specific page in full: official blogs, press releases, papers, changelogs |

## Search Tips

- Use company + product names for precision
- Always include the current month/year for recency
- Run company searches in parallel for efficiency
- Search for each distinct item separately
- Use `WebFetch` on the original source before repeating a claim from a secondary article
- Cite the source you actually read, not the one that merely mentioned it

## Using This Skill With the Writing Skills

When the user wants a post about AI news, run this workflow first, then hand the verified findings to `writing-x-posts` or `writing-linkedin-posts`. The writing skills must only use facts that came out of this research.
