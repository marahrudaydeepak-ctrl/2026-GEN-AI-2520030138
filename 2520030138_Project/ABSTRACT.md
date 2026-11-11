# Abstract
## Hallucination and Knowledge-Cutoff Probe for a Library Assistant

Large language models (LLMs) can generate fluent but incorrect or unsupported answers. Their training knowledge also has a cutoff, so facts such as library policies, opening hours, editions, and availability may become outdated. In a library setting, these errors can mislead students who rely on the assistant.

This project proposes a prototype library assistant that answers questions using a controlled collection of library documents. It retrieves relevant passages, generates an answer grounded in those passages, and displays supporting evidence. If the documents do not contain enough information, the assistant should state that it cannot verify the answer rather than inventing one. Questions that may require current information are flagged as freshness-sensitive.

The prototype will be tested with four question categories: answerable, unanswerable, conflicting/versioned, and freshness-sensitive. Evaluation will consider answer correctness, evidence support, citation correctness, appropriate abstention, and freshness awareness.

The expected outcome is a practical demonstration of how retrieval, visible evidence, uncertainty handling, and knowledge-cutoff probing can improve the dependability of a library assistant. The work is scoped as a student prototype and does not replace librarians or official institutional notices.

**Keywords:** LLM, hallucination, knowledge cutoff, Retrieval-Augmented Generation, library assistant, citation, abstention, freshness.
