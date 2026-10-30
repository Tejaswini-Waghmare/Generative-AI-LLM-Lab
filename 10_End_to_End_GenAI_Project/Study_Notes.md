# End-to-End GenAI Project — Detailed Study Notes

## Learning objectives
Understand production-style architecture, evaluation, monitoring, documentation. Explain how the technique works, identify assumptions, and test a small offline demonstration.

## Core concepts

### Requirements
Specify target users, permitted answers, expected sources, latency goals, and escalation criteria.

### Pipeline
Load FAQ → vectorize → retrieve → threshold → cite → log metadata.

### Quality gates
Measure hit@k, inspect wrong answers, check source IDs and abstentions.

### Deployment considerations
Add authentication, access controls, secret management, monitoring, and incident response before production.

## Worked case study
Build a grounded helpdesk assistant with retrieval, evaluation and audit logs.

The shared dataset `data/helpdesk_faq.csv` contains synthetic policies and `data/evaluation_queries.csv` contains labeled questions. Use these only as learning examples.

## Responsible interpretation
A local lexical or rules-based demonstration does not prove that a real LLM, agent, or vector database works in production. Test the actual provider and real deployment constraints separately.

## Further reading
- scikit-learn User Guide: https://scikit-learn.org/stable/user_guide.html
- OWASP Top 10 for LLM Applications: https://genai.owasp.org/
- Hugging Face NLP Course: https://huggingface.co/learn/nlp-course/
