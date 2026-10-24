# Scientific Storytelling

> **Give your research a narrative spine.**

[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](SKILL.md)
[![Type](https://img.shields.io/badge/Agent_Skill-Modular-green.svg)](https://agentskills.io/)

A modular [Agent Skill](https://agentskills.io/) for planning, drafting, diagnosing, and revising scientific research articles. Built from the University of Guelph's *Writing in the Sciences* modules, it brings together research-article conventions, **ABT (And–But–Therefore)**, **loglines**, and **storyboarding**.

> *Research provides the evidence. Narrative design makes the argument navigable.*
>
> **Think of it as a dependency graph for a scientific paper—one readers can follow without a debugger.**

---

## ⚡ What It Does

| Workflow | Goal | Methods |
| :--- | :--- | :--- |
| **Plan** | Turn a research question and available evidence into a manuscript plan. | Journal genre analysis, IMRAD mapping, ABT, logline, storyboard |
| **Draft** | Develop a focused research-article section. | Introduction, Methods, Results, Discussion, title, abstract |
| **Diagnose** | Trace the argument through an existing draft. | ABT audit, AAA/DHY patterns, Known-to-New flow, reverse outlining |
| **Adapt** | Shape a research narrative for other formats. | Theses, posters, presentations, grant summaries, elevator pitches |

Research-stage awareness keeps the narrative aligned with available evidence, from experimental design through analyzed results.

---

## 📦 Installation

### Option 1: One-Prompt Install

Paste into **Claude Code** or **Codex** with terminal access:

```text
Install the scientific-storytelling Agent Skill from https://github.com/GeoGeekLab/scientific-storytelling-skill globally for this assistant, preserve the complete skill directory, and verify that the skill is discoverable.
```

### Option 2: Skills CLI

Install globally for **Claude Code and Codex**:

```bash
npx skills add GeoGeekLab/scientific-storytelling-skill -g -a claude-code -a codex -y
```

Install for one assistant:

```bash
# Claude Code → ~/.claude/skills/scientific-storytelling/
npx skills add GeoGeekLab/scientific-storytelling-skill -g -a claude-code -y

# Codex → ~/.agents/skills/scientific-storytelling/
npx skills add GeoGeekLab/scientific-storytelling-skill -g -a codex -y
```

The commands use the [Skills CLI](https://github.com/vercel-labs/skills).

### Option 3: Manual Install

Clone or copy the repository into the assistant's user-level skills directory:

- **Claude Code:** `~/.claude/skills/scientific-storytelling/`
- **Codex:** `~/.agents/skills/scientific-storytelling/`

Keep `SKILL.md` at the skill root, alongside `references/`, `assets/`, and `evals/`.

---

## 🚀 Quickstart

**1. Map an argument**

```text
Use scientific-storytelling to identify the ABT, logline, and Known-to-New
flow in this Introduction. Preserve all in-text citations.
```

**2. Design a manuscript**

```text
Use scientific-storytelling to plan a research article from these methods
and results. Build a storyboard for the central argument.
```

**3. Reverse-engineer journal conventions**

```text
Use scientific-storytelling to analyze three articles from [Target Journal]
and extract a section map and paragraph-level patterns.
```

---

## 🛠️ System Architecture

```text
      Research material + target format
                     |
                     v
             SKILL.md (router)
                     |
          +----------+----------+
          |          |          |
       Plan/Draft  Diagnose    Adapt
          |          |          |
          +----------+----------+
                     |
                     v
         On-demand references
              + worksheets
                     |
                     v
           Research narrative
```

**Lean context engineering:** `SKILL.md` routes the task. Supporting references load on demand. Worksheets give the output a structure. Evidence gets the bandwidth.

---

## 📂 Repository Topology

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
├── assets/                          # Working templates
│   ├── feedback-response-log.md
│   ├── genre-analysis.md
│   ├── research-article-map.md
│   └── storyboard.md
└── evals/                           # Acceptance scenarios
    └── acceptance-cases.md
```

---

## 📚 Core Frameworks

### 1. Writing Research Articles

Seven units: *Getting Started, Introduction, Methods, Results, Discussion, Titles and Abstracts,* and *Revising and Responding to Feedback*.

Analyze target-journal conventions, map article sections, develop drafts, and plan revisions.

### 2. Storytelling in Science Writing

Three techniques form the narrative architecture:

- **ABT (And–But–Therefore):** Connect established knowledge, the central problem, and the research response.
- **Logline:** Capture the central question and its evidence-backed answer.
- **Storyboarding:** Organize Acts, Scenes, Point, Known, and New into a readable sequence.

From question to evidence to conclusion: one argument, a clear route.

---

## 📜 Sources & Attribution

Based on the University of Guelph's [*Writing in the Sciences*](https://writinginthesciences.uoguelph.ca/) project:

- **Writing Research Articles** — Jodie Salter and Sarah Gibbons. [Course module](https://writinginthesciences.uoguelph.ca/getting-started/).
- **Storytelling in Science Writing** — Christopher Greyson-Gaito. [Course module](https://writinginthesciences.uoguelph.ca/storytelling-in-science-writing/).

See [`references/09-sources-attribution.md`](references/09-sources-attribution.md) for source links, method attribution, and licensing details. The source website identifies its main educational content as **CC BY-NC-SA**, with individually marked exceptions.
