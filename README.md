# Grounded Brain-Network Knowledge Graph

A source-grounded, physician-adjudicated knowledge graph of human brain networks — built so an AI can reason over neuroscience **only from checked, cited evidence**, and say *"I don't know"* when the evidence isn't there.

**Author:** Steven Anander, MD — board-certified internal medicine physician
**Status:** Active research build. This repository is an overview with representative samples; the full corpus is available on request.

---

## The problem

Ask an AI a hard brain or medical question today and it can sound confident while quietly guessing — blurring the direction of a connection, overstating certainty, or stating an association as if it were a cause. In medicine, that failure mode is dangerous.

## What this is

A machine-readable, traversable map of brain networks. For each structure it captures what it is, where it sits, how it is wired, what it does, and what it connects to — and only what the peer-reviewed evidence supports. A language model is intended to sit on top of the graph and answer by **following the actual nodes and edges**, showing its sources and stopping where the evidence stops.

It is **not** a chatbot, an interactive textbook, or another UpToDate/WebMD. It is a mechanistic substrate an AI can reason across.

## How it's built

Every node is constructed under a strict operational **doctrine stack** — a set of interlocking standards that turn a published scientific claim into a stable graph node and a typed relationship. Sources are current peer-reviewed publications (primary papers and major reviews, not textbook summaries). Because every entry is built to the same standard, findings from molecular biology, clinical neurology and psychiatry, behavioral psychology, and systems neuroscience all occupy the **same graph language** rather than staying trapped in separate literatures.

**I make the final call on every node.** The AI does the labor; the scientific judgment — meticulous construction, review, and sign-off — is human.

## What exists today

| Structure | State | ~Entries |
|---|---|---|
| Anterior cingulate cortex (ACC) | Built in depth, across five analytic lenses | ~254 |
| Midcingulate cortex (MCC) | Solid slice, in progress | partial |
| Thalamus | Earlier map; already wired into the cingulate | ~232 |

Roughly **500 graphable nodes** in total, with **cross-region traversal already demonstrated** — the thalamus map connects into the cingulate circuits. See **[SAMPLE_ENTRIES.md](SAMPLE_ENTRIES.md)** for real nodes and their typed edges.

## The goal

Load the corpus into a graph backend (e.g., Neo4j) and put a Claude agent on top: a grounded query tool that answers plain-English questions from the sourced graph, holds up against ordinary ungrounded answers, and can generate diagrams constrained by the graph itself. The long-term aim is a grounded, mechanistic brain map that clinicians, researchers, and drug developers can question and trust.

## Contact

Steven Anander, MD. Sample entries, a written summary, and further detail available on request.
