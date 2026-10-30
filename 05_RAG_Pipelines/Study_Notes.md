# Retrieval-Augmented Generation — Detailed Study Notes

## Learning objectives
Understand chunking, retrieval, citations, abstention, grounded generation. Explain how the technique works, identify assumptions, and test a small offline demonstration.

## Core concepts

### RAG architecture
Ingest → chunk → embed/index → retrieve → rerank → assemble context → answer → cite → evaluate.

### Grounded answers
Require each factual claim to be supported by retrieved context. Abstain when evidence is weak.

### Chunking
Chunks balance context completeness with retrieval precision; keep stable source identifiers.

### No model in demo
The notebook returns an extractive answer with a citation, not newly generated text.

## Worked case study
Build a local extractive RAG assistant with source citations.

The shared dataset `data/helpdesk_faq.csv` contains synthetic policies and `data/evaluation_queries.csv` contains labeled questions. Use these only as learning examples.

## Responsible interpretation
A local lexical or rules-based demonstration does not prove that a real LLM, agent, or vector database works in production. Test the actual provider and real deployment constraints separately.

## Further reading
- scikit-learn User Guide: https://scikit-learn.org/stable/user_guide.html
- OWASP Top 10 for LLM Applications: https://genai.owasp.org/
- Hugging Face NLP Course: https://huggingface.co/learn/nlp-course/
