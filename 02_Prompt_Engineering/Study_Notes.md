# Prompt Engineering — Detailed Study Notes

## Learning objectives
Understand task instructions, examples, structured outputs, prompt injection defense. Explain how the technique works, identify assumptions, and test a small offline demonstration.

## Core concepts

### Prompt anatomy
State role/task, relevant context, constraints, expected output schema, and examples. Prefer explicit success criteria.

### Few-shot prompting
Show representative input-output pairs. Check for overfitting to examples and unseen cases.

### Structured outputs
Validate JSON against a schema. Never trust unvalidated model output as code or tool arguments.

### Injection risk
Treat retrieved documents and user content as untrusted data, not higher-priority instructions.

## Worked case study
Build a template-based support-ticket classifier and test prompts.

The shared dataset `data/helpdesk_faq.csv` contains synthetic policies and `data/evaluation_queries.csv` contains labeled questions. Use these only as learning examples.

## Responsible interpretation
A local lexical or rules-based demonstration does not prove that a real LLM, agent, or vector database works in production. Test the actual provider and real deployment constraints separately.

## Further reading
- scikit-learn User Guide: https://scikit-learn.org/stable/user_guide.html
- OWASP Top 10 for LLM Applications: https://genai.owasp.org/
- Hugging Face NLP Course: https://huggingface.co/learn/nlp-course/
