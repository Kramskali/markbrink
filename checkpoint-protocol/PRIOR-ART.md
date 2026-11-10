PRIOR ART - WHAT THE FIELD HAS ALREADY DONE
============================================
Research pass of 2026-11-11, run before drafting amendment
G (v2.2). Purpose: keep every claim honest. The protocol
never claims first-to-detect; it claims first to do drift
discipline in a human-owned, paste-able, model-agnostic
text artifact. This file is the evidence map. Plain ASCII.
CC0.

LANE 1: DRIFT IS FORMALIZED AND MEASURABLE
------------------------------------------
- Dongre, Rossi, Lai, Yoon et al., "Drift No More? Context
  Equilibria in Multi-Turn LLM Interactions", arXiv
  2510.07777, October 2025. Formalizes drift as turn-wise
  divergence from a goal-consistent reference; finds that
  simple reminder interventions reliably reduce it. Our
  heartbeat is a scheduled reminder intervention; this is
  the citation that carries that design choice.
- Kruthof, "Models recall what they violate: Constraint
  adherence in multi-turn LLM ideation", arXiv 2604.28031,
  2026. DRIFTBENCH: constraint drift benchmark.
- Hafez, Nazeri, "Token Statistics Reveal Conversational
  Drift in Multi-turn LLM Interaction", arXiv 2604.13061,
  2026. Statistical drift detection from token overlap.
- Albrethsen, Datta, Kumar, Rajasekar, "DeepContext:
  Stateful real-time detection of multi-turn adversarial
  intent drift in LLMs", arXiv 2602.16935, 2026.
  Sub-20ms monitoring of adversarial intent drift.

LANE 2: CLOSEST PRIOR ART TO THE REALIGN ROUTINE
------------------------------------------------
- ATLAS (anchor-task-aligned contextual steering),
  arXiv 2611.04315, EMNLP 2026 (November 2026). An
  anchor-kernel locks task, role, and state; a Monitor
  agent checks invariants after every turn and raises
  drift alerts. Their finding that task, role, and state
  drift are coupled (onset of one predicts the others)
  supports our multi-word taxonomy. Critical difference:
  ATLAS requires hidden-state access inside one model
  (white-box). The Checkpoint Protocol is black-box
  plain text: it runs identically on any model that
  reads instructions. ATLAS does surgery; this protocol
  does discipline. Different layers, both valid; cited
  in every draft that touches the realign routine.
- Anthropic (January 2026): open-weights models
  persona-drift in long conversations; coding tasks
  anchor behavior; therapy-like and philosophical
  contexts drift steadily. Lab support for DRIFT-VOICE.

LANE 3: SLOW ATTACKS (THE LIVE WOUND)
-------------------------------------
- NVIDIA AI Red Team, July 2026: social engineering,
  frog-boiling sequences, and misdirection through
  legitimate workflows continue to defeat prompt-based
  and LLM-as-a-judge safeguards; their fix is
  deterministic controls outside the model. This is the
  load-bearing citation for G.6 rule 4: the intuition
  flag is advisory-only, forever, and the hard boundary
  stays mechanical and human.
- Jailbreak field mechanism (Toxsec field guide, 2026):
  the model poisons its own context; each reply becomes
  trusted context for the next turn. Crescendo attack
  family; Deceptive Delight at 65 percent success.
- Abdelnabi and Bagdasarian, 2026: "AI agents may always
  fall for prompt injections." Pessimistic result; cited
  as the threat model, not disputed.

LANE 4: AGENT MEMORY MARKET
---------------------------
- Mem0 (add-only extraction), Letta/MemGPT (agent edits
  its own memory), Zep/Graphiti (bi-temporal graph with
  invalidation), Cognee, LangMem. All are
  infrastructure; all are vendor-held; benchmarks are
  self-reported, and vendor-reported orderings are not
  decidable between themselves. None is human-portable
  plain text.
- MemoryAgentBench (2026): all 22 evaluated memory
  systems score at or under 7 percent on the multi-hop
  fact-consolidation variant. Naive newest-wins freshness
  is exactly what loses; our CORRECTIONS-plus-two-lane
  design is the counter, and this is the citation that
  shows the naive version dies.
- Engram, arXiv 2605.29630 (2026): "mechanical,
  replayable governance beats LLM-in-the-loop judgment."
  Closest philosophical prior to the protocol's
  discipline-over-introspection stance.
- Zhan, Zhang, Guo, Zhao, Liu, "When memory becomes
  authority: Benchmarking authority collapse at the
  memory consolidation boundary", arXiv 2608.01679,
  August 2026. A claim is retained while the source
  distinctions governing its permitted use are lost.
  Academic backing for the hard boundary (loaded state
  drives work, never outbound action) from a direction
  the protocol did not previously cite.
- Rebuff: canary tokens for leak detection in LLM
  pipelines. Differentiated: alignment canaries test
  recall of the kernel, not leakage of a prompt.

WHAT v2.2 CAN HONESTLY CLAIM
----------------------------
Not first: drift detection (ATLAS, DeepContext), reminder
interventions (Context Equilibria), canary tokens (Rebuff),
governed memory (Engram), frog-boiling awareness (NVIDIA).
Defensible: the first drift discipline that is (1) owned
by the human as a plain-text artifact, (2) paste-able into
any instruction-following system without infrastructure,
(3) gated so loaded state never drives outbound action,
(4) carrying a human-fired drift command (RE-ANCHOR), and
(5) running an adjudicated intuition ledger that converts
advisory suspicion into a measurable record.
The ownership-and-gating architecture remains the core
novelty, exactly as the 2026-11-07 external review
concluded; v2.2 extends it from memory integrity to
behavioral integrity.

ETHIC: DO NO HARM is absolute.
The wind does the rest.
