# AI Agents and Tools — Detailed Study Notes

## Learning objectives
Understand tool selection, bounded loops, validation, human approvals. Explain how the technique works, identify assumptions, and test a small offline demonstration.

## Core concepts

### Agent loop
Plan → select permitted tool → validate arguments → execute → inspect → stop or continue.

### Tool contracts
Use typed parameters, allowlists, and explicit limits. Never execute arbitrary model-produced code.

### Approvals
Require human approval for irreversible or sensitive actions.

### Bounded execution
Use a maximum step count, timeouts, audit logs, and failure handling.

## Worked case study
Create a deterministic agent simulator with a calculator and FAQ lookup.

The shared dataset `data/helpdesk_faq.csv` contains synthetic policies and `data/evaluation_queries.csv` contains labeled questions. Use these only as learning examples.

## Responsible interpretation
A local lexical or rules-based demonstration does not prove that a real LLM, agent, or vector database works in production. Test the actual provider and real deployment constraints separately.

## Further reading
- scikit-learn User Guide: https://scikit-learn.org/stable/user_guide.html
- OWASP Top 10 for LLM Applications: https://genai.owasp.org/
- Hugging Face NLP Course: https://huggingface.co/learn/nlp-course/
