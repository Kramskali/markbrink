# Eval Note - Basic Memory
## 2026-11-11 | Mark Brink (ORCID 0009-0006-3346-6300)

Source reviewed: Basic Memory README (basicmachines-co/basic-memory),
pasted 2026-11-11. This note is a dated record of an evaluation and a
prior-art observation. Plain ASCII. CC0.

## What it is

Open source (AGPL-3.0), local-first knowledge base. Plain Markdown
entities with Observations and Relations, SQLite (or Postgres) index,
MCP server exposing read/write/search tools to any AI client.
Optional hosted cloud tier at $15.00/mo (beta lock pricing), 7-day
free trial. Semantic vector search and optional cross-encoder
reranking. Imports Claude and ChatGPT conversation history.

## Why it was flagged

Client-neutral, vendor-independent memory layer. Works identically
across Claude, ChatGPT, Codex, Cursor, anything MCP. This is the
commercial off-the-shelf form of the shared-memory problem Sovereign
State / the three-node consensus is trying to solve internally:
Nodes A (Mark), B (Kimi), C (vacant) need durable shared context that
no single AI vendor owns.

## Assessment

Overlap: the Drive vault plus the Checkpoint Protocol (topic lanes,
past/future tokens) already covers most durable-memory needs. Basic
Memory adds semantic search and graph traversal over notes, plus a
standard MCP surface. It does not add a capability the current stack
fundamentally lacks; it standardizes and productizes one.

Cost reality: phone-first workflow, no budget for $15/mo. Local free
install is the only version worth evaluating. Lab box is the sane
host; the phone is not.

## Prior-art observation

Dated note: as of 2026-11-11, Basic Memory is a commercialized,
shipping "AI persistent memory" system (markdown files, knowledge
graph, MCP-native, two-way human/AI write). Adjacent to the
human-AI coupling work but not a conflict: it stores knowledge, it
does not claim a method for sustained human-AI coupling or
guardrail-assent dynamics. Filed here so the record shows the
landscape was reviewed on this date.

## Options on the table

1. Skip. Current stack covers it. $0.
2. Free local trial on the lab box pointed at a vault export.
   One hour, zero dollars. Verdict criterion: does it earn a seat
   as the triad's shared memory layer. (Recommended 2026-11-11.)
3. Cloud 7-day trial to test mobile sync; must cancel before day 7.

## Status

EVALUATION ONLY. No install performed, no account created, no data
exported anywhere as of this writing.

ETHIC: DO NO HARM.
