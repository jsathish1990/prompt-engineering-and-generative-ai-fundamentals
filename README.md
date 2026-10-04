# Prompt Engineering and Generative AI Notebooks

Notebooks and datasets for the Udemy course Prompt Engineering and Generative AI - Fundamentals: https://www.udemy.com/course/prompt-engineering-and-generative-ai-fundamentals

Repository: https://github.com/jsathish1990/prompt-engineering-and-generative-ai-fundamentals

All the analysis in the Jupyter notebooks in this repository is from the references listed below and in the References section of each notebook.

The notebooks were vetted with Claude Code.

## Notebooks

| Section | Segment | Notebook |
|---|---|---|
| 1 - Prompt Engineering Fundamentals | 1–4: Definition, best practices, streaming, temperature and tokens, zero-shot, few-shot, chain-of-thought | `Set_up_Gemini+(1).ipynb` |
| 1 - Prompt Engineering Fundamentals | Setting up the GPT model | `Set_up_OpenAI.ipynb` |
| 1 - Prompt Engineering Fundamentals | Tree-of-Thoughts, 4x4 Sudoku | `4x4_example_OpenAI.ipynb` |
| 2 - Retrieval Augmented Generation | 1: RAG on a CSV file | `Retrieval_Augmented_Generation_1.ipynb` |
| 2 - Retrieval Augmented Generation | 2: Arxiv loader, FAISS, conversational retrieval chain | `Arxiv_Loader_RAG_.ipynb` |
| 2 - Retrieval Augmented Generation | 3: Evaluation with RAGAS | `PyPDF_RAG_with_RAGAS.ipynb` |
| 2 - Retrieval Augmented Generation | 4: LangSmith with RAGAS | `RAGAS_langsmith.ipynb` |
| 2 - Retrieval Augmented Generation | 5: Gemini embeddings and document search | `Document_Q_A_Gemini.ipynb` |
| 3 - LLM Fine-tuning | 1: Prompting vs fine-tuning | `Finetuning_vs_Prompting.ipynb` |
| 3 - LLM Fine-tuning | 2–3: Types of fine-tuning, EDA, task-specific fine-tuning | `Fine_tuning_an_LLM_.ipynb` |
| 4 - Guardrails for LLMs | 1: Guardrails from OpenAI | `Topical_guardrail.ipynb` |
| 4 - Guardrails for LLMs | 2: GuardrailsAI, extracting information from text | `GuardrailsAI_extracting_text.ipynb` |
| 4 - Guardrails for LLMs | 3: GuardrailsAI, generating structured data | `GuardrailsAI_generating_structured_data.ipynb` |
| 4 - Guardrails for LLMs | 3: GuardrailsAI with a chat model | `Guardrails_with_ChatModel.ipynb` |

## Datasets and documents

* `data_QA_.csv` (Section 2 - Retrieval_Augmented_Generation_1). Questions with Wikipedia excerpts, from the Kaggle dataset "Science exam - use sci or not sci questions?" by Radek Osmulski: https://www.kaggle.com/datasets/radek1/sci-or-not-sci-hypthesis-testing-pack. Wikipedia text is available under the CC BY-SA license.
* Sentiments Dataset (381 Classes) (Section 3 - Fine_tuning_an_LLM_). Loaded from Hugging Face when the notebook runs. Salieh, F. G. (2023). Apache 2.0 license. https://huggingface.co/datasets/Falah/sentiments-dataset-381-classes
* `ref_.pdf` (Section 2 - PyPDF_RAG_with_RAGAS). Not included in this repository. Download the paper from arXiv and save it as `ref_.pdf`. Roberson, R., Kaki, G., & Trivedi, A. (2024). Analyzing the Effectiveness of Large Language Models on Text-to-SQL Synthesis. arXiv:2401.12379. https://arxiv.org/abs/2401.12379
* `Gemma_Google.pdf` (Section 4 - Guardrails_with_ChatModel). Not included in this repository. Save the Google blog post as a PDF named `Gemma_Google.pdf`. Google (2024). Gemma: Google introduces new state-of-the-art open models. https://blog.google/technology/developers/gemma-open-models/
* Arxiv_Loader_RAG_ loads papers directly from arXiv when the notebook runs.

## Running the notebooks

The notebooks were written for Google Colab. See [How_to_run_the_notebooks.pdf](How_to_run_the_notebooks.pdf) for the full steps. In short:

* Add your API keys (`OPENAI_API_KEY`, `GOOGLE_API_KEY`, `HF_TOKEN`) under the key icon (Secrets) in Colab's left sidebar.
* Three notebooks read data from Google Drive (`/content/drive/MyDrive/...`). Upload `data_QA_.csv`, `ref_.pdf` and `Gemma_Google.pdf` to the top level of your Google Drive, or change the path to the file name and skip the `drive.mount(...)` cell.
* Use a GPU runtime for the Section 3 notebooks.
* Each notebook installs pinned library versions in its first cell. If Colab asks to restart the session after the install cell, restart and run all again.

Updates in October 2026: library versions were pinned, and retired models were replaced (OpenAI gpt-3.5-turbo, gpt-3.5-turbo-instruct and gpt-4 now use `gpt-4o-mini`; Gemini-Pro now uses `gemini-3.1-flash-lite`). Responses will not exactly match the outputs saved in the notebooks.

## References

### Papers

* Yao, S., et al. (2023). Tree of Thoughts: Deliberate Problem Solving with Large Language Models. arXiv:2305.10601.
* Long, J. (2023). Large Language Model Guided Tree-of-Thought. arXiv:2305.08291.
* Wei, J., et al. (2022). Chain-of-Thought Prompting Elicits Reasoning in Large Language Models. Advances in Neural Information Processing Systems 35, 24824–24837.
* Ekin, S. (2023). Prompt Engineering for ChatGPT: A Quick Guide to Techniques, Tips, and Best Practices. Authorea Preprints.
* Hadi, M. U., et al. (2023). A Survey on Large Language Models: Applications, Challenges, Limitations, and Practical Usage. Authorea Preprints.
* Lewis, P., et al. (2020). Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks. Advances in Neural Information Processing Systems 33, 9459–9474.
* Es, S., et al. (2023). RAGAS: Automated Evaluation of Retrieval Augmented Generation. arXiv:2309.15217.
* Roberson, R., Kaki, G., & Trivedi, A. (2024). Analyzing the Effectiveness of Large Language Models on Text-to-SQL Synthesis. arXiv:2401.12379.
* Hu, Z., et al. (2023). LLM-Adapters: An Adapter Family for Parameter-Efficient Fine-Tuning of Large Language Models. arXiv:2304.01933.
* Xu, L., et al. (2023). Parameter-Efficient Fine-Tuning Methods for Pretrained Language Models: A Critical Review and Assessment. arXiv:2312.12148. https://doi.org/10.48550/arXiv.2312.12148
* Dong, Y., et al. (2024). Building Guardrails for Large Language Models. arXiv:2402.01822.
* Chase, H. (2022). LangChain. https://github.com/hwchase17/langchain

### Section 1 - Prompt Engineering Fundamentals

* Prompt Engineering Guide: https://www.promptingguide.ai/, https://www.promptingguide.ai/techniques/fewshot, https://www.promptingguide.ai/techniques/tot
* Hugging Face documentation: https://huggingface.co/docs
* LangChain cookbook: https://python.langchain.com/cookbook

### Section 2 - Retrieval Augmented Generation

* Prompt Engineering Guide, RAG: https://www.promptingguide.ai/techniques/rag
* AWS, What is RAG: https://aws.amazon.com/what-is/retrieval-augmented-generation/
* DataCamp, What is RAG: https://www.datacamp.com/blog/what-is-retrieval-augmented-generation-rag
* Neum AI blog: https://www.neum.ai/post/
* Deci AI: https://deci.ai/
* Towards Data Science, 4 Ways of Question Answering in LangChain: https://towardsdatascience.com/4-ways-of-question-answering-in-langchain-188c6707cc5a
* Dev Genius, Tree of Thoughts implementation to solve the Game of 24: https://blog.devgenius.io/tree-of-thoughts-implementation-to-solve-the-game-of-24-13fb1fa2034b
* LangChain documentation: document loaders, ArxivLoader, MergedDataLoader, text splitters, OpenAI embeddings, FAISS, vector stores, ConversationalRetrievalChain (https://python.langchain.com/docs)
* RAGAS documentation, LangChain integration: https://docs.ragas.io/en/latest/howtos/integrations/langchain.html
* LangChain blog, Evaluating RAG pipelines with Ragas + LangSmith: https://blog.langchain.dev/evaluating-rag-pipelines-with-ragas-langsmith/
* Sentence Transformers all-mpnet-base-v2: https://huggingface.co/sentence-transformers/all-mpnet-base-v2
* Google AI, Document search with embeddings: https://ai.google.dev/examples/doc_search_emb

### Section 3 - LLM Fine-tuning

* Towards Data Science, Fine-tuning Large Language Models (LLMs): https://towardsdatascience.com/fine-tuning-large-language-models-llms-23473d763b91
* Turing, Fine-tuning large language models: https://www.turing.com/resources/finetuning-large-language-models
* Hugging Face Transformers documentation, prompting: https://huggingface.co/docs/transformers/main/tasks/prompting
* Hugging Face Transformers glossary: https://huggingface.co/docs/transformers/en/glossary
* Hugging Face AutoTokenizer: https://huggingface.co/transformers/v3.0.2/model_doc/auto.html

### Section 4 - Guardrails for LLMs

* OpenAI Cookbook, How to implement LLM guardrails: https://cookbook.openai.com/examples/how_to_use_guardrails
* Guardrails AI: https://github.com/guardrails-ai/guardrails, https://www.guardrailsai.com/docs/guardrails_ai/getting_started, https://www.guardrailsai.com/docs/examples/generate_structured_data
* Attri AI blog: https://attri.ai/blog
* Meta Llama Guard: https://huggingface.co/meta-llama/LlamaGuard-7b

Models used: OpenAI GPT models, Google Gemini models, and Hugging Face models (bert-base-cased, Mistral-7B, Falcon-7B-Instruct, Flan-T5, DeepSeek-Math-7B-Instruct), each under its own license.
