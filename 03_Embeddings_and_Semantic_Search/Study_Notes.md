# Embeddings and Semantic Search — Detailed Study Notes

## Learning objectives
Understand vector representations, cosine similarity, retrieval metrics. Explain how the technique works, identify assumptions, and test a small offline demonstration.

## Core concepts

### Vector representation
TF-IDF weights terms by frequency and inverse document frequency. It is sparse lexical retrieval, not neural semantic understanding.

### Cosine similarity
cos(a,b) = dot(a,b) / (norm(a)*norm(b)). Higher cosine often means closer vector direction.

### Retrieval metrics
Precision@k measures fraction of retrieved items relevant; recall@k measures fraction of all relevant items retrieved.

### Failure modes
Synonyms, negation, short queries, and ambiguous vocabulary can reduce lexical retrieval quality.

## Worked case study
Implement TF-IDF semantic-ish retrieval baseline over a FAQ corpus.

The shared dataset `data/helpdesk_faq.csv` contains synthetic policies and `data/evaluation_queries.csv` contains labeled questions. Use these only as learning examples.

## Responsible interpretation
A local lexical or rules-based demonstration does not prove that a real LLM, agent, or vector database works in production. Test the actual provider and real deployment constraints separately.

## Further reading
- scikit-learn User Guide: https://scikit-learn.org/stable/user_guide.html
- OWASP Top 10 for LLM Applications: https://genai.owasp.org/
- Hugging Face NLP Course: https://huggingface.co/learn/nlp-course/
