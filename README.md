# Scientific Storytelling

**Give your research a narrative spine.**

A modular [Agent Skill](https://agentskills.io/) for planning, drafting, diagnosing, and revising scientific research articles. Built from the University of Guelph's *Writing in the Sciences* modules, it connects research-article conventions with **ABT**, **loglines**, and **storyboarding**.

Research provides the evidence. Narrative design makes the argument navigable. Think of it as a dependency graph for a scientific paper—one that readers can follow without a debugger.

**Version:** `1.0.0` · **Entry point:** [`SKILL.md`](SKILL.md)

## What it does

| Workflow | Goal | Methods |
| --- | --- | --- |
| **Plan** | Turn a research question and evidence into a manuscript plan. | Journal genre analysis, IMRAD mapping, ABT, logline, storyboard |
| **Draft** | Develop a focused research-article section. | Introduction, Methods, Results, Discussion, title, abstract |
| **Diagnose** | Trace the argument through an existing draft. | ABT audit, AAA/DHY patterns, Known-to-New, reverse outlining |
| **Adapt** | Shape a research narrative for another format. | Theses, posters, presentations, grant summaries, elevator pitches |

Research-stage awareness keeps the narrative synchronized with the available evidence—from a planned study to analyzed results.

## Install

### One-prompt install

Paste this into **Claude Code** or **Codex** with terminal access:

```text
Install the scientific-storytelling Agent Skill from https://github.com/GeoGeekLab/scientific-storytelling-skill-skill globally for this assistant, preserve the complete skill directory, and verify that the skill is discoverable.
```

### One-command install

Install globally for **both Claude Code and Codex**:

```bash
npx skills add GeoGeekLab/scientific-storytelling-skill -g -a claude-code -a codex -y
```

Or target one assistant:

| Assistant | Command | User-level directory |
| --- | --- | --- |
| **Claude Code** | `npx skills add GeoGeekLab/scientific-storytelling-skill -g -a claude-code -y` | `~/.claude/skills/scientific-storytelling/` |
| **Codex** | `npx skills add GeoGeekLab/scientific-storytelling-skill -g -a codex -y` | `~/.agents/skills/scientific-storytelling/` |

The commands use the [Skills CLI](https://github.com/vercel-labs/skills). Keep `SKILL.md`, `references/`, `assets/`, and `evals/` in the installed folder.

### Manual install

Clone or copy this repository into the assistant's user-level skill directory shown above. The `scientific-storytelling/` directory must contain `SKILL.md` at its root.

## Try it

**Map an argument**

```text
Use scientific-storytelling to identify the ABT, logline, and
Known-to-New flow in this Introduction. Preserve the citations.
```

**Design a paper**

```text
Use scientific-storytelling to plan a research article from these
methods and results. Build a storyboard for the central argument.
```

**Learn a journal's conventions**

```text
Use scientific-storytelling to analyze three research articles
from my target journal and build a section map.
```

## How it works

```text
Research material + target format
              |
              v
         SKILL.md
              |
       +------+------+------+
       |      |      |      |
      Plan   Draft Diagnose Adapt
       |      |      |      |
       +------+------+------+
              |
              v
   Relevant reference + worksheet
              |
              v
       Research narrative
```

The entry point routes the task. References load on demand. Worksheets capture the output. Context stays lean; the evidence gets the bandwidth.

## Repository map

```text
scientific-storytelling-skill/
├── SKILL.md
├── README.md
├── references/
│   ├── 01-getting-started.md
│   ├── 02-introduction.md
│   ├── 03-methods.md
│   ├── 04-results.md
│   ├── 05-discussion.md
│   ├── 06-titles-abstracts.md
│   ├── 07-revising-feedback.md
│   ├── 08-storytelling.md
│   └── 09-sources-attribution.md
├── assets/
│   ├── feedback-response-log.md
│   ├── genre-analysis.md
│   ├── research-article-map.md
│   └── storyboard.md
└── evals/
    └── acceptance-cases.md
```

## The two modules

### Writing Research Articles

Seven units: Getting Started, Introduction, Methods, Results, Discussion, Titles and Abstracts, and Revising and Responding to Feedback. Use these to analyze journal conventions, structure articles, draft sections, and plan revisions.

### Storytelling in Science Writing

Three techniques work together:

- **ABT (And–But–Therefore)** establishes the narrative spine.
- **Logline** captures the central question and supported answer.
- **Storyboarding** organizes Acts, Scenes, Point, Known, and New.

Each technique has a job. The manuscript gains a clear route from question to evidence to conclusion.

## Sources and attribution

Based on the University of Guelph's [Writing in the Sciences](https://writinginthesciences.uoguelph.ca/) project:

- **Writing Research Articles** — Jodie Salter and Sarah Gibbons. [Course module](https://writinginthesciences.uoguelph.ca/getting-started/).
- **Storytelling in Science Writing** — Christopher Greyson-Gaito. [Course module](https://writinginthesciences.uoguelph.ca/storytelling-in-science-writing/).

See [`references/09-sources-attribution.md`](references/09-sources-attribution.md) for source links, method attribution, and licensing details. The course website identifies its main educational content as **CC BY-NC-SA**, with individually marked exceptions.