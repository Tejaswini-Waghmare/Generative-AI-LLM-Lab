# LLM Fundamentals — Detailed Study Notes

## Learning objectives
Understand tokenization, context windows, generation, temperature, limitations. Explain how the technique works, identify assumptions, and test a small offline demonstration.

## Core concepts

### What is a language model?
A language model estimates probabilities over token sequences. A generative model selects or samples a continuation conditioned on its context. A deterministic frequency counter is a baseline, not an LLM.

### Tokens and context
A token is a unit from a tokenizer, often a word fragment. Context windows limit the amount of text the model can attend to. Long inputs may be truncated or summarized.

### Sampling
Temperature scales logits before softmax. Higher values generally increase randomness. Reproducibility requires controlling seeds and model/version settings.

### Limitations
Fluent text does not guarantee factuality. Assess grounding, privacy, bias, latency, and cost.

## Worked case study
Implement a simple word/token frequency baseline and compare sampling.

The shared dataset `data/helpdesk_faq.csv` contains synthetic policies and `data/evaluation_queries.csv` contains labeled questions. Use these only as learning examples.

## Responsible interpretation
A local lexical or rules-based demonstration does not prove that a real LLM, agent, or vector database works in production. Test the actual provider and real deployment constraints separately.

## Further reading
- scikit-learn User Guide: https://scikit-learn.org/stable/user_guide.html
- OWASP Top 10 for LLM Applications: https://genai.owasp.org/
- Hugging Face NLP Course: https://huggingface.co/learn/nlp-course/
