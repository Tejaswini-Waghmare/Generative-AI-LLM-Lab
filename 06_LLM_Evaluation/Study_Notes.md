# LLM Evaluation — Detailed Study Notes

## Learning objectives
Understand groundedness, precision@k, recall@k, latency, regression tests. Explain how the technique works, identify assumptions, and test a small offline demonstration.

## Core concepts

### Retrieval evaluation
Compare top-k IDs to labeled relevant document IDs; calculate hit@k and mean reciprocal rank.

### Answer evaluation
Assess correctness, faithfulness, citation accuracy, refusal behavior, and helpfulness separately.

### Regression tests
Pin a fixed evaluation set and rerun after any prompt, model, or index change.

### Uncertainty
Small synthetic test sets do not establish production quality; report sample size and failure cases.

## Worked case study
Evaluate retrieval with labeled question-answer pairs.

The shared dataset `data/helpdesk_faq.csv` contains synthetic policies and `data/evaluation_queries.csv` contains labeled questions. Use these only as learning examples.

## Responsible interpretation
A local lexical or rules-based demonstration does not prove that a real LLM, agent, or vector database works in production. Test the actual provider and real deployment constraints separately.

## Further reading
- scikit-learn User Guide: https://scikit-learn.org/stable/user_guide.html
- OWASP Top 10 for LLM Applications: https://genai.owasp.org/
- Hugging Face NLP Course: https://huggingface.co/learn/nlp-course/
