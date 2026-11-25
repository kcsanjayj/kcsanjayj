<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=230&section=header&text=Sanjay%20J&fontSize=72&fontColor=ffffff&fontAlignY=36&animation=fadeIn&desc=AI%20Engineer%20%C2%B7%20Built%20for%20Reliability&descSize=20&descAlignY=58" alt="Sanjay J — AI Engineer" width="100%" />

<a href="https://github.com/kcsanjayj">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1200&color=7DD3FC&center=true&vCenter=true&width=760&height=50&lines=LLM+systems+that+recover+from+failure;Agents+with+budgets%2C+critics+and+repair+loops;Models+trained+from+scratch;Evals+that+state+their+limits" alt="Typing animation" />
</a>

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

```mermaid
flowchart LR
    R([Request]) --> P[Planner<br/>validated DAG]
    P --> A[Task A]
    P --> B[Task B]
    P --> C[Task C]
    A --> K{Critic}
    B --> K
    C --> K
    K -- weak output --> F[Targeted feedback]
    F -.repair.-> A
    K -- accepted --> O([Result<br/>retries counted])
    style P fill:#131c2e,stroke:#7dd3fc,color:#e6edf7
    style K fill:#131c2e,stroke:#a78bfa,color:#e6edf7
    style O fill:#0f2e24,stroke:#34d399,color:#e6edf7
    style F fill:#2e1330,stroke:#f0abfc,color:#e6edf7
```

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

<a href="mailto:kcsanjayj@gmail.com">kcsanjayj@gmail.com</a> · <a href="https://linkedin.com/in/kcsanjayj">linkedin.com/in/kcsanjayj</a>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=120&section=footer&animation=fadeIn" alt="" width="100%" />

</div>
