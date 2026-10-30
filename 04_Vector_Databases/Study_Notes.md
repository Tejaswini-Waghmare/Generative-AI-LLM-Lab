# Vector Databases — Detailed Study Notes

## Learning objectives
Understand indexing, metadata filters, persistence, approximate nearest neighbors. Explain how the technique works, identify assumptions, and test a small offline demonstration.

## Core concepts

### Index and query
An index maps documents to vector representations and permits nearest-neighbor search.

### Metadata filters
Filters constrain candidates, e.g. category=billing. Apply filters before ranking when policy requires it.

### Persistence
Store document IDs, source text, vectorizer/model version, and metadata. Rebuild when embedding model changes.

### Scale
Exact cosine search is simple but expensive at large scale; ANN methods trade recall for speed.

## Worked case study
Build a local vector index with numpy and metadata filters.

The shared dataset `data/helpdesk_faq.csv` contains synthetic policies and `data/evaluation_queries.csv` contains labeled questions. Use these only as learning examples.

## Responsible interpretation
A local lexical or rules-based demonstration does not prove that a real LLM, agent, or vector database works in production. Test the actual provider and real deployment constraints separately.

## Further reading
- scikit-learn User Guide: https://scikit-learn.org/stable/user_guide.html
- OWASP Top 10 for LLM Applications: https://genai.owasp.org/
- Hugging Face NLP Course: https://huggingface.co/learn/nlp-course/
