# Origin

## The short version

I was a good computing student. Then life intervened, and I spent nearly
thirty years as a silent architect — sketching systems on paper, not
building them. In January 2026 I started again, with free AI tools and a
4 GB laptop. This is what happened next.

## The longer version

I did a BSc in Computing. By the end of second year I had top marks in
assembly, C++, object-oriented analysis and design, Pascal, and Java. I
was on a first-class trajectory.

Then a family tragedy chain hit — my sister died, my stepmum was arrested
and we lost the council home as a result. We, as in the family, became
homeless, then in private rented accommodation I was  forced to work
menial jobs with my father just to keep the rent paid. I dropped out of
third year. Deferred for a year. Came back part-time, interrupted. What
should have been three years took seven and a half, and ended with a 2.2.

At the time it had felt like all of it — the GCSE resits, the two years
of college A-levels to reach the degree and then the degree itself — had 
amounted to nothing but a waste of nearly 11 years.

But I never stopped thinking about the problem. Over the next thirty
years, on scraps of paper and idle moments, I kept doing what I'd been
trained to do: object-oriented analysis of systems I could see clearly
and couldn't build. A multiplayer poker arena with programmable bots,
skill-credit training, and levelling metrics. Problem-statement
decomposition analysers. NLP programming in Pascal. I was a silent
architect, and I had a drawer full of half-built designs.

## January 2026

The media spotlight turned on AI, and I had time on my hands — I hadn't
been working, because of depression. I started having chats with ChatGPT
and Gemini. I watched the "how I made a million with AI" videos, then
realised the people making them had GPUs, audiences, and hardware I
didn't have. I had a Dell Inspiron with 4 GB of RAM and 1.5 GB free
after the OS loaded.

So I tried freemium AI on Windows. A month of fighting with PowerShell
and the popular IDEs — Android Studio, Cursor, VS Code — and I gave up
on friction. I installed Linux Mint XFCE, installed Python, and in May
2026 I wrote my first code in nearly thirty years.

## What I built, and why it kept stopping

My first project was a dynamic todo list — a file tree with purpose-
named directories, a text file of what I wanted to make, a database of
persistent tasks, and an HTML interface where clicking a task generated
instructions for an AI. It worked all the way to the AI. Then I hit
friction: I wasn't sure how to conduct the rest of the build, and I
abandoned it.

I kept experimenting. Lightweight agentic clients. Ollama with Qwen
2.5. An Android app built on the command line, talking to Termux, which
enriched task text with Qwen into JSON, sent it via Telegram, and picked
it up on the Dell. Message-passing between edge nodes and the laptop,
resource-efficient. A golden-template Android baseline build. Each one
taught me a piece.

## The pattern I found

Every experiment hit the same wall: the AI could generate, but it could
not *stay on task*. It drifted, hallucinated, truncated, lost alignment.
I was spending my time managing the AI's failures instead of building.

So I made a decision. Stop shipping apps. Build the system that *forces*
the AI to stay on task — a governed, lifecycle-driven factory with
guardrails for both AI and human users, built on the smallest possible
unit, so that every part of it carries its own telemetry and its own
contract.

That system is the **META-SYSTEM**. It is what this site is about.

## A note on the 4 GB

Every byte counts. The laptop has 1.5 GB free after the OS loads. The
system is built for that constraint deliberately, not despite it: a
deterministic DOS/Pascal console governing probabilistic Python and AI
backends, a filesystem as memory, a single-threaded worker, and free AI
backends only. The constraint is the design.
