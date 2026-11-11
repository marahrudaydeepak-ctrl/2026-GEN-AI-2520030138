# Review-1 Presentation Guide
## Hallucination and Knowledge-Cutoff Probe for a Library Assistant

### Suggested 5–7 minute flow
1. Title and introduction (30 sec): state the title and library use case.
2. Problem (45 sec): LLMs may invent unsupported details or give outdated answers.
3. Proposed solution (60 sec): retrieve from library documents, answer from evidence, show sources, and abstain when evidence is insufficient.
4. Research and literature (90 sec): summarize FreshLLMs, Self-RAG, the hallucination survey, and the RAG evaluation survey.
5. Research gap and novelty (45 sec): test grounding, abstention, conflicting versions, and freshness together in a library setting.
6. Feasibility and architecture (60 sec): explain the limited dataset, retrieval pipeline, and test set.
7. Societal need and conclusion (30 sec): explain the value of reliable information for students.

### Proposed architecture
Library documents → text extraction → chunking/indexing → user question → retrieval → grounded response → citations or abstention → evaluation.

### Review rubric preparation
**1. Clarity of title (10):** Explain the terms. Hallucination means unsupported/fabricated output; knowledge cutoff is the limit of learned information; probe means systematic testing; library assistant defines the application.

**2. Feasibility (10):** Begin with a small set of permitted text/PDF documents, a basic retrieval pipeline, and a fixed test set. Risks include poor scans, irrelevant retrieval, conflicting versions, API limits, and wrong citations. Mitigate by starting with clean documents, preserving dates/titles, displaying source passages, and testing abstention. Present this as a prototype, not a production system.

**3. Societal need (10):** Students depend on reliable library information. Incorrect answers waste time and can spread misinformation. Evidence links encourage verification. The assistant supports, but does not replace, librarians or official notices.

**4. Novelty (10):** The title is specific and research-oriented. The focused contribution is combining hallucination probing and knowledge-freshness testing with evidence-based responses in a library-assistant scenario. Do not claim that RAG or hallucination detection is entirely new.

**5. Presentation skills (10):** Speak clearly, define technical terms, show one answerable and one unanswerable question, point to evidence, demonstrate abstention, and finish with limitations.

### Demo examples
- Ask for a borrowing period that is present in a sample policy; show the cited passage.
- Ask about a service absent from the documents; the assistant should say it cannot verify the answer.
- Ask for current opening hours using an old document; the assistant should flag possible outdated information.

### Likely questions
**What is hallucination?** An AI response that is false, unsupported, or not grounded in available evidence.

**What is a knowledge cutoff?** The point after which information may not be represented in training knowledge. It does not mean all earlier facts are correct.

**How will you reduce hallucinations?** Retrieve relevant documents, ground answers in passages, show citations, and abstain when evidence is insufficient. This reduces risk but cannot guarantee zero errors.

**How will you test it?** Use answerable, unanswerable, conflicting/versioned, and freshness-sensitive questions; measure correctness, evidence support, citations, and abstention.

**What is the novelty?** A focused library-specific evaluation of grounding, missing-evidence abstention, version conflicts, and freshness.

**Is it feasible?** Yes, as a limited prototype with a small document collection, retrieval, a response layer, and a fixed test set.

### Generic team split
- Member 1: title, abstract, problem.
- Member 2: research papers.
- Member 3: literature survey and research gap.
- Member 4: feasibility, architecture, evaluation, conclusion.
- All members: societal need, novelty, and Q&A.

**Important:** Describe planned features as planned. Report measured results only after running the prototype and recording results.
