---
name: tech-writer
description: 'Write explanations and documents in ASD-STE100 Simplified Technical English, with Mermaid diagrams, as Markdown (or HTML on request). Use when the user asks to explain a concept, write a document, doc, guide, README, or explainer, or says "STE", "simplified English", or "tech-writer".'
argument-hint: "Topic to explain or document to write"
---

# Tech Writer

Produce writing that a reader can parse fast: controlled prose based on ASD-STE100. The user chooses how closely to follow the specification (see [Conformance level](#conformance-level)). Each document also gets diagrams.

The default output format is Markdown. HTML is an alternative that the user must choose.

For a short answer in chat (no document), apply steps 3 and 4 only. Use "optimize for brevity" without a question. Diagrams and the format question apply to documents only.

## Style

These rules apply in all conformance levels.

- Write direct statements. Do not use metaphor, analogy, or figurative language in place of a plain statement. Write "The cache stores the result", not "The cache is a memory bank for answers".
- Do not use flourish: no dramatic openers, no rhetorical questions, no filler like "it is worth noting".
- Do not use em dashes. Use a period, a comma, or parentheses.
- Use few superlatives ("best", "fastest", "most powerful", "very"). Use one only when the source gives evidence for it. Give a number or a fact in its place.

## Procedure

1. **Ask the questions.** Before you write a document, ask the user two questions in one turn. Use the ask-questions tool if it is available.
   - Format: "Markdown (default) or an interactive HTML page?"
   - Conformance: "How strict must the ASD-STE100 conformance be?" Give two options: "Strict conformance" or "Optimize for brevity".

   Done when the user answers both.
2. **Find the content.** Read the source material (code, docs, the conversation). Make a list of the facts the reader must know. Done when each section in the plan has its facts.
3. **Write the prose.** Apply the [Style](#style) rules and the rules for the chosen level in [STE rules](./references/ste-rules.md). Done when each sentence passes the checklist for that level.
4. **Add diagrams.** Add a minimum of one Mermaid diagram to each document. Add one diagram for each process, flow, structure, or state model in the content. See [Diagrams](#diagrams). Done when each diagram parses.
5. **Assemble the output.** See [Output formats](#output-formats). Done when the file exists and you have read it back.
6. **Review.** Read the full output one time against the checklist for the chosen level and the Style rules. Correct each sentence that fails.

## Conformance level

| Level                | What to do                                                                                                                              |
| -------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| Strict conformance   | Apply as much of the ASD-STE100 specification as possible. Treat the soft rules as hard rules. Do not combine sentences to save space. |
| Optimize for brevity | Apply the hard rules and the soft rules where natural. Combine short sentences that carry sparse ideas into one sentence.              |

Example for "optimize for brevity":

- Before: "ABC is a new product. ABC is hosted on the XYZ platform."
- After: "ABC is a new product hosted on the XYZ platform."

The full rules for each level are in [STE rules](./references/ste-rules.md).

## Diagrams

- Write diagrams as fenced ` ```mermaid ` blocks in the Markdown source.
- Select the diagram type that matches the content:

  | Content                     | Mermaid type                  |
  | --------------------------- | ----------------------------- |
  | Steps, decisions            | `flowchart`                   |
  | Messages between components | `sequenceDiagram`             |
  | Lifecycle, modes            | `stateDiagram-v2`             |
  | Data model                  | `erDiagram` or `classDiagram` |
  | Schedule, phases            | `gantt` or `timeline`         |
  | Hierarchy, concepts         | `mindmap`                     |

- Write node labels in STE: short nouns and approved verbs.
- Put one sentence of STE prose before each diagram. This sentence tells the reader what the diagram shows.
- In `sequenceDiagram` labels, a semicolon ends the statement. Use a comma or `#59;` for a literal semicolon.

## Output formats

**Markdown (default)**

- Write a `.md` file. Use headings, numbered lists for procedures, and tables for comparisons.
- Put the Mermaid source in fenced blocks so the reader can see and edit it.

**HTML (only when the user selects it)**

- Write one self-contained `.html` file. Load Mermaid from a CDN and render each diagram in a `<pre class="mermaid">` element.
- Apply the same STE rules to all visible text.
- Make the page interactive where this helps the reader understand: collapsible sections, step-through animations, tabs, hover details.
- Keep all content in the page. Do not load data from other sources.
