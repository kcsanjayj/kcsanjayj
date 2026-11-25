<div align="center">

<img src="assets/hero.svg" alt="Sanjay J — AI Engineer" width="100%" />

<br/>

<a href="mailto:kcsanjayj@gmail.com"><img src="https://img.shields.io/badge/Email-0b1020?style=for-the-badge&logo=gmail&logoColor=f0abfc" alt="Email" /></a>
<a href="https://linkedin.com/in/kcsanjayj"><img src="https://img.shields.io/badge/LinkedIn-0b1020?style=for-the-badge&logo=linkedin&logoColor=7dd3fc" alt="LinkedIn" /></a>
<a href="https://huggingface.co/kcsanjayj"><img src="https://img.shields.io/badge/Hugging_Face-0b1020?style=for-the-badge&logo=huggingface&logoColor=FFD21E" alt="Hugging Face" /></a>

</div>

<br/>

## ⚡ In one breath

I build LLM systems that **fail visibly and recover on purpose**: validated plans, critics that review output, bounded retries and budgets, and evals that say plainly what they do *and don't* prove.

Early-career, and I learn each layer from first principles: build it, test it, document its limits.

<br/>

## 📊 By the numbers

<div align="center">

| **63** | **26** | **87** | **13.9M** | **6.05** |
|:---:|:---:|:---:|:---:|:---:|
| Rust tests in rapTOR | deterministic e2e evals | tests in Spaghetti | params, trained from scratch | val. perplexity on TinyStories |

</div>

<br/>

## 🚀 Selected Projects

### 🦀 [rapTOR](https://github.com/kcsanjayj/rapTOR) · Multi-agent orchestrator

<div align="center"><img src="assets/flow.svg" alt="rapTOR pipeline: request, planner, parallel tasks, critic with repair loop, result" width="100%" /></div>

Plans a request into a validated dependency graph, runs independent tasks in parallel, reviews each result with a critic, and repairs weak output with targeted feedback. Runs fully offline against a local model or a seeded simulator with fault injection.

- ✅ 63 Rust tests and 26 deterministic end-to-end evals, in CI on Ubuntu and Windows
- 🔁 Rewritten after a self-review found eight defects; each now has a regression test
- 🪶 Four direct dependencies; plan validator, calculator and parsers are hand-written and bounded

`Rust` `Python` `GitHub Actions` `Ollama`

<br/>

### 📚 [Spaghetti](https://github.com/kcsanjayj/Spaghetti) · Local document Q&A (RAG)

Ask questions over PDF, DOCX and text files using a model on your own machine: streaming answers with citations, no cloud, no API keys. [Live UI](https://spaghetti.kcsanjayj.workers.dev) *(chat needs the local backend)*.

- 🎯 Relevance threshold chosen by ablation: abstention up from 0.8 to 1.0, no loss in retrieval
- ⚙️ Rust core for chunking and ranking, with a pure-Python twin and parity tests
- ♿ 87 tests, a 28-case eval harness, zero axe-core accessibility violations

`Python` `Rust` `JavaScript` `BM25` `Ollama`

<br/>

### 🧠 [TinyGPT-X](https://github.com/kcsanjayj/TinyGPT-X) · A language model from scratch

A 13.9M-parameter decoder-only transformer in PyTorch, trained from random init on a single 6 GB laptop GPU in about 11 minutes. Published on the [Hugging Face Hub](https://huggingface.co/kcsanjayj/TinyGPT-X) in GPT-2 format.

- 📉 Validation perplexity 6.05 on TinyStories
- 🔬 Exported logits verified against the native implementation
- 🧪 Tests for causality, attention equivalence and export parity

`PyTorch` `Python` `Hugging Face`

<br/>

## 🧭 How I work

| Principle | In practice |
|---|---|
| 👁️ **Make failure visible** | Retries are counted, partial results labelled, call budgets capped. |
| 🧪 **Test the machinery** | Simulators and fault injection make recovery reproducible. |
| 📏 **State the limits** | Every README says what its evals prove, and what they don't. |

<br/>

## 🛠️ Toolbox

<div align="center">

<img src="https://skillicons.dev/icons?i=py,rust,pytorch,js,html,css,git,github,githubactions,vscode,powershell&perline=11" alt="Python, Rust, PyTorch, JavaScript, HTML, CSS, Git, GitHub, GitHub Actions, VS Code, PowerShell" />

<img src="https://img.shields.io/badge/Ollama-0b1020?style=flat-square&logo=ollama&logoColor=white" alt="Ollama" />
<img src="https://img.shields.io/badge/Hugging_Face-0b1020?style=flat-square&logo=huggingface&logoColor=FFD21E" alt="Hugging Face" />
<img src="https://img.shields.io/badge/pytest-0b1020?style=flat-square&logo=pytest&logoColor=0A9EDC" alt="pytest" />
<img src="https://img.shields.io/badge/Playwright-0b1020?style=flat-square&logo=playwright&logoColor=2EAD33" alt="Playwright" />
<img src="https://img.shields.io/badge/BM25-retrieval-0b1020?style=flat-square" alt="BM25 retrieval" />
<img src="https://img.shields.io/badge/LLM-evaluation-0b1020?style=flat-square" alt="LLM evaluation" />

</div>

<br/>

## 🔭 Currently

- Evaluating rapTOR against local models and tuning planner prompts
- Adding embedding-based retrieval to Spaghetti behind its existing ranking interface

<br/>

<div align="center">

### 🟢 Open to AI and ML engineering roles

<img src="assets/footer.svg" alt="Let's build something reliable." width="100%" />

<a href="mailto:kcsanjayj@gmail.com">kcsanjayj@gmail.com</a> · <a href="https://linkedin.com/in/kcsanjayj">linkedin.com/in/kcsanjayj</a>

</div>
