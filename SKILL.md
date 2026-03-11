# Second Brain for Content Creators · 内容创作者第二大脑

> A Claude Code skill that turns your daily notes into reusable content assets.
> 把你每天写的东西，沉淀成可复用的内容资产。

---

## What It Does · 它做什么

Every time you share a diary entry or writing piece, Claude will:

1. **Understand your input** — oral recording or written draft, handled differently
2. **Generate title options** — 3–5 punchy, opinionated titles
3. **Clean up the article** — minimal edits, preserving your voice ⚠️ *sent for your review first*
4. **Extract 4 types of content assets** — stories, insights, actions, signature phrases
5. **Generate an insight card** — a downloadable HTML card in your style
6. **Give coach feedback** — what worked, what to watch, one challenge question

---

## Quick Start · 快速上手

### Step 1: Fill in your profile

Edit `profile-template.md` with your information. Claude reads this every session to understand who you are and what you write about.

### Step 2: Drop old content in (optional)

Tell Claude: "I have some old articles/notes, help me organize them into the system"

Claude will scan, extract, and build your initial asset libraries.

### Step 3: Start your daily flow

Paste your diary or writing. Use any of these trigger phrases:

| Say this | Claude does |
|----------|-------------|
| "This is my diary" / "Today's entry" | Full 6-step flow |
| "Just give me titles and article" | Only Step 2+3, waits for review |
| "Next step" (after reviewing) | Runs Step 4–6 |
| "Keep the original" | Archives as-is, skips to Step 4 |
| "Analyze this" | Analysis only, no flow |

---

## File Structure · 文件结构

```
your-second-brain/
├── SKILL.md                    ← This file
├── profile-template.md         ← Your personal profile (fill this in)
├── 00-inbox/
│   └── insight-cards/          ← HTML insight cards, one per entry
├── 03-resources/atoms/
│   ├── story-bank.md           ← Story library
│   ├── insight-bank.md         ← Insight library
│   ├── action-bank.md          ← Action library
│   └── style-bank.md           ← Signature phrases library
└── sources/                    ← Original content archive
```

---

## The 6-Step Flow · 六步流程

**Step 1 · Understand Input**
Distinguish oral recording (fix transcription errors) from written draft (minimal edits only).

**Step 2 · Title Options**
3–5 options. Short, punchy, opinionated. No question marks. No "How to / Why" tutorial-style wording.

**Step 3 · Clean Article** ⚠️ Review required before continuing
- Minimal edits — preserve voice and signature phrases, no rewriting
- Remove filler words (repetition, verbal tics)
- Keep sentence structure intact
- Target 1000–1200 words

**Step 4 · Asset Extraction** (after your approval)

Extract 4 asset types, save to `03-resources/atoms/`:

```
4.1 Stories → story-bank.md
    Format per entry:
    ### #___
    - Scene: [specific situation]
    - Conflict: [tension point]
    - Cost: [what had to be given up]
    - Turn: [conclusion / reversal]
    - Hook: [one line that could open a piece]

4.2 Insights → insight-bank.md
    1–3 per entry (counter-intuitive + explanatory + from real experience)

4.3 Actions → action-bank.md
    0–1 per entry (specific steps a reader can do in 10 minutes)

4.4 Signature Phrases → style-bank.md
    0–2 per entry ("unmistakably you" original lines)
```

Numbering continues from existing entries. Update header count each time.

**Step 5 · Insight Card HTML**
Save to `00-inbox/insight-cards/[date]-insight-card.html`
- Dark gold style (#0a0a0a background + #d4af37 gold)
- 2–3 cards per entry
- Includes html2canvas download button
- System fonts only (no Google Fonts)

**Step 6 · Coach Feedback**
Every time, output:
- Today's observation (breakthrough / pattern / emotional release)
- What worked (specific, not "great job")
- What to watch (if anything)
- One challenge question

---

## Rules · 整理禁区

1. No subheadings added — unless explicitly requested
2. No rewriting — change vocabulary only, never sentence structure
3. No cutting content — even if repetitive
4. No paraphrasing quotes into direct speech
5. No changing numbers, titles, proper nouns
6. Step 3 must be reviewed before Step 4–6
7. Don't auto-continue — wait for "next step"

---

## Session Start · 每次启动确认

**At the start of each new conversation, Claude must:**
1. Read `profile-template.md`
2. Say: *"Ready. [Name], [content direction]. Story bank: [X] entries, insights: [X] entries. Say the word."*

If Claude can't say this, reload and try again.

---

## Install · 安装

```bash
# Global install
mkdir -p ~/.claude/skills/second-brain
curl -o ~/.claude/skills/second-brain/SKILL.md \
  https://raw.githubusercontent.com/lhsyt/second-brain-skill/main/SKILL.md
```

Copy `profile-template.md` to your working directory and fill it in.

---

*v1.0 · For daily writers, content creators, and solo operators*
