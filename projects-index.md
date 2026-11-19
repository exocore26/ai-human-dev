# Projects

A map of what I've built this year, in roughly reverse order of
importance. Each entry says what it is, what it proves, and where to
see it. The current project — the META-SYSTEM — has its own page; the
rest are summarised here with links.


---

## Live Client Work

**Carpet Clean Derby** — [carpetcleanderby.co.uk](https://carpetcleanderby.co.uk/)
**What it is:** A live, public-facing website built for a real-world local business (my stepson's carpet cleaning company).
**What it proves:** That I can take a brief, design a functional interface, and ship a finished product to the open web. It is the "in the wild" proof that what I build actually works for real users, not just in a local test environment.
**Status:** Live and in use.

---
## META-SYSTEM

**What it is:** A governed software factory. A non-technical user
describes what they want to build, and the system guides them through a
structured project lifecycle with AI assistance that stays on task
because the guardrails are built in. Runs on free AI tiers and a 4 GB
laptop.

**What it proves:** That the cost of AI-assisted development — managing
the AI's drift, hallucination, and truncation — can be moved from the
user into the tool's architecture. Not better AI; a better envelope
around the AI.

**Status:** In active development. The console, bridge, three AI
backends, JSON validation and repair, and the archiver are working. The
three-tier architecture is being consolidated from a year of prior
experiments.

**Where:** [Full page →](meta-system.md) · [Code and working notes on request]

---

## MOE — Micro-SaaS Discovery Engine

**What it is:** A discovery engine that identifies micro-SaaS
opportunities and turns them into candidate projects, with a pipeline
from signal to paying customer. Each opportunity moves through
discovery, framing, and candidate stages, with its own telemetry and
working-set state.

**What it proves:** That I can build and ship a working system that
takes an open-ended problem (find a viable micro-business) and
decomposes it into a repeatable, multi-stage pipeline — the same
factory pattern the META-SYSTEM generalises.

**Status:** Working. Hosted publicly.

**Where:** [exocore26.github.io/hub](https://exocore26.github.io/hub/)

---

## Factory Forge — Common Tool Requirements Forge

**What it is:** A static, dependency-free tool that turns a tool idea
into a reusable requirements document and a development TODO, while
actively testing what belongs in a shared "Parent-Engine" layer versus
what stays project-specific. It walks through frame → outcome → flow →
abstract → human-in-the-loop → acceptance → review → generate.

**What it proves:** The abstraction discipline at the heart of the
META-SYSTEM — "describe the sub-project first, abstract the shared
capability second" — implemented as a working interface. It is the
single-test design rule ("would a second unrelated project need the
same mechanism?") made concrete.

**Status:** Working. Hosted publicly.

**Where:** [exocore26.github.io/factory](https://exocore26.github.io/factory)

---

## The experiments (2026)

A year of deliberately small experiments, each one teaching a piece of
what the META-SYSTEM now consolidates. Documented as build-in-public
video logs on YouTube.

**What they cover:**

- **Task pipeline** — a purpose-named file tree, a persistent task
  database, and an HTML interface that generated AI instructions from
  clicked tasks. Worked end-to-end to the AI; stopped at the point
  where conducting the rest of the build became unclear.
- **Agentic clients** — hands-on with as many lightweight agentic
  clients as I could find, to learn what they could and couldn't hold.
- **Local models** — Ollama with Qwen 2.5, exploring what a small local
  model could do on limited hardware.
- **Edge-to-laptop message passing** — an Android app (command-line
  built) talking to Termux, enriching task text with Qwen into JSON,
  sending via Telegram, and picked up by the Dell. A resource-efficient
  message-passing pattern between edge nodes and the laptop.
- **Android baseline** — a golden-template mapper to a new Android app
  baseline build on the command line, proving I could make Android apps
  independently.
- **Poker arena (design only)** — an object-oriented analysis from
  earlier years: a multiplayer no-limit hold'em tournament arena with
  programmable bots, skill-credit training, and levelling metrics. Not
  built; included because it shows the kind of system I was designing
  long before I could build it.

**What they prove:** Each experiment added one piece — message passing,
local inference, interface generation, lifecycle thinking — and each
one hit the same wall: the AI could generate, but could not stay on
task. That repeated wall is what the META-SYSTEM exists to remove.

**Where:** [YouTube — @AI-HUMAN-DEV-4GB](https://www.youtube.com/@AI-HUMAN-DEV-4GB)

---

## Earlier work (the silent years)

Not projects in the software sense, but part of the record: thirty years
of object-oriented analysis on paper — problem-statement decomposition
analysers, NLP programming in Pascal, the poker arena above. Sketched,
not built. The Origin page tells that story.

**Where:** [Origin →](origin.md)
