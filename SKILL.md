---
name: writing-post-skills
description: Entry point for the writing-post-skills plugin, a set of skills for writing X (Twitter) posts, X threads, LinkedIn posts and blog posts. Use this whenever the user asks for a tweet, X post, thread, LinkedIn post, blog post, article, thought-leadership content, or social content about AI, even if they don't name a skill. It routes the request to the right skill inside the skills/ folder and sets the order when more than one is needed.
---

# writing-post-skills

This is the root skill for the plugin. It does not write posts itself. It decides which skill in `skills/` to read and in what order.

## Skills in this plugin

| Skill | Path | Use it for |
|-------|------|-----------|
| `writing-linkedin-posts` | `skills/writing-linkedin-posts/SKILL.md` | Authentic LinkedIn posts: hooks, formats, engagement strategy. |
| `writing-x-posts` | `skills/writing-x-posts/SKILL.md` | X posts and threads. Full Topic / Link / Freeform / Random workflow lives in `skills/writing-x-posts/references/x-content-manager.md`. |
| `writing-blog-posts` | `skills/writing-blog-posts/SKILL.md` | Publish-ready blog posts and long-form articles: tutorials, listicles, opinion, case studies, explainers, comparisons, with title, meta description, slug and SEO structure. |

## Routing

Read the matching SKILL.md **before** writing anything.

1. **Request is for an X post, tweet or thread** → read `writing-x-posts`.
2. **Request is for a LinkedIn post or professional thought-leadership content** → read `writing-linkedin-posts`.
3. **Request is for a blog post, article, long-form piece, newsletter essay, or a blog outline, intro, headline or SEO pass** → read `writing-blog-posts`.
4. **Request is for more than one format** (for example a blog plus a thread, or both social platforms) → read each matching skill and adapt per format. Do not paste the same text into several formats. For blog-to-social repurposing, write the blog first, then adapt it.
5. **Request is unclear about the format** → ask once: X, LinkedIn, or blog?

## Current events and facts

When a post is about AI news, a product launch or any current event:

1. Search the web first and open the official source (company blog, docs, announcement) to confirm the details.
2. Use only facts you verified, and keep the source link.
3. Write the post with `writing-x-posts`, `writing-linkedin-posts` and/or `writing-blog-posts`.

Never add claims, numbers or quotes you could not confirm. If a search finds nothing reliable, say so instead of filling the gap.

For posts that do not depend on current events (opinions, lessons learned, how-tos), skip the search and go straight to the writing skill.

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
│   ├── writing-blog-posts/
│   ├── writing-linkedin-posts/
│   └── writing-x-posts/
├── README.md
└── LICENSE
```
