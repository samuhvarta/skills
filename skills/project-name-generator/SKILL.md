---
name: project-name-generator
description: Generate catchy, short, professional names for a software project, service, library or tool from a short description (language, functionality, workload, workflow, domain). Use when the user asks for a project name, repo name, product name, codename, or help naming something they are building.
model: claude-haiku-5-5
---

# Project Name Generator

Suggest memorable project names from a short description, using the naming techniques below.

## Input

The user gives a short description. Useful signals, any of which may be missing:

- **Language/stack**: Rust, Go, Python, Kubernetes, etc.
- **Functionality**: what it does (index, authorize, ingest, route, monitor...)
- **Workload/workflow**: batch, streaming, request/response, pipeline, orchestration
- **Domain**: fintech, healthcare, telecom, security, data, devtools
- **Tone/constraints** (optional): playful vs. serious, max length, CLI-friendly

If the description is too thin to name anything (no idea what the project does), ask one short clarifying question. Otherwise proceed with sensible assumptions and state them.

## Naming techniques

Work through these. Not every technique fits every project; skip the ones that produce forced results.

### Core techniques
1. **Backcronym**: pick a word first, then expand its letters into a long form that describes the project. Example: TRACED = Telephone Robocall Abuse Criminal Enforcement and Deterrence.
2. **Professional role**: a human role that mirrors what the software does. A one-letter change is allowed. Examples: apostille, factotum, architekt, notary, cartographer, sexton, steward.
3. **Acronym that is a word**: build an acronym from the functional description that spells a real word whose meaning loosely fits. Example: Customer Profile Index Service = CuPiD (cupid, the matchmaker).
4. **Mythological deity**: Norse, Greek, Indian (and other pantheons) where the deity's domain overlaps the project's function. Examples: Athena for a knowledge base, Sanchaar for communication, Heimdall for monitoring, Hermes for messaging.
5. **Civil engineering, architecture or defense term**: Examples: bastion, vanguard, bulwark, keystone, buttress, lintel, yapi (Turkish for facade/structure), citadel, rampart.
6. **Programming-language wordplay**: a pun on the implementation language. Examples: TRusty (Rust auth service), gotel (Go telemetry, "go-tell"), Pythia, Rustle, Swiftly, Gopher-derived names.

### Additional techniques
7. **Portmanteau/blend**: fuse two relevant words, overlapping shared letters where possible. Examples: Pinterest (pin + interest), Instagram (instant + telegram), Hadoop-era names like Sqoop (SQL + Hadoop).
8. **Nature and animal metaphor**: an animal or natural phenomenon whose trait matches the behavior. Examples: Falcon (fast, sharp-eyed monitoring), Mantis (precise strikes), Ant (many small workers), Tide, Moraine, Mycelium (distributed network).
9. **Foreign-language word**: a short word from Latin, Sanskrit, Turkish, Japanese, German, Old Norse, etc. with a fitting meaning. Examples: Sutra (rules/threads), Setu (bridge, Sanskrit), Kaizen (improvement), Tezgah (workbench, Turkish), Wegweiser (signpost, German). Verify meaning and connotation before suggesting.
10. **Verb or action word**: a short imperative that says what the tool does. Examples: Fetch, Sift, Weave, Forge, Relay, Prune, Scout.
11. **Science, math and physics term**: Examples: vector, tensor, flux, entropy, prism, lattice, quanta, vertex, delta.
12. **Navigation, maritime and aviation term**: Examples: helm, keel, sextant, beacon, compass, pylon, ballast, jetty, sonar.
13. **Craft, tool and material**: Examples: anvil, loom, forge, lathe, kiln, rivet, chisel, crucible, mortar.
14. **Astronomy and cartography**: Examples: Polaris, Nebula, Meridian, Atlas, Orrery, Zenith, Isobar.
15. **Mythical place, object or creature** (beyond deities): Examples: Bifrost (bridge between systems), Mjolnir (a heavy-hitting tool), Argus (many eyes, observability), Cerberus (guard), Labyrinth, Ariadne (thread through a maze).
16. **Historical figure or pioneer** relevant to the field. Use sparingly, and only for figures with a clear tie to the function. Examples: Turing, Lovelace, Hopper, Babbage.
17. **Letter play**: drop a vowel, swap a letter, or alter spelling to make the name shorter, more distinctive and more searchable. Examples: Flickr, Tumblr, architekt. Keep it pronounceable.
18. **Sound and onomatopoeia**: a short word that evokes the action or feel. Examples: Ping, Zap, Whirr, Click, Thrum.
19. **Domain pun**: wordplay on the business domain or workflow. Example: a Kafka-based pipeline named "Metamorphosis" or "Trial"; a payments reconciler named "Tally".
20. **Prefix and suffix patterns**: attach a recognizable affix to a root for family feel or brevity: -ly, -ify, -io, -ix, -ora, -ex, micro-, meta-, omni-, re-. Example: Tallyx, Routify.

## Quality filters

Before presenting a candidate, check it:

- **Short**: aim for 4 to 8 characters; 3 to 10 is acceptable. Prefer 1 to 3 syllables.
- **Pronounceable and spellable**: someone hearing it once can type it. Avoid ambiguous spellings.
- **Typeable as a CLI/package name**: lowercase, no spaces, easy on a keyboard.
- **Distinct**: avoid names that are already a famous product in the same space (for example Atlas, Athena, Kafka are heavily used in tech; mention the collision if suggesting them anyway).
- **No bad connotations**: do a quick sanity check for offensive or unfortunate meanings in major languages.
- **Meaningful**: the name should be explainable in one sentence tied to the project's purpose.
- **Professional**: no jokes that age badly or that a team would hesitate to say in front of a customer.

## Availability checks

If tools allow, spot-check the top picks for collisions: GitHub repo search, the relevant package registry (npm, PyPI, crates.io, Go modules), and a domain lookup. Report what was checked and what was not. Never claim a name is "available" without having checked; say "not verified" instead.

## Output format

Present 6 to 10 candidates, mixing techniques. For each:

| Name | Technique | Why it fits |
|------|-----------|-------------|

Then:

1. **Top pick** and a one-line reason.
2. **Runner-ups**: two names, with the case for each.
3. For any backcronym, write out the full expansion.
4. A short note on assumptions made and checks not performed.

Keep the response compact. Do not explain every technique; only name the one used for each candidate. Offer to iterate: more playful, shorter, a different mythology, a specific technique, or names starting with a given letter.

## Example

**Input**: "Authorization service written in Rust for a payments platform."

| Name | Technique | Why it fits |
|------|-----------|-------------|
| TRusty | Language wordplay | Rust + trusty; authorization is about trust |
| Bastion | Defense term | Fortified gatekeeping of access |
| Sentinel | Role/defense | Standing guard over every request |
| Warden | Professional role | Decides who may pass |
| Themis | Greek deity | Goddess of law and order; fits policy decisions |
| Rampart | Defense term | A protective barrier around services |

**Top pick**: TRusty, for its immediate language and purpose signal.
