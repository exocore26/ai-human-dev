# META-SYSTEM

## What it is, in one paragraph

The META-SYSTEM is a governed software factory. A non-technical user
describes what they want to build, and the system guides them through a
structured project lifecycle — problem statement, analysis, design,
implementation, testing, documentation, artifact — with AI assistance
that stays on task because the guardrails are built into the tool, not
bolted on. It runs entirely on free AI tiers and a 4 GB laptop. It is
built so that the AI cannot drift, hallucinate, or lose alignment
without the system catching it, recording it, and handing it to a human.

## Why it matters

AI can generate code. What it cannot reliably do is *stay on task* across
a multi-phase project. It drifts, invents, truncates, and loses the
thread — and today the person using it has to manage all of that
themselves. That management is the actual cost of AI-assisted
development, and it is what stops non-technical people from building
real software with AI.

The META-SYSTEM moves that cost. The AI's failures are handled by the
system's architecture — contracts, checkpoints, validation, repair,
human fallback — so the person building the software never has to think
about them. That is the novelty: **not better AI, but a better envelope
around the AI**, so the AI's unreliability stops being the user's
problem.

## Why it's credible

It is built, not proposed. The current working system includes:

- a deterministic console (Turbo Pascal, DOS) that governs the AI
  backends and holds the state;
- a binary bridge that passes work to a Python worker and returns
  results safely;
- three working AI backends (Gemini, Groq, Manus) with automatic
  validation and cross-backend repair of structured output;
- a telemetry/archiver layer that records every file placed, every
  request and response, and every human fallback;
- a year of prior experimental work, publicly visible on YouTube
  (@AI-HUMAN-DEV-4GB) and on two hosted systems (the MOE Hub and the
  Factory Forge).

The current project — the consolidation of that year of experiments
into a single governed architecture — is what this page describes.

## Where it's going (short version)

2027: the system ships as a working lifecycle-driven factory with
guardrails for AI and human users. 2028–2030: the tier structure
generalises — packaged user clones, an engineer tier for project
managers, and eventually a platform on which advanced users compose
their own systems-of-systems. The full forecast is on its own page.

---

## For the technically minded

The rest of this page is the architecture. Skip it if you don't need it.

### The three-tier gradient

The system is a gradient of AI complexity. The **Architect** (the
operator, me) absorbs the difficulty of safe AI use at authoring time.
The **Systems Engineer** composes project structure from the Architect's
pre-built atoms, with zero AI exposure. The **End User** runs the
composed lifecycle with AI present but safe — never managing failure.

The design rule: *does this push AI complexity up, or leak it down?*

### The atom

The smallest unit is the atom: a self-describing module that carries, by
construction, its own telemetry (a devlog hook), its own governance (a
contract, HITL checkpoints, validation and repair), and its own
provenance (who designed it, when, with which AI collaborator, for what
purpose). A topology built from atoms inherits all three. A topology
that bolts them on is not built from atoms.

### Governance as contract

AI sessions are governed by **discussion packets** — a transport (a
browser session or an in-interface endpoint) carrying a set of `.md`
documents and a prompt that define the session's contract: what it may
discuss, what it must return, how the output is checked. Each
discussion type (design, brainstorm, analysis-from-problem-statement)
has its own output contract, and the next phase's input contract is the
previous phase's output contract. The lifecycle is a contract pipeline.

### Telemetry as an archiver

A conceptual **archiver** records every file placement (datetime, path,
purpose), every request and response (prompt, response, status), and
every fallback (reason as error code, result). It is append-only and
machine-readable; human interpretation is a separate writer process that
reads the archiver and co-creates a narrative with an AI-writer. This is
what makes downstream devlogs, build-in-public videos, and ebooks a
*read* of the record rather than a re-authoring.

### The constraints are the design

- 4 GB laptop, 1.5 GB free after OS: deterministic DOS/Pascal console,
  filesystem as memory, single-threaded worker, one AI call at a time.
- Freemium AI only: Gemini and Groq reliably free, Manus as an agent;
  cross-backend repair; human fallback when the free tier cannot
  deliver.
- FaSaP: Functionality as Simply as Possible. Lucid code, no
  dependencies beyond the necessary.
