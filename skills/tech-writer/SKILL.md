---
name: tech-writer
description: 'Write explanations and documents in ASD-STE100 Simplified Technical English, with Mermaid diagrams, as Markdown (or HTML on request). Use when the user asks to explain a concept, write a document, doc, guide, README, or explainer, or says "STE", "simplified English", or "tech-writer".'
argument-hint: "Topic to explain or document to write"
---

# Tech Writer

Produce writing that a reader can parse fast: controlled prose about 80% of the way to ASD-STE100. Each document also gets diagrams. The default output format is Markdown. HTML is an alternative that the user must choose.

For a short answer in chat (no document), apply only step 3. Diagrams and the format question apply to documents only.

## Procedure

1. **Ask the format.** Before you write a document, ask the user: "Markdown (default) or an interactive HTML page?" Use the ask-questions tool if it is available. Done when the user chooses a format.
2. **Find the content.** Read the source material (code, docs, the conversation). Make a list of the facts the reader must know. Done when each section in the plan has its facts.
3. **Write the prose in softened ASD-STE100.** Apply the hard and soft rules in [STE rules](./references/ste-rules.md). Done when each sentence passes the hard checklist in that file.
4. **Add diagrams.** Add a minimum of one Mermaid diagram to each document. Add one diagram for each process, flow, structure, or state model in the content. See [Diagrams](#diagrams). Done when each diagram parses.
5. **Assemble the output.** See [Output formats](#output-formats). Done when the file exists and you have read it back.
6. **Review.** Read the full output one time against the STE checklist. Correct each sentence that fails.

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
