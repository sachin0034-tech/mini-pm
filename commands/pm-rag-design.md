---
description: Design a RAG (Retrieval-Augmented Generation) system product spec with architecture, quality, and eval plan
---

You are a PM speccing a RAG system for:

**Input:** $ARGUMENTS (use case, data sources, users, latency/quality requirements)

## 1. RAG System Overview

**Use case:**
**Users:**
**Queries per day (estimated):**
**Latency requirement (P99):**
**Quality bar:** (what does a "correct" answer mean here?)

---

## 2. Knowledge Base Design

### Data Sources
| Source | Type | Update frequency | Volume | Sensitivity |
|--------|------|-----------------|--------|------------|
| | Doc / DB / API | | | Public / Internal / PII |

### Chunking Strategy
| Approach | Best for | Trade-off |
|----------|---------|----------|
| Fixed-size (512 tokens) | Uniform content | May split mid-concept |
| Sentence-based | Q&A, facts | Variable chunk size |
| Semantic (paragraph) | Narrative docs | Requires more compute |
| Hierarchical | Long documents | Complex to implement |

**Recommendation for this use case:** [Approach + rationale]

### Metadata Schema
What metadata should be stored alongside each chunk?
- Source document / URL
- Creation / update date
- Author / team
- Document type
- Confidence / quality score
- Access control tags

---

## 3. Retrieval Architecture

### Retrieval Strategy
| Strategy | Mechanism | When to use |
|----------|-----------|------------|
| Dense (semantic) | Embedding similarity | Meaning-based queries |
| Sparse (BM25/TF-IDF) | Keyword matching | Exact term queries |
| Hybrid | Combine both | General purpose (recommended) |

**Recommended for this use case:** Hybrid retrieval

### Embedding Model
| Model | Quality | Cost | Latency | Recommended if |
|-------|---------|------|---------|----------------|
| text-embedding-3-small | Good | Low | Fast | Volume > cost |
| text-embedding-3-large | Excellent | High | Medium | Quality critical |

### Reranking
Should retrieved chunks be reranked before passing to LLM?
- Cross-encoder reranker improves quality by ~15–20% but adds ~100ms latency
- Recommendation: [Yes/No based on latency requirement]

---

## 4. Generation Design

### Context Window Management
- Retrieved chunks: [N chunks × ~500 tokens each = X tokens]
- System prompt: ~200 tokens
- Reserve for output: ~500 tokens
- Total must fit in model context window

### Citation Requirements
- [ ] Every factual claim must cite source
- [ ] Citation format: inline [1] or footnote
- [ ] Show source document title + link

### Hallucination Mitigation
- Instruction to model: "Only use information from the provided context. If the answer isn't in the context, say so."
- Groundedness eval: automated check that claims appear in retrieved chunks

---

## 5. Quality Dimensions & Eval Plan

| Dimension | Definition | Target | Eval method |
|-----------|-----------|--------|-------------|
| **Retrieval Recall** | Relevant docs in top-K | >90% | Labeled test set |
| **Retrieval Precision** | % of retrieved docs that are relevant | >70% | Labeled test set |
| **Answer Correctness** | Answer matches ground truth | >85% | Human eval |
| **Groundedness** | Answer supported by retrieved context | >95% | Automated |
| **Latency (P99)** | End-to-end response time | <[X]s | Automated |
| **No-Answer Rate** | Model says "I don't know" when it should | <5% | Labeled no-answer set |

---

## 6. Failure Modes

| Failure | Cause | Mitigation |
|---------|-------|-----------|
| Retrieved wrong context | Query-chunk mismatch | Hybrid retrieval, reranking |
| Hallucinated beyond context | Model ignores retrieval | System prompt constraints |
| Stale information | Knowledge base not updated | Update cadence SLA |
| No results returned | Query not in KB | Fallback behavior defined |
| PII in retrieved chunks | Sensitive data in KB | Pre-filter and access control |

---

## 7. Knowledge Base Maintenance
- **Update frequency:**
- **Ingestion pipeline:**
- **Chunk freshness tracking:**
- **Stale doc removal:**
- **Quality monitoring:**

---

## 8. Cost Model
| Component | Cost driver | Estimated monthly cost |
|-----------|------------|----------------------|
| Embedding (indexing) | # documents × tokens | |
| Embedding (query time) | Queries/day × tokens | |
| Vector DB storage | # vectors × dimensions | |
| LLM generation | Tokens in + out | |
| **Total** | | |
