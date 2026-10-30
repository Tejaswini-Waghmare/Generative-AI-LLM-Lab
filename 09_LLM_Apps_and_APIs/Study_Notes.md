# LLM Apps and APIs — Detailed Study Notes

## Learning objectives
Understand app architecture, caching, retries, cost, api integration. Explain how the technique works, identify assumptions, and test a small offline demonstration.

## Core concepts

### Application architecture
Separate UI, retrieval, orchestration, model adapter, validation, and logging.

### Reliability
Use retries with exponential backoff for transient failures, timeouts, caching, and circuit breakers.

### Cost and latency
Track token use, request duration, cache hit rate, and error rates.

### Secrets
Use environment variables or a secret manager; never commit API keys.

## Worked case study
Build a CLI FAQ application with optional API integration notes.

The shared dataset `data/helpdesk_faq.csv` contains synthetic policies and `data/evaluation_queries.csv` contains labeled questions. Use these only as learning examples.

## Responsible interpretation
A local lexical or rules-based demonstration does not prove that a real LLM, agent, or vector database works in production. Test the actual provider and real deployment constraints separately.

## Further reading
- scikit-learn User Guide: https://scikit-learn.org/stable/user_guide.html
- OWASP Top 10 for LLM Applications: https://genai.owasp.org/
- Hugging Face NLP Course: https://huggingface.co/learn/nlp-course/
