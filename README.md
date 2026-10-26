# writing-post-skills

A Claude Code plugin for writing X (Twitter) and LinkedIn posts. One plugin, three skills:

| Skill | What it does |
|-------|--------------|
| `researching-ai-news` | Compiles current, source-linked AI news using Claude's built-in web search and fetch tools (no search MCP needed) |
| `writing-linkedin-posts` | Writes authentic LinkedIn posts: hooks, formats, engagement strategy |
| `writing-x-posts` | Writes X posts and threads; full Topic / Link / Freeform / Random workflow in `references/x-content-manager.md` |

## Install

```
/plugin marketplace add heyashishsaini/writing-post-skills
/plugin install writing-post-skills@writing-post-skills
```

Local testing from a clone:

```
/plugin marketplace add ./writing-post-skills
/plugin install writing-post-skills@writing-post-skills
```

## Structure

```
writing-post-skills/
├── .claude-plugin/
│   ├── plugin.json
│   └── marketplace.json
├── skills/
│   ├── researching-ai-news/
│   ├── writing-linkedin-posts/
│   └── writing-x-posts/
├── README.md
└── LICENSE
```

## How the skills work together

For posts about AI news, `researching-ai-news` runs first and the writing skills use only the facts it verified.
