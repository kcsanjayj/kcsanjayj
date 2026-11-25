<div align="center">

# Sanjay J

### AI Engineer

LLM systems · Agent orchestration · Retrieval · Model training

<a href="mailto:kcsanjayj@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
<a href="https://linkedin.com/in/kcsanjayj"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
<a href="https://huggingface.co/kcsanjayj"><img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="Hugging Face" /></a>

</div>

---

## About

I build LLM-based systems with an emphasis on reliability. That means validated task planning, review and repair of weak outputs, bounded retries and budgets, and evaluation harnesses that state clearly what they do and do not measure.

I am an early-career engineer. I learn each layer from first principles, build a working system around it, and document its limitations in the repository.

---

## Selected Projects

<table>
<tr>
<td width="72" align="center" valign="top">
  <img src="https://skillicons.dev/icons?i=rust" alt="Rust" width="48" />
</td>
<td valign="top">

### [rapTOR](https://github.com/kcsanjayj/rapTOR) · Multi-agent orchestrator

Plans a request into a validated dependency graph, runs independent tasks in parallel, reviews each result with a critic, and repairs weak output with targeted feedback. Runs offline against a local model or a seeded simulator with fault injection.

- 63 Rust tests and 26 deterministic end-to-end evals, run in CI on Ubuntu and Windows
- Rewritten after a self-review of the first version found eight defects; each now has a regression test
- Four direct dependencies; the plan validator, calculator and parsers are hand-written and bounded

<img src="https://skillicons.dev/icons?i=rust,py,githubactions" alt="Rust, Python, GitHub Actions" />
<img src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white" alt="Ollama" />

</td>
</tr>
<tr>
<td align="center" valign="top">
  <img src="https://skillicons.dev/icons?i=py" alt="Python" width="48" />
</td>
<td valign="top">

### [Spaghetti](https://github.com/kcsanjayj/Spaghetti) · Local document Q&A (RAG)

Answers questions over PDF, DOCX and text files using a model running on the user's own machine, with streaming responses and citations. No cloud services or API keys. [Live UI](https://spaghetti.kcsanjayj.workers.dev) (requires the local backend for chat).

- BM25 retrieval; relevance threshold chosen by ablation, raising abstention from 0.8 to 1.0 with no loss in retrieval
- Rust core for chunking and ranking, with a pure-Python equivalent and parity tests
- 87 tests, a 28-case evaluation harness, and zero axe-core accessibility violations

<img src="https://skillicons.dev/icons?i=py,rust,js,html,css" alt="Python, Rust, JavaScript, HTML, CSS" />
<img src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white" alt="Ollama" />

</td>
</tr>
<tr>
<td align="center" valign="top">
  <img src="https://skillicons.dev/icons?i=pytorch" alt="PyTorch" width="48" />
</td>
<td valign="top">

### [TinyGPT-X](https://github.com/kcsanjayj/TinyGPT-X) · Language model from scratch

A 13.9M-parameter decoder-only transformer implemented in PyTorch and trained from random initialization on a single 6 GB laptop GPU. Published on the [Hugging Face Hub](https://huggingface.co/kcsanjayj/TinyGPT-X) in GPT-2 format.

- Validation perplexity of 6.05 on TinyStories; training completed in about 11 minutes
- Exported logits verified against the native implementation
- Unit tests covering causality, attention equivalence and export parity

<img src="https://skillicons.dev/icons?i=pytorch,py" alt="PyTorch, Python" />
<img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black" alt="Hugging Face" />

</td>
</tr>
</table>

---

## Technical Skills

<table>
<tr>
<td width="150"><b>Languages</b></td>
<td><img src="https://skillicons.dev/icons?i=py,rust,js,html,css" alt="Python, Rust, JavaScript, HTML, CSS" /></td>
</tr>
<tr>
<td><b>ML and LLMs</b></td>
<td>
  <img src="https://skillicons.dev/icons?i=pytorch" alt="PyTorch" />
  <img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="Hugging Face" />
  <img src="https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logo=ollama&logoColor=white" alt="Ollama" />
  <br/>
  <img src="https://img.shields.io/badge/Retrieval-BM25-2F81F7?style=flat-square" alt="BM25 retrieval" />
  <img src="https://img.shields.io/badge/Agent-Orchestration-2F81F7?style=flat-square" alt="Agent orchestration" />
  <img src="https://img.shields.io/badge/LLM-Evaluation-2F81F7?style=flat-square" alt="LLM evaluation" />
</td>
</tr>
<tr>
<td><b>Engineering</b></td>
<td>
  <img src="https://skillicons.dev/icons?i=git,github,githubactions,vscode,powershell" alt="Git, GitHub, GitHub Actions, VS Code, PowerShell" />
  <br/>
  <img src="https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white" alt="pytest" />
  <img src="https://img.shields.io/badge/cargo%20test-000000?style=flat-square&logo=rust&logoColor=white" alt="cargo test" />
  <img src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white" alt="Playwright" />
</td>
</tr>
</table>

---

## How I Work

| Principle | In practice |
|---|---|
| Make failure visible | Retries are counted, partial results are labelled, and call budgets are capped. |
| Test the machinery | Deterministic simulators and fault injection make recovery reproducible. |
| State the limits | Each README says what its evals prove and what they do not. |

---

## Current Work

- Evaluating rapTOR against local models and tuning planner prompts
- Adding embedding-based retrieval to Spaghetti behind the existing ranking interface

---

<div align="center">

### Open to AI and ML engineering roles

<a href="mailto:kcsanjayj@gmail.com"><img src="https://img.shields.io/badge/kcsanjayj@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
<a href="https://linkedin.com/in/kcsanjayj"><img src="https://img.shields.io/badge/linkedin.com/in/kcsanjayj-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>

</div>
