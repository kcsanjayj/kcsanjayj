# Sanjay J

**AI Engineer** · LLM systems, agent orchestration and retrieval

[Email](mailto:kcsanjayj@gmail.com) · [LinkedIn](https://linkedin.com/in/kcsanjayj) · [Hugging Face](https://huggingface.co/kcsanjayj)

---

## About

I build LLM-based systems with a focus on reliability: validated task planning, review and repair of weak outputs, bounded retries and budgets, and evaluation harnesses that state clearly what they do and do not measure.

I am an early-career engineer. My approach is to learn each layer from first principles, build a working system around it, and document its limitations in the repository.

## Selected Projects

### [rapTOR](https://github.com/kcsanjayj/rapTOR): Multi-agent orchestrator
*Rust, Python, Ollama*

Plans a request into a validated dependency graph, runs independent tasks in parallel, reviews each result with a critic, and repairs weak output with targeted feedback. Runs offline against a local model or a seeded simulator with fault injection.

- 63 Rust tests and 26 deterministic end-to-end evals, run in CI on Ubuntu and Windows
- Rewritten after a self-review of a first version that found eight defects; each now has a regression test
- Four direct dependencies; plan validator, calculator and parsers are hand-written and bounded

### [Spaghetti](https://github.com/kcsanjayj/Spaghetti): Local document Q&A (RAG)
*Python, Rust, JavaScript, Ollama*

Answers questions over PDF, DOCX and text files using a model running on the user's own machine, with streaming responses and citations. No cloud services or API keys. [Live UI](https://spaghetti.kcsanjayj.workers.dev) (requires the local backend for chat).

- BM25 retrieval; relevance threshold chosen by ablation, raising abstention from 0.8 to 1.0 with no loss in retrieval
- Rust core for chunking and ranking, with a pure-Python equivalent and parity tests
- 87 tests, a 28-case evaluation harness, and zero axe-core accessibility violations

### [TinyGPT-X](https://github.com/kcsanjayj/TinyGPT-X): Language model from scratch
*PyTorch, Hugging Face*

A 13.9M-parameter decoder-only transformer implemented in PyTorch and trained from random initialization on a single 6 GB laptop GPU. Published on the [Hugging Face Hub](https://huggingface.co/kcsanjayj/TinyGPT-X) in GPT-2 format.

- Validation perplexity of 6.05 on TinyStories, with training completing in about 11 minutes
- Exported logits verified against the native implementation
- Unit tests covering causality, attention equivalence and export parity

## Technical Skills

| Area | Tools |
|---|---|
| Languages | Python, Rust, JavaScript |
| ML and LLMs | PyTorch, Hugging Face, Ollama, retrieval (BM25), agent orchestration, LLM evaluation |
| Engineering | Git, GitHub Actions, pytest, cargo test, Playwright |

## Current Work

- Evaluating rapTOR against local models and tuning planner prompts
- Adding embedding-based retrieval to Spaghetti behind the existing ranking interface

## Contact

Open to AI and ML engineering roles.
[kcsanjayj@gmail.com](mailto:kcsanjayj@gmail.com) · [linkedin.com/in/kcsanjayj](https://linkedin.com/in/kcsanjayj)
