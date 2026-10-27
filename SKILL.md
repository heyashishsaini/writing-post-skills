---
name: writing-post-skills
description: Entry point for the writing-post-skills plugin, a set of skills for writing X (Twitter) posts, X threads and LinkedIn posts, and for researching current AI news to ground them. Use this whenever the user asks for a tweet, X post, thread, LinkedIn post, thought-leadership content, social content about AI, or "latest AI news", even if they don't name a skill. It routes the request to the right skill inside the skills/ folder and sets the order when more than one is needed.
---

# writing-post-skills

This is the root skill for the plugin. It does not write posts itself. It decides which skill in `skills/` to read and in what order.

## Skills in this plugin

| Skill | Path | Use it for |
|-------|------|-----------|
| `researching-ai-news` | `skills/researching-ai-news/SKILL.md` | Finding current, source-linked AI news with web search and fetch. No search MCP needed. |
| `writing-linkedin-posts` | `skills/writing-linkedin-posts/SKILL.md` | Authentic LinkedIn posts: hooks, formats, engagement strategy. |
| `writing-x-posts` | `skills/writing-x-posts/SKILL.md` | X posts and threads. Full Topic / Link / Freeform / Random workflow lives in `skills/writing-x-posts/references/x-content-manager.md`. |

## Routing

Read the matching SKILL.md **before** writing anything.

1. **Request is about AI news, announcements or "what's new in AI"** → read `researching-ai-news`.
2. **Request is for an X post, tweet or thread** → read `writing-x-posts`.
3. **Request is for a LinkedIn post or professional thought-leadership content** → read `writing-linkedin-posts`.
4. **Request is for both platforms** → read both writing skills and adapt the post per platform. Do not paste the same text into both.
5. **Request is unclear about the platform** → ask once: X or LinkedIn?

## Combining skills

When the post is about AI news or any current event:

1. Run `researching-ai-news` first.
2. Pass only the facts it verified (with their sources) to the writing skill.
3. Write the post with `writing-x-posts` and/or `writing-linkedin-posts`.

Never add claims, numbers or quotes the research step did not confirm. If research finds nothing reliable, say so instead of filling the gap.

For posts that do not depend on current events (opinions, lessons learned, how-tos), skip research and go straight to the writing skill.

## Ground rules

- Follow the platform skill's own format, length and style guidance. This file only routes.
- Keep references one level deep: load files in a skill's `references/` folder only when that skill points to them.
- Match the user's voice and topic. Offer a short draft first, then iterate.
- Cite or link sources for news-based claims.

## Folder layout

```
writing-post-skills/
├── .claude-plugin/
│   ├── plugin.json
│   └── marketplace.json
├── SKILL.md                      ← this file
├── skills/
│   ├── researching-ai-news/
│   ├── writing-linkedin-posts/
│   └── writing-x-posts/
├── README.md
└── LICENSE
```
