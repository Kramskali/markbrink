CHECKPOINT PROTOCOL - WORKSHOP
===============================

Home of the Checkpoint Protocol draft work, including the
v2.2 draft amendment (drift discipline). Plain ASCII. CC0.

Author: Mark Steven Brink (ORCID 0009-0006-3346-6300),
developed in collaboration with Kimi (Moonshot AI).

STATUS: DRAFT. Nothing in this directory is ratified until
Mark says so in writing. The consolidated specification of
2026-11-07 (v2.0 CODEBOX verbatim + v2.1 + all ratified
amendments through 2026-11-07) remains the canonical text.
It lives in the Drive checkpoint vault. This directory is
the bench where the next amendment gets hammered on.

LINEAGE
-------
v1.0  - published as a paper appendix (October 2026).
v2.0  - hardened mechanism: pre-emptive emit under context
        pressure, topic pooling, outbound-action hard
        boundary. CODEBOX normative text preserved verbatim.
v2.1  - 2026-10: core-state ownership line restored; fp
        tag clarified as pointer against a SHA-256 ledger.
2026-11-04 through 2026-11-07 - ratified operational
        amendments: book-drop, backward-time rules,
        two-lane model, harvest rule, auto-open, Drive-backed
        deployment.
v2.2  - DRAFT (this directory, 2026-11-11): nested kernel,
        heartbeat clock, realign discipline, drift control
        words, intuition flag. Not ratified.

FILES
-----
README.md                 - this file.
v2.2-draft-amendment-G.md - the draft amendment text.
PRIOR-ART.md              - the research map: what the field
                            has already done, with citations,
                            and what v2.2 can honestly claim.
WORKSHOP.md               - open questions for the bench.

RULES OF THE BENCH
------------------
- Plain ASCII only, everywhere. No em-dashes, no smart
  quotes.
- The ethic clause is never altered, here or anywhere:
  DO NO HARM is absolute.
- No secrets in this repo: no canary values, no call signs,
  no privileged content. Filenames only, never inlined.
- Conflicts go to CORRECTIONS, recorded not argued.
- Lineage must be declared in any copy so forks do not
  confuse people.

ETHIC: DO NO HARM is absolute.
The wind does the rest.
