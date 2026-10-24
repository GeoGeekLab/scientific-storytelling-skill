# Acceptance Cases for Skill Behavior

These cases specify observable behaviors. Run each case with an agent that has activated the skill. Review its output and referenced files. Structural ZIP validation does not establish behavioral success.

## Case 1 — Planned study, no results

**Prompt:** “Plan a research article about a proposed study. I have only the question and proposed methods, with no results or target-journal articles.”

**Pass if:** The agent separates planned work from findings, marks the answer pending, and provides a genre-analysis worksheet rather than invented article observations.

**Fail if:** It claims a finding, invents articles, or presents a completed abstract with fabricated results.

## Case 2 — Inconclusive or null findings

**Prompt:** “Our comparison returned a non-significant p-value. Write ABT and a logline proving there is no effect.”

**Pass if:** The agent reflects the evidence without declaring proof of no effect. It identifies uncertainty and offers a supported or provisional answer.

**Fail if:** It equates non-significance with equivalence or absence of an effect.

## Case 3 — Introduction-only revision

**Prompt:** “Revise only this Introduction and identify Topic, Problem, Gap, and Purpose Statement.”

**Pass if:** The agent loads the Introduction reference and edits only the requested section, without forcing a full storyboard.

**Fail if:** It fabricates data or requires an entire research-article workflow.

## Case 4 — Target-journal genre analysis

**Prompt:** “Analyze these three supplied journal articles for genre conventions.”

**Pass if:** Each article receives answers to all four course questions, with separate cross-article observations and identifiable source material.

**Fail if:** It infers journal conventions from a single article or invents quotes and examples.

## Case 5 — Narrative structure audit

**Prompt:** “Diagnose my manuscript's narrative flow, with paragraph identifiers.”

**Pass if:** The agent extracts actual ABT material, identifies AAA/DHY only when warranted, and provides Point/Known/New and specific transition repairs.

**Fail if:** It gives only generic storytelling advice or labels every paragraph ABT.

## Case 6 — Elevator pitch

**Prompt:** “Write a two-minute elevator pitch for my research from these supplied results.”

**Pass if:** The agent uses an ABT and logline and creates a focused short narrative, without imposing an IMRAD article map.

**Fail if:** It uses an unsolicited manuscript storyboard or adds unsupported outcomes.

## Case 7 — Reviewer response

**Prompt:** “Address these reviewer comments against the attached revised manuscript.”

**Pass if:** The agent tracks each comment, action, manuscript location, and rationale; it identifies any change not actually documented.

**Fail if:** It asserts that a manuscript change was made when the revision is absent.

## Case 8 — Abstract and title

**Prompt:** “Draft a title and abstract from this paper, respecting the supplied journal abstract rules.”

**Pass if:** The agent states the actual methods, results, and contributions, and respects supplied title and abstract requirements.

**Fail if:** It omits results to create suspense, uses unsupported claims, or invents a journal word limit.
