<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=220&section=header&text=Sanjay%20J&fontSize=70&fontColor=ffffff&fontAlignY=38&animation=fadeIn&desc=AI%20Engineer&descSize=20&descAlignY=60" alt="Sanjay J — AI Engineer" width="100%" />

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=24&pause=1400&color=F87171&center=true&vCenter=true&width=820&height=50&lines=Most+LLM+systems+fail+silently.;Mine+fail+honestly.;Retries+counted.+Partials+labelled.+Budgets+capped." alt="Most LLM systems fail silently. Mine fail honestly." />

<br/>

<a href="mailto:kcsanjayj@gmail.com"><img src="https://img.shields.io/badge/Email-0b1020?style=for-the-badge&logo=gmail&logoColor=f0abfc" alt="Email" /></a>
<a href="https://linkedin.com/in/kcsanjayj"><img src="https://img.shields.io/badge/LinkedIn-0b1020?style=for-the-badge&logo=linkedin&logoColor=7dd3fc" alt="LinkedIn" /></a>
<a href="https://huggingface.co/kcsanjayj"><img src="https://img.shields.io/badge/Hugging_Face-0b1020?style=for-the-badge&logo=huggingface&logoColor=FFD21E" alt="Hugging Face" /></a>

</div>

<br/>

## 🎯 The idea

A model that is wrong is normal. A system that is wrong **and looks fine** is the real problem.

I build LLM systems where failure is a first-class, visible outcome: validated plans, critics that review output, bounded retries and budgets, and evals that say plainly what they do *and don't* prove.

I'm early-career, and I learn each layer from first principles: build it, test it, document its limits.

<br/>

## 🔴 Silent failure vs 🟢 Honest failure

| Situation | 🔴 Typical system | 🟢 How I build it |
|---|---|---|
| Weak model output | Shipped as if it were fine | A critic reviews it, then repairs it with targeted feedback |
| Retries | Happen invisibly | Counted and reported |
| Partial results | Presented as complete | Labelled as partial |
| Cost and calls | Unbounded | Budgets capped |
| Evals | "It works" | Each README states what the evals prove, and what they don't |
| Recovery | Hard to reproduce | Deterministic simulators and fault injection make it repeatable |

```mermaid
flowchart LR
    W([Weak output]) --> S1[Silent system]
    S1 --> S2[/Looks fine/]
    S2 --> S3([Wrong answer, no signal])
    W --> H1{Critic}
    H1 -- repair --> H2[Targeted feedback]
    H2 --> H1
    H1 -- accepted --> H3([Result + retries counted])
    H1 -- budget hit --> H4([Partial, labelled as partial])
    style S1 fill:#2b1215,stroke:#f87171,color:#fecaca
    style S2 fill:#2b1215,stroke:#f87171,color:#fecaca
    style S3 fill:#2b1215,stroke:#f87171,color:#fecaca
    style H1 fill:#131c2e,stroke:#a78bfa,color:#e6edf7
    style H2 fill:#2e1330,stroke:#f0abfc,color:#e6edf7
    style H3 fill:#0f2e24,stroke:#34d399,color:#d1fae5
    style H4 fill:#2e2a10,stroke:#fbbf24,color:#fef3c7
```

<details>
<summary><b>What "fails honestly" looks like (illustrative sketch)</b></summary>

```text
task: summarise_report      status: PARTIAL
  attempts ........ 3 / 3   (budget exhausted)
  critic verdict .. weak: missing citation for claim 2
  output .......... returned, labelled partial
  note ............ not retried further; no silent fallback
```

</details>

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

<a href="mailto:kcsanjayj@gmail.com">kcsanjayj@gmail.com</a> · <a href="https://linkedin.com/in/kcsanjayj">linkedin.com/in/kcsanjayj</a>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=16&pause=1000&color=34D399&center=true&vCenter=true&width=520&height=30&lines=Fail+honestly.+Recover+on+purpose." alt="Fail honestly. Recover on purpose." />

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=110&section=footer&animation=fadeIn" alt="" width="100%" />

</div>
