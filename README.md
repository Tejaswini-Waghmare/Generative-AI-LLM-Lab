# Generative AI & LLM Lab

Ten educational modules on LLM concepts, prompting, embeddings, retrieval, RAG, evaluation, agents, safety, applications, and an end-to-end helpdesk assistant.

**Important:** All demonstrations run offline using local, deterministic baselines. TF-IDF is a lexical vector baseline, **not** a pretrained neural embedding or a generative LLM. The RAG examples return retrieved source text rather than generating new text. The agent examples simulate orchestration; no external tools are executed. These boundaries are intentional for reproducibility and zero API cost.

## Quick start

```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
jupyter lab
```

If Jupyter is missing, install `jupyterlab` or upload the notebooks to Colab. Run from the repository root so relative `data/` paths resolve; in Colab upload both CSV files to a `data` directory.

## Study order

- [01_LLM_Fundamentals](./01_LLM_Fundamentals/README.md): LLM Fundamentals
- [02_Prompt_Engineering](./02_Prompt_Engineering/README.md): Prompt Engineering
- [03_Embeddings_and_Semantic_Search](./03_Embeddings_and_Semantic_Search/README.md): Embeddings and Semantic Search
- [04_Vector_Databases](./04_Vector_Databases/README.md): Vector Databases
- [05_RAG_Pipelines](./05_RAG_Pipelines/README.md): Retrieval-Augmented Generation
- [06_LLM_Evaluation](./06_LLM_Evaluation/README.md): LLM Evaluation
- [07_AI_Agents_and_Tools](./07_AI_Agents_and_Tools/README.md): AI Agents and Tools
- [08_Safety_and_Guardrails](./08_Safety_and_Guardrails/README.md): Safety and Guardrails
- [09_LLM_Apps_and_APIs](./09_LLM_Apps_and_APIs/README.md): LLM Apps and APIs
- [10_End_to_End_GenAI_Project](./10_End_to_End_GenAI_Project/README.md): End-to-End GenAI Project

All data are synthetic. Practice answers are learning references, not production claims.
