<h1 align="center">writing-post-skills</h1>

<p align="center">
  <a href="LICENSE"><img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-blue.svg"></a>
  <img alt="Claude Code" src="https://img.shields.io/badge/Claude_Code-plugin-D97757?logo=claude&logoColor=white">
  <img alt="OpenAI Codex" src="https://img.shields.io/badge/OpenAI_Codex-compatible-412991?logo=openai&logoColor=white">
  <img alt="X" src="https://img.shields.io/badge/X-posts_%26_threads-000000?logo=x&logoColor=white">
  <img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-posts-0A66C2?logo=linkedin&logoColor=white">
</p>

A plugin for writing **X (Twitter)** and **LinkedIn** posts, grounded in verified AI news. One plugin, three skills. Built for **Claude Code** and also usable with **Codex/ChatGPT**, since both read the open `SKILL.md` format.

## Works with

| Tool | Support | How |
|------|---------|-----|
| ![Claude](https://img.shields.io/badge/Claude_Code-D97757?logo=claude&logoColor=white) | Native plugin | Plugin marketplace (see below) |
| ![Codex](https://img.shields.io/badge/OpenAI_Codex-412991?logo=openai&logoColor=white) | Skills | Copy skills into a Codex skills folder |
| ![Claude.ai](https://img.shields.io/badge/Claude.ai-D97757?logo=claude&logoColor=white) | Skills | Upload a skill folder as a ZIP |

## Skills

| | Skill | What it does |
|---|-------|--------------|
| 🔎 | **`researching-ai-news`** | Compiles current, source-linked AI news using the built-in web search and fetch tools. No search MCP needed. |
| 💼 | **`writing-linkedin-posts`** | Writes authentic LinkedIn posts: hooks, formats, and engagement strategy. |
| 🐦 | **`writing-x-posts`** | Writes X posts and threads. Full Topic / Link / Freeform / Random workflow in `references/x-content-manager.md`. |

### How they work together

For posts about AI news, `researching-ai-news` runs first and the writing skills use only the facts it verified.

```
researching-ai-news ──┬──► writing-x-posts
                      └──► writing-linkedin-posts
```

## Install

### Claude Code

```bash
/plugin marketplace add heyashishsaini/writing-post-skills
/plugin install writing-post-skills@writing-post-skills
```

Local testing from a clone:

```bash
git clone https://github.com/heyashishsaini/writing-post-skills.git
/plugin marketplace add ./writing-post-skills
/plugin install writing-post-skills@writing-post-skills
```

### OpenAI Codex

Codex discovers skills from `.agents/skills` folders. Copy the three skill folders there:

```bash
git clone https://github.com/heyashishsaini/writing-post-skills.git

# For all your projects
mkdir -p ~/.agents/skills
cp -r writing-post-skills/skills/* ~/.agents/skills/

# Or for one repo only
mkdir -p .agents/skills
cp -r writing-post-skills/skills/* .agents/skills/
```

Or use the community `skills` CLI, which routes skills to the right agent folders:

```bash
npx skills add heyashishsaini/writing-post-skills -a codex -a claude-code
```

### Claude.ai

Zip one skill folder (for example `skills/writing-x-posts/`) and upload it under Settings, Skills.

## Usage

Just ask in plain language. The right skill triggers automatically.

| Platform | Example prompts |
|----------|-----------------|
| ![X](https://img.shields.io/badge/X-000000?logo=x&logoColor=white) | "Write a tweet about the latest Anthropic announcement" · "Turn this link into a thread" · "Give me a random tweet for today" |
| ![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?logo=linkedin&logoColor=white) | "Write a LinkedIn post about what I learned shipping my first skill" · "Make this draft less salesy" |
| 🔎 News | "What's new in AI this week?" · "Latest updates from OpenAI and Google" |

## Repository structure

```
writing-post-skills/
├── .claude-plugin/
│   ├── plugin.json
│   └── marketplace.json
├── assets/
│   └── banner.svg
├── skills/
│   ├── researching-ai-news/
│   ├── writing-linkedin-posts/
│   └── writing-x-posts/
├── docs/
├── SKILL.md
├── README.md
└── LICENSE
```

## Contributing

Issues and pull requests are welcome. If you add or change a skill, keep its `SKILL.md` description specific about when it should trigger.

## License

[MIT](LICENSE) © heyashishsaini
