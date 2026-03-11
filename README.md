# Second Brain for Content Creators

**Turn your daily notes into reusable content assets — automatically.**

A Claude Code skill for writers, content creators, and solo operators who publish consistently.

---

## The Problem

You write every day. Good stuff comes out. Then it disappears.

Three months later you're stuck, and you've forgotten you already solved this problem twice. Your best lines are buried in old files. Your stories aren't connected to your themes. Nothing compounds.

## What This Does

Every time you share a diary entry or piece of writing, Claude:

- Cleans it up with **minimal edits** (your voice stays intact)
- Pulls out **stories, insights, actionable steps, and signature phrases**
- Saves them to **4 searchable asset libraries**
- Generates a **downloadable insight card** in your brand style
- Gives you **coach feedback** — what worked, what to watch

Over time, you build a library of raw material you can pull from anytime.

---

## How It Works

```
You write something
        ↓
Claude cleans it (you review first)
        ↓
Assets extracted → story-bank / insight-bank / action-bank / style-bank
        ↓
Insight card generated (HTML, downloadable)
        ↓
Coach feedback
```

---

## Install

```bash
# Option 1: Global (works in all Claude Code sessions)
mkdir -p ~/.claude/skills/second-brain
curl -o ~/.claude/skills/second-brain/SKILL.md \
  https://raw.githubusercontent.com/lhsyt/second-brain-skill/main/SKILL.md

# Option 2: Project-level
mkdir -p .claude/skills/second-brain
curl -o .claude/skills/second-brain/SKILL.md \
  https://raw.githubusercontent.com/lhsyt/second-brain-skill/main/SKILL.md
```

Then copy `profile-template.md` to your working directory and fill it in.

---

## File Structure After Setup

```
your-project/
├── profile-template.md         ← Fill this in (your writing DNA)
├── 00-inbox/
│   └── insight-cards/          ← Generated HTML cards
├── 03-resources/atoms/
│   ├── story-bank.md
│   ├── insight-bank.md
│   ├── action-bank.md
│   └── style-bank.md
└── sources/                    ← Original archive
```

---

## Trigger Phrases

| Say this | Claude does |
|----------|-------------|
| "This is my diary" | Full 6-step flow |
| "Just titles and article" | Steps 2–3, waits for review |
| "Next step" | Runs Steps 4–6 |
| "Keep the original" | Archive as-is, extract assets |
| "Analyze this" | Analysis only |

---

## Key Principle

> Minimal edits. Your voice stays. The system does the organizing.

Claude does not rewrite your work. It cleans up transcription errors, removes filler words, and preserves your sentence structure. Everything that makes your writing sound like you stays in.

---

## Requirements

- [Claude Code](https://claude.ai/claude-code)
- A working directory with `profile-template.md` filled in

---

## License

MIT

---

*Built by a daily writer who needed this.*
