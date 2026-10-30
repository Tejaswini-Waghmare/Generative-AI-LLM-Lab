# Worked Solutions and Answer Guide

These are reference approaches; many questions permit multiple valid answers.

## 1. Explain the primary concept of this module in your own words.

End-to-End GenAI Project concerns production-style architecture, evaluation, monitoring, documentation.


## 2. Identify two limitations of the offline baseline.

The local baseline lacks pretrained generative reasoning and may fail on synonyms or adversarial input.


## 3. Load the FAQ CSV and count rows per category.

```python
print(faq.groupby('category').size())
```


## 4. Inspect and report missing values in both CSVs.

```python
print(faq.isna().sum())
print(labels.isna().sum())
```


## 5. Write one new realistic user question and its expected FAQ document.

Example: “Can I get an invoice?” → FAQ-006; verify using the dataset.


## 6. Describe how you would measure whether the system answers correctly.

Use a labeled holdout set, top-1 accuracy or hit@k, and human review of unsupported answers.


## 7. Change one parameter in the example and record the outcome.

Change the retrieval k, threshold, or n-gram range; compare retrieved document IDs.


## 8. Create one negative test case that should abstain or escalate.

Ask an out-of-domain question such as “What is the weather on Mars?” and require escalation.


## 9. Explain why untrusted document text must not control tool behavior.

Documents can contain attacker instructions; keep them as quoted evidence, never privileged commands.


## 10. Compare lexical TF-IDF retrieval with neural embeddings.

TF-IDF relies on term overlap; neural embeddings may capture paraphrases but need model evaluation.


## 11. Write a function that checks a response contains a source ID.

```python
import re
def has_citation(s):
    return bool(re.search(r'FAQ-\d{3}',s))
```


## 12. Design a 5-row evaluation table with query, expected ID, predicted ID, pass/fail.

Create columns query, expected_doc_id, predicted_doc_id, correct; compute correct.mean().


## 13. Describe a privacy risk and a mitigation.

Do not log raw emails or account details; redact and limit retention.


## 14. Describe one failure mode for ambiguous or multi-intent questions.

A request combining returns and billing may require clarification or multiple sources.


## 15. Propose a safe human-review fallback.

Escalate low-confidence answers to a human, preserving source references.


## 16. Write three unit tests for a helper function in this module.

```python
assert len(faq)>0
assert faq.doc_id.is_unique
assert set(labels.relevant_doc_id).issubset(set(faq.doc_id))
```


## 17. Explain which outputs are deterministic and which would change with a real LLM.

The provided notebooks are deterministic except seeded sampling; hosted LLM outputs can vary by model and settings.


## 18. Write a short README summary of your findings and limitations.

Report data source, experiment, metric, errors, limitations, and next steps.
