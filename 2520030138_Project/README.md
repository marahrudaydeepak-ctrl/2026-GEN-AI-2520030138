# Hallucination and Knowledge-Cutoff Probe for a Library Assistant

**Review-1 documentation**

## Documents
- [Abstract](ABSTRACT.md)
- [Research Papers](RESEARCH_PAPERS.md)
- [Literature Survey](LITERATURE_SURVEY.md)
- [Review-1 Presentation Guide](REVIEW1_PRESENTATION.md)

## Problem statement
A library assistant powered by an LLM may provide fabricated, unsupported, or outdated information. This project proposes a prototype that retrieves evidence from a controlled library-document collection, grounds answers in retrieved passages, displays sources, and abstains when evidence is insufficient.

## Objectives
1. Probe hallucinated and unsupported answers in a library setting.
2. Test questions affected by model knowledge cutoff and changing information.
3. Retrieve library documents and show supporting evidence.
4. Handle missing evidence and conflicting versions transparently.
5. Evaluate using a repeatable set of test questions.

## Feasibility
Start with a small collection of permitted documents and a limited test set. A basic implementation can use document extraction, chunking, retrieval, a language-model or controlled response layer, and a simple interface. Expand only after the basic workflow works.

## Societal relevance
Students need dependable library information. Evidence and honest uncertainty can reduce misinformation and encourage verification with official sources or library staff.

## Workflow
Documents → extraction → chunking/indexing → question → retrieval → grounded response → citations or abstention → evaluation.

## Review-1 rubric
Prepare title clarity, feasibility, societal need, novelty, and presentation skills. Use the linked presentation guide for talking points and likely questions.

**Scope note:** This is a proposed student prototype. Do not claim features are implemented or performance measured until verified experimentally.
