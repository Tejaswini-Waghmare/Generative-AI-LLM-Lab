# Safety and Guardrails — Detailed Study Notes

## Learning objectives
Understand pii handling, injection, unsafe requests, policy gates. Explain how the technique works, identify assumptions, and test a small offline demonstration.

## Core concepts

### Threat model
Consider prompt injection, exfiltration, sensitive data leakage, unsafe tool use, and hallucinations.

### PII minimization
Avoid storing unnecessary personal identifiers; redact in logs and limit retention.

### Input checks
Validation is defense-in-depth, not a guarantee. Rules are bypassable; evaluate adversarially.

### Output checks
Validate format, citations, source provenance, and action permissions.

## Worked case study
Build input/output checks and adversarial tests.

The shared dataset `data/helpdesk_faq.csv` contains synthetic policies and `data/evaluation_queries.csv` contains labeled questions. Use these only as learning examples.

## Responsible interpretation
A local lexical or rules-based demonstration does not prove that a real LLM, agent, or vector database works in production. Test the actual provider and real deployment constraints separately.

## Further reading
- scikit-learn User Guide: https://scikit-learn.org/stable/user_guide.html
- OWASP Top 10 for LLM Applications: https://genai.owasp.org/
- Hugging Face NLP Course: https://huggingface.co/learn/nlp-course/
