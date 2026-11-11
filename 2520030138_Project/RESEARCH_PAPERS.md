# Research Papers
## Hallucination and Knowledge-Cutoff Probe for a Library Assistant

### 1. FreshLLMs: Refreshing Large Language Models with Search Engine Augmentation
- Tu et al., Findings of ACL 2024.
- Paper: https://aclanthology.org/2024.findings-acl.813/
- Preprint: https://arxiv.org/abs/2310.03214
- Relevance: Studies freshness-sensitive question answering and motivates testing questions whose answers may have changed after model training.

### 2. Self-RAG: Learning to Retrieve, Generate, and Critique through Self-Reflection
- Asai et al., ICLR 2024.
- Paper: https://proceedings.iclr.cc/paper_files/paper/2024/hash/25f7be9694d7b32d5cc670927b8091e1-Abstract-Conference.html
- Preprint: https://arxiv.org/abs/2310.11511
- Relevance: Explores selective retrieval and self-critique; it motivates grounding responses in retrieved passages and checking support.

### 3. A Survey on Hallucination in Large Language Models: Principles, Taxonomy, Challenges, and Open Questions
- Huang et al., ACM Transactions on Information Systems, 2025.
- DOI: https://doi.org/10.1145/3703155
- Relevance: Provides a taxonomy and overview of causes, evaluation, and mitigation of hallucination.

### 4. Retrieval-Augmented Generation (RAG) Evaluation: A Survey
- Gan et al., 2025.
- Preprint: https://arxiv.org/abs/2504.14891
- Relevance: Reviews evaluation approaches for retrieval-augmented systems and informs our choice of retrieval, grounding, and answer-quality measures.

## Connection to this project
| Research theme | How it informs the prototype |
|---|---|
| Freshness-sensitive QA | Test questions about information that may have changed |
| Retrieval and self-critique | Retrieve passages and check whether claims are supported |
| Hallucination taxonomy | Classify unsupported, contradictory, and fabricated responses |
| RAG evaluation | Measure retrieval relevance, faithfulness, and answer quality |

These papers are starting references. The prototype must be evaluated independently; their reported results must not be presented as results of this project.
