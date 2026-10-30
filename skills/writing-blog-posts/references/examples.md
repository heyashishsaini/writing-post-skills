# Examples

These show the shape and tone the skill aims for. Names, numbers and scenarios are illustrations. Never reuse them as facts in a real post.

## Contents

1. Example brief and assumptions line
2. Example outline (tutorial)
3. Example short post (full)
4. Example revision note (draft feedback)
5. Example delivery block

---

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

# How to Add a Skill to a Claude Code Plugin

You have a plugin that works, and now a task keeps coming up that it does not cover. A new skill fixes that without touching the rest. This guide walks through the five steps, from empty folder to a tested skill.

## What you need

A plugin repo with a `skills/` folder and Claude Code installed. This guide assumes a layout where each skill lives in its own folder under `skills/`.

## Step 1: Create the skill folder

Add a folder named after the skill, using lowercase and hyphens.

```bash
mkdir -p skills/writing-blog-posts
```

You should now see the new folder next to your existing skills.

## Step 2: Write SKILL.md

Create `SKILL.md` inside the folder. It starts with a short header containing the skill's `name` and `description`, followed by the instructions.

The description matters most. It is what Claude reads to decide whether to use the skill, so say what the skill does and list the situations that should trigger it, including phrases a user might actually say.

## Step 3: Add references only if you need them

If the skill needs long material, such as templates or checklists, put it in a `references/` folder and point to it from `SKILL.md` with a note on when to read it. Keep the main file short so it loads quickly.

## Step 4: Update your docs and manifest

Add the skill to the README table and, if you keep keywords in your plugin manifest, add the new topic there so people can find it.

## Step 5: Install locally and test

Add your local clone as a marketplace and install the plugin, then ask for something the skill should handle.

```bash
/plugin marketplace add ./your-plugin-repo
/plugin install your-plugin@your-plugin
```

If the skill does not trigger, the usual cause is a description that is too narrow. Add the phrases people really use and try again.

## Next step

Run three real prompts, note where the output disappoints, and tighten the instructions where it went wrong.

---

Why this works: the intro states the problem and the result, each step says what to do and what to expect, there is no padding, and the ending gives a concrete next action. It makes no claim the author could not support.

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
