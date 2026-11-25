<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=240&section=header&text=Sanjay%20J&fontSize=76&fontColor=ffffff&fontAlignY=38&animation=fadeIn&desc=AI%20Engineer%20%C2%B7%20LLM%20systems%20%C2%B7%20Agents%20%C2%B7%20Models%20from%20scratch&descSize=18&descAlignY=60" alt="Sanjay J, AI Engineer" width="100%" />

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=25&pause=1400&color=F87171&center=true&vCenter=true&width=820&height=52&lines=Most+LLM+systems+fail+silently.;Mine+fail+honestly.;Retries+counted.+Partials+labelled.+Budgets+capped.;Evals+that+say+what+they+don%27t+prove." alt="Most LLM systems fail silently. Mine fail honestly." />

<br/>

<a href="mailto:kcsanjayj@gmail.com"><img src="https://img.shields.io/badge/Hire_me-0b1020?style=for-the-badge&logo=gmail&logoColor=f0abfc" alt="Email" /></a>
<a href="https://linkedin.com/in/kcsanjayj"><img src="https://img.shields.io/badge/LinkedIn-0b1020?style=for-the-badge&logo=linkedin&logoColor=7dd3fc" alt="LinkedIn" /></a>
<a href="https://huggingface.co/kcsanjayj"><img src="https://img.shields.io/badge/Hugging_Face-0b1020?style=for-the-badge&logo=huggingface&logoColor=FFD21E" alt="Hugging Face" /></a>

</div>

<br/>

## 👋 Hi, I'm Sanjay

I'm an early-career AI engineer, and I'm upfront about that. I make up for it by **building every layer myself, testing it, and writing down where it breaks.**

A wrong model is normal. A system that is wrong **and looks fine** is the real risk. So I build LLM systems where failure is visible and bounded:

- 🔢 **Retries are counted**, not hidden
- 🏷️ **Partial results are labelled** as partial
- 💸 **Budgets are capped**, so nothing runs away
- 🧪 **Evals say what they don't prove**, not just what they do

<br/>

## 🔴 Silent failure vs 🟢 Honest failure

| Situation | 🔴 Typical demo | 🟢 How I build it |
|---|---|---|
| Weak model output | Shipped as if fine | A critic reviews it and repairs it with targeted feedback |
| Transient errors | Crash, or retry invisibly | Only transient errors retry, with backoff, and every retry is counted |
| A task dies | Answer looks complete anyway | Dependents are skipped and the result is labelled partial |
| Cost and calls | Unbounded | Hard call budget plus a deadline |
| "It works" | One happy-path demo | Deterministic simulator with seeded fault injection |
| Eval numbers | Quoted without context | Each README states what they prove, and what they don't |

<br/>

## 🚀 What I've built

<table>
<tr>
<td width="33%" valign="top">

### 🦀 rapTOR
**Agents that fail honestly**

Plans a request into a validated dependency graph, runs tasks in parallel, and has a critic review and repair every result.

`Rust` `Python` `Ollama`

**[View repo →](https://github.com/kcsanjayj/rapTOR)**

</td>
<td width="33%" valign="top">

### 🍝 Spaghetti
**Private document Q&A**

Chat with your own PDFs and DOCX on your own laptop. Streaming answers with citations. No cloud, no accounts, no API keys.

`Python` `Rust` `JavaScript`

**[View repo →](https://github.com/kcsanjayj/Spaghetti)** · **[Live UI →](https://spaghetti.kcsanjayj.workers.dev)**

</td>
<td width="33%" valign="top">

### 🧠 TinyGPT-X
**A GPT from scratch**

A 13.9M-parameter transformer in PyTorch, trained from random initialization on one 6 GB laptop GPU. No pretrained weights.

`PyTorch` `Hugging Face`

**[View repo →](https://github.com/kcsanjayj/TinyGPT-X)** · **[Model →](https://huggingface.co/kcsanjayj/TinyGPT-X)**

</td>
</tr>
</table>

<br/>

### 🦀 rapTOR · A multi-agent orchestrator you can trust to fail honestly

```mermaid
flowchart LR
    R([Request]) --> P[Plan<br/>JSON DAG]
    P --> V{Validate}
    V -- bad plan --> P
    V -- ok --> T[Run ready tasks<br/>in parallel]
    T --> C{Critic<br/>score 0-10}
    C -- below 7 --> F[Repair with feedback<br/>max 2 rounds]
    F --> C
    C -- good --> D[Release dependents]
    D --> T
    D --> S([Synthesize<br/>answer + metrics])
    style V fill:#131c2e,stroke:#7dd3fc,color:#e6edf7
    style C fill:#131c2e,stroke:#a78bfa,color:#e6edf7
    style F fill:#2e1330,stroke:#f0abfc,color:#e6edf7
    style S fill:#0f2e24,stroke:#34d399,color:#d1fae5
```

My first version looked fine and was broken: tasks never received their dependencies' outputs, the critic skipped the last step, and `9**9**9` hung the calculator. I reviewed it honestly, rewrote it, and **all 8 defects now have regression tests that fail if they return.**

- ✅ **63 Rust tests, 6 Python tests and 26 deterministic end-to-end evals**, in CI on Ubuntu and Windows
- 🧪 **Seeded fault injection** (transient 503s, weak drafts, permanent failures) makes recovery reproducible
- 🪶 **4 direct Rust dependencies.** The plan validator, calculator and parsers are hand-written and bounded
- 🔒 **Local only by design:** remote model endpoints are rejected

<br/>

### 🍝 Spaghetti · Chat with your documents, privately

Five small "agents" plan, search, write, check and serve each answer using a model running locally through Ollama.

- 🎯 **Measured, not guessed.** The relevance filter was chosen from an ablation: **abstention 0.8 → 1.0 with no loss in retrieval**
- ⚙️ **Rust core with a Python twin.** Chunking, BM25 and ranking are in Rust, with a pure-Python equivalent and parity tests, so Rust stays optional
- 💬 **Streaming chat** with stop, regenerate, citations and saved history
- 📊 **87 tests, a 28-case evaluation harness with CI gates, 19 browser end-to-end checks, and 0 axe-core accessibility violations** in light and dark
- ⚡ **Worst frame 17 ms while streaming** (headless Chromium)
- 🔐 **Security by allowlist:** strict Content-Security-Policy, exact-origin CORS, model downloads limited to a built-in menu

> **Honest note from the repo:** the eval mock is extractive, so its perfect scores prove plumbing and retrieval, not model quality. I haven't verified a real Ollama install, real model speed or Safari. It uses BM25, not embeddings, so synonyms are a known limitation with two eval cases documenting it on purpose.

<br/>

### 🧠 TinyGPT-X · A language model, built from nothing

```mermaid
flowchart LR
    D[TinyStories<br/>subset] --> T[Byte-level BPE<br/>8,192 tokens]
    T --> M[Hand-written<br/>transformer]
    M --> R[Train<br/>6,000 steps]
    R --> E[Evaluate]
    E --> X[Export to<br/>GPT-2 format]
    X --> V{Logits match<br/>native model?}
    V -- no --> F([Script fails])
    V -- yes --> H([Hugging Face Hub])
    style V fill:#131c2e,stroke:#a78bfa,color:#e6edf7
    style F fill:#2b1215,stroke:#f87171,color:#fecaca
    style H fill:#0f2e24,stroke:#34d399,color:#d1fae5
```

<div align="center">

| **13.9M** | **6.05** | **11.3 min** | **2.02 GB** | **56.2%** |
|:---:|:---:|:---:|:---:|:---:|
| parameters | best val. perplexity | training time | peak GPU memory | next-token top-1 |

</div>

- 🏗️ **Transformer, tokenizer and training loop written by hand.** The vocabulary is learned from the training text, with no pretrained weights anywhere
- 🔬 **Verified, not assumed:** tests prove causality, hand-written attention equal to the fused kernel, and CPU-vs-GPU agreement
- 📦 **Export is checked.** The exported GPT-2-format model's logits are compared to the native model, and the script fails if they differ
- 🧾 **Every number in the README is generated** from a real run by a script, not typed by hand

> **Honest note from the repo:** it only knows simple children's stories. It won't answer questions or follow instructions, and it repeats over longer outputs.

<br/>

## 🧭 How I work

| Principle | In practice |
|---|---|
| 👁️ **Make failure visible** | Retries counted, partials labelled, budgets capped |
| 🧪 **Test the machinery** | Simulators and fault injection turn "it recovered once" into something reproducible |
| 📏 **Measure before tuning** | An ablation changed my threshold. I write the eval harness before trusting a number |
| 🪞 **Review my own work** | I audited my own v1, found 8 defects, and gave each a regression test |
| 🛟 **Keep a fallback** | Every native component has a pure-Python twin and parity tests |
| 📝 **State the limits** | Every README has an "honest limitations" section |

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
<img src="https://img.shields.io/badge/Agent-orchestration-0b1020?style=flat-square" alt="Agent orchestration" />

</div>

<br/>

## 🔭 What I'm working on now

- 🧪 Running rapTOR against real local models and tuning the planner prompts
- 🔎 Adding embedding-based retrieval to Spaghetti behind the existing ranking interface
- 📈 Next for rapTOR: model-graded evals with variance reporting, and per-task timeouts with cancellation

<br/>

## 🤝 Let's talk

I'm looking for **AI and ML engineering roles** where reliability matters and someone would rather hear about a limitation from me than find it in production.

<div align="center">

<a href="mailto:kcsanjayj@gmail.com"><img src="https://img.shields.io/badge/kcsanjayj@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
<a href="https://linkedin.com/in/kcsanjayj"><img src="https://img.shields.io/badge/linkedin.com/in/kcsanjayj-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>

<br/><br/>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=17&pause=1000&color=34D399&center=true&vCenter=true&width=560&height=30&lines=Fail+honestly.+Recover+on+purpose." alt="Fail honestly. Recover on purpose." />

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=110&section=footer&animation=fadeIn" alt="" width="100%" />

</div>
