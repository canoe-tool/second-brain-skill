# 内容创作者第二大脑 · Second Brain for Content Creators

**把你每天写的东西，自动沉淀成可复用的内容资产。**

一个跑在 Claude Code 上的技能包，适合日更写作者、内容创作者、独立创业者。

---

## 为什么要做这个

### 问题：内容创作者的"漏桶"困境

你每天都在写。写出来不少好东西。然后它消失了。

三个月后你卡住了，你忘了自己已经解决过这个问题。最好的金句埋在旧文件里。故事散落在各处，没有被归类。同一个洞见你重新发现了三次，但每次都觉得是第一次。

这不是懒，是系统缺失。**内容不会自己复利，除非有人（或某样东西）帮你把它整理成可以复用的原材料。**

### 根本原因：两件事被混在一起了

写作有两件事：**生产** 和 **整理**。

大多数人把它们混在一起——边写边整理，或者写完之后太累不想整理。结果两件事都没做好。

这个系统把它们分开：你只管写，Claude 负责整理。

---

## 设计原则

### 原则一：最小改动，保留原声

AI 整理文章最常见的错误是"帮你写得更好"——结果文章变流畅了，但读起来不像你了。

这个系统的核心约束是：**只改口头语重复和语音识别错误，句式结构一律不动。**

为什么？因为你的写作风格本身就是资产。让你的文章读起来像你，比让它读起来"更好"更重要。

### 原则二：先审核，再存档

整理完的文章必须发给你确认，你同意之后才会存档、提取资产。

为什么？因为 Claude 可能误判你的意图，改掉了某个关键表达。**你是唯一有权判断"这还是我"的人。**

### 原则三：资产分层提取

一篇文章里有不同类型的价值，混在一起存没用，要拆开来放：

| 资产类型 | 是什么 | 为什么单独存 |
|---------|--------|------------|
| 故事库 | 有场景、冲突、转折的具体经历 | 故事可以跨文章复用，作为开头或论据 |
| 洞见库 | 反直觉、有解释力、来自真实经历的判断 | 洞见是内容的核心，也是你的认知资产 |
| 动作库 | 读者 10 分钟内能做的具体步骤 | 动作类内容转化率高，单独存方便调用 |
| 风格表达库 | "一看就是你写的"标志性原句 | 保存你的语言指纹，帮你找回自己的腔调 |

### 原则四：每篇都有教练反馈

不只是整理，还要复盘。

每次处理完，Claude 会输出：做得好的地方（具体的，不是"你很棒"）、值得留意的地方、一个挑战问题。

为什么？因为写作能力是可以训练的，但你需要一个不说废话的观察者。

### 原则五：积累才有价值

单次使用这个系统没太大意义。它的价值在复利——**用得越久，资产库越厚，你越容易找到原材料，写作越快越好。**

这就是为什么它叫"第二大脑"：不是替代你，是把你的经历和思考变成可以检索、可以组合的库存。

---

## 它做什么

每次你发来一篇日记或文章，Claude 会：

1. 理解输入（区分口述 vs 手写，处理方式不同）
2. 生成 3–5 个标题备选
3. 整理文章（最小改动）→ **发你审核**
4. 审核通过后，提取 4 类资产存入对应的库
5. 生成洞见卡片（HTML，可下载）
6. 给教练反馈

---

## 安装

```bash
# 全局安装（所有 Claude Code 会话都可用）
mkdir -p ~/.claude/skills/second-brain
curl -o ~/.claude/skills/second-brain/SKILL.md \
  https://raw.githubusercontent.com/lhsyt/second-brain-skill/main/SKILL.md
```

安装后，把 `profile-template.md` 复制到你的工作目录，填写你的个人信息。

---

## 文件结构

```
你的项目/
├── profile-template.md         ← 填你的信息（写作 DNA）
├── 00-inbox/
│   └── insight-cards/          ← 生成的 HTML 洞见卡片
├── 03-resources/atoms/
│   ├── story-bank.md           ← 故事库
│   ├── insight-bank.md         ← 洞见库
│   ├── action-bank.md          ← 动作库
│   └── style-bank.md           ← 风格表达库
└── sources/                    ← 原始内容存档
```

---

## 触发词

| 你说 | Claude 执行 |
|------|------------|
| 「这是我的日记」/ 「今天的文章」 | 完整 6 步流程 |
| 「只要标题和文章」 | 只做整理，等你审核 |
| 「下一步」（审核后） | 执行资产提取 + 卡片 + 反馈 |
| 「按原文记录」 | 原文存档，直接提取资产 |
| 「分析一下」 | 只分析，不走流程 |

---

## 使用要求

- [Claude Code](https://claude.ai/claude-code)（Claude 官方 CLI 工具）
- 工作目录里有填好的 `profile-template.md`

---

## License · 许可

MIT — 随意使用、fork、基于它做自己的版本。

---

*一个日更 400+ 天的创作者做的，因为自己需要它。*

---

## English Summary

A Claude Code skill that processes your daily writing and extracts reusable content assets (stories, insights, actions, signature phrases). Core principle: minimal edits — your voice stays intact, Claude only organizes. Article review required before archiving. Generates downloadable insight cards. Gives coach feedback every session.

The system is designed around one idea: writing ability compounds when you have organized raw material to draw from. The longer you use it, the more useful it gets.

Install: `curl -o ~/.claude/skills/second-brain/SKILL.md https://raw.githubusercontent.com/lhsyt/second-brain-skill/main/SKILL.md`
