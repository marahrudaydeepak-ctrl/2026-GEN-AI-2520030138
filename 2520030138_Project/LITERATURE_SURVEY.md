# Literature Survey
## Hallucination and Knowledge-Cutoff Probe for a Library Assistant

### 1. Background
LLMs generate text from patterns learned during training and may produce plausible statements unsupported by evidence. Their training data also has a cutoff, meaning that policies, opening hours, editions, and availability can change after the model's knowledge was formed. A library assistant must therefore distinguish verified document-based answers from guesses and potentially outdated information.

### 2. Review of related work
**FreshLLMs (Tu et al., Findings of ACL 2024).** This work studies freshness-sensitive question answering and the limitations of relying on static model knowledge. It motivates a test category for facts that may have changed. Our project applies this concern to library documents and versioned information.

**Self-RAG (Asai et al., ICLR 2024).** This work investigates when a model should retrieve information and how it can critique generated responses. It motivates retrieving passages before answering and checking whether the evidence supports the response. Our prototype makes the evidence visible to users.

**Huang et al. (ACM TOIS, 2025).** This survey organizes research on hallucination, including definitions, causes, evaluation, and mitigation. It provides a basis for classifying unsupported claims, contradictions, and factual errors.

**Gan et al. (2025), RAG Evaluation Survey.** This survey reviews evaluation methods for retrieval-augmented generation. It supports evaluating retrieval and grounding rather than judging an answer only by fluency.

### 3. Comparative summary
| Work | Main focus | Project relevance | Limitation for our use |
|---|---|---|---|
| FreshLLMs (2024) | Freshness-sensitive QA | Motivates freshness tests | Not library-specific |
| Self-RAG (2024) | Retrieval and self-reflection | Motivates evidence retrieval and checking | Full implementation may exceed prototype scope |
| Huang et al. (2025) | Hallucination survey | Supplies definitions and taxonomy | Survey does not implement our application |
| Gan et al. (2025) | RAG evaluation | Guides evaluation dimensions | General methods need adaptation to our small dataset |

### 4. Research gap
The reviewed work addresses freshness, retrieval, hallucination, and RAG evaluation as broader topics. This project brings these concerns together in a focused library-assistant probe. It will test whether:
1. An answer is present in the supplied documents.
2. Important claims are supported by retrieved passages.
3. The assistant abstains when evidence is missing or insufficient.
4. Conflicting document versions are identified.
5. Freshness-sensitive questions are flagged when no current source is available.

This is the project's application and evaluation focus, not a claim that hallucination detection or RAG is entirely new.

### 5. Proposed evaluation
- **Answer correctness:** consistency with a reference answer.
- **Evidence support / faithfulness:** whether factual claims are supported by retrieved passages.
- **Citation correctness:** whether citations point to supporting passages.
- **Abstention quality:** whether the assistant avoids guessing when evidence is insufficient.
- **Freshness awareness:** whether potentially changed facts are flagged.
- **Retrieval relevance:** whether retrieved passages relate to the question.

Use a manually checked test set covering answerable, unanswerable, conflicting/versioned, and freshness-sensitive questions. Report the test-set size, examples, and observed failures.

### 6. Conclusion
The literature motivates combining document retrieval, visible evidence, uncertainty handling, and freshness tests. The prototype will investigate these features in a library use case and report limitations transparently.
