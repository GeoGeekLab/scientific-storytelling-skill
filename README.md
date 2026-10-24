# Scientific Storytelling

[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](SKILL.md)
[![Type](https://img.shields.io/badge/Agent_Skill-Modular-green.svg)](https://agentskills.io/)

**Good science starts with a good question. A good paper tells a clear story.**

Here's the thing: You can have an important research question, sound methods, and useful results — and still write a paper that's hard to follow.

Why? Because a collection of findings isn't automatically a coherent argument. Your readers need to know what problem you're tackling, why it matters, and how your findings bring them closer to an answer.

That's where **Scientific Storytelling** comes in.

Scientific Storytelling is a modular [Agent Skill](https://agentskills.io/) for planning, drafting, diagnosing, and adapting scientific research narratives. It combines research-article writing methods from the University of Guelph's *Writing in the Sciences* project with **ABT (And–But–Therefore)**, **scientific loglines**, **storyboarding**, and **Known-to-New flow**.

The goal? **Help readers see how the research question, methods, and findings come together.**

> **One question. One clear thread.** Bring the research problem, methods, and results into a coherent narrative. Show readers what the findings reveal and where the research leads next.

---

## ⚡ What Can You Do With It?

Where are you in the writing process? Start there.

| Workflow | When to use it | What it helps you do |
| :--- | :--- | :--- |
| **Plan** | You have a research question and research materials, but no clear manuscript structure. | Analyze journal conventions, map IMRAD sections, develop an ABT and logline, and build a storyboard. |
| **Draft** | You're ready to write or revise a section. | Develop an Introduction, Methods, Results, Discussion, title, or abstract around the available research material. |
| **Diagnose** | The draft contains the right information, but the argument doesn't quite flow. | Audit the ABT, identify AAA/DHY patterns, check Known-to-New transitions, and reverse-outline paragraphs. |
| **Adapt** | You need to explain the same research in another format. | Shape a narrative for a thesis, poster, talk, grant summary, or elevator pitch. |

Choose the workflow that fits your task and build from there.

---

## 📦 Installation

Choose the setup that works for you.

### Option 1: Install With One Prompt

Using **Claude Code** or **Codex** with terminal access? Paste this instruction:

```text
Install the scientific-storytelling Agent Skill from https://github.com/GeoGeekLab/scientific-storytelling-skill globally for this assistant, preserve the complete skill directory, and verify that the skill is discoverable.
```

### Option 2: Use the Skills CLI

Install globally for **both Claude Code and Codex**:

```bash
npx skills add GeoGeekLab/scientific-storytelling-skill -g -a claude-code -a codex -y
```

Or install for just one assistant:

```bash
# Claude Code → ~/.claude/skills/scientific-storytelling/
npx skills add GeoGeekLab/scientific-storytelling-skill -g -a claude-code -y

# Codex → ~/.agents/skills/scientific-storytelling/
npx skills add GeoGeekLab/scientific-storytelling-skill -g -a codex -y
```

These commands use the [Skills CLI](https://github.com/vercel-labs/skills).

### Option 3: Install Manually

Clone or copy the repository into the assistant's user-level skills directory:

- **Claude Code:** `~/.claude/skills/scientific-storytelling/`
- **Codex:** `~/.agents/skills/scientific-storytelling/`

Keep `SKILL.md` at the skill root, alongside `references/`, `assets/`, and `evals/`. The router needs those files to do its job.

---

## 🚀 Quickstart

Not sure where to begin? Try one of these prompts.

**1. Find the argument in an Introduction**

```text
Use scientific-storytelling to identify the ABT, logline, and Known-to-New
flow in this Introduction. Preserve all in-text citations.
```

**2. Turn research material into a manuscript plan**

```text
Use scientific-storytelling to plan a research article from these methods
and results. Build a storyboard for the central argument.
```

**3. Learn how a target journal tells its stories**

```text
Use scientific-storytelling to analyze three articles from [Target Journal]
and extract a section map and paragraph-level patterns.
```

Each prompt starts with a different problem. The skill selects the methods and worksheets that fit the task.

---

## 📚 How Does the Storytelling Work?

Every scientific story starts with a question worth asking. A meaningful research problem gives the narrative direction, and the findings move it toward a conclusion readers can follow.

Scientific Storytelling draws on two complementary frameworks.

### 1. Writing Research Articles

Research-article conventions give the narrative its structure and help readers navigate the study.

The University of Guelph's *Writing Research Articles* module covers seven units: **Getting Started, Introduction, Methods, Results, Discussion, Titles and Abstracts,** and **Revising and Responding to Feedback**.

Use these methods to examine target-journal conventions, organize sections, develop drafts, and respond to feedback. The journal's conventions and the study's findings guide the structure.

### 2. Storytelling in Science Writing

This is where the argument takes shape.

- **ABT (And–But–Therefore)** connects established knowledge (**And**), the unresolved problem (**But**), and the research response or supported conclusion (**Therefore**).
- **Scientific loglines** capture the central research problem and the answer supported by the findings in one focused sentence. No results yet? Mark the answer as pending.
- **Storyboarding** organizes the narrative into Acts and Scenes. Each Scene has a **Point**, while **Known** and **New** show how one idea leads to the next.
- **Known-to-New flow** helps readers connect each new claim to information they've already encountered.

There are two common problems to watch for, too. **AAA** means facts keep accumulating without a clear problem. **DHY** means too many competing problems pull the narrative in different directions. The Diagnose workflow helps you recognize these patterns and sharpen the central argument.

Think of the frameworks as a map. They show you where the argument starts, where it turns, and how the findings bring it together.

---

## 🛠️ How Is the Skill Organized?

Here's the useful part: The skill brings the right writing guidance to each task.

`SKILL.md` acts as a compact router. It reads the request, selects a workflow, and loads only the references or worksheets that the task needs.

```text
       Research material + target format
                      |
                      v
              SKILL.md (router)
                      |
        +-----------+-----------+-----------+
        |           |           |           |
       Plan        Draft     Diagnose      Adapt
        |           |           |           |
        +-----------+-----------+-----------+
                      |
                      v
            On-demand references
               + worksheets
                      |
                      v
               Research narrative
```

**Lean context engineering:** Load the relevant guidance. Keep the research question and findings in focus. Use worksheets when they help structure the output.

### What's in the Repository?

The skill includes **nine reference documents**, **four working worksheets**, and **eight acceptance scenarios** that describe expected agent behavior.

```text
scientific-storytelling-skill/
├── SKILL.md                         # Skill entry point and task router
├── README.md                        # Project guide
├── references/                      # Research-writing methods
│   ├── 01-getting-started.md
│   ├── 02-introduction.md
│   ├── 03-methods.md
│   ├── 04-results.md
│   ├── 05-discussion.md
│   ├── 06-titles-abstracts.md
│   ├── 07-revising-feedback.md
│   ├── 08-storytelling.md
│   └── 09-sources-attribution.md
├── assets/                          # Working worksheets
│   ├── feedback-response-log.md
│   ├── genre-analysis.md
│   ├── research-article-map.md
│   └── storyboard.md
└── evals/                           # Acceptance scenarios
    └── acceptance-cases.md
```

The references provide the writing methods. The worksheets help organize the work. The acceptance scenarios describe expected behavior for cases such as missing results, inconclusive findings, and reviewer feedback.

---

## 📜 Sources & Attribution

Scientific Storytelling is based on the University of Guelph's [*Writing in the Sciences*](https://writinginthesciences.uoguelph.ca/) project:

- **Writing Research Articles** — Jodie Salter and Sarah Gibbons. [Course module](https://writinginthesciences.uoguelph.ca/getting-started/).
- **Storytelling in Science Writing** — Christopher Greyson-Gaito. [Course module](https://writinginthesciences.uoguelph.ca/storytelling-in-science-writing/).

The Markdown worksheets adapt these teaching methods for assistant workflows.

For original sources, method attribution, and licensing details, see [`references/09-sources-attribution.md`](references/09-sources-attribution.md). The university website identifies its main educational content as **CC BY-NC-SA**, with individually marked exceptions. Check the license notice for each source before reusing it.

---

**Start with the question. Follow the science. Help the reader see the story.**
