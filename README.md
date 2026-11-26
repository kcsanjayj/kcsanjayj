<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=220&section=header&text=Sanjay%20J&fontSize=72&fontColor=ffffff&fontAlignY=38&animation=fadeIn&desc=AI%20Engineer%20%C2%B7%20LLM%20systems%20%C2%B7%20Agents%20%C2%B7%20Models%20from%20scratch&descSize=18&descAlignY=60" alt="Sanjay J, AI Engineer" width="100%" />

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=24&pause=1400&color=F87171&center=true&vCenter=true&width=820&height=50&lines=Most+LLM+systems+fail+silently.;Mine+fail+honestly.;Retries+counted.+Partials+labelled.+Budgets+capped." alt="Most LLM systems fail silently. Mine fail honestly." />

<br/>

<a href="mailto:kcsanjayj@gmail.com"><img src="https://img.shields.io/badge/Hire_me-0b1020?style=for-the-badge&logo=gmail&logoColor=f0abfc" alt="Email" /></a>
<a href="https://linkedin.com/in/kcsanjayj"><img src="https://img.shields.io/badge/LinkedIn-0b1020?style=for-the-badge&logo=linkedin&logoColor=7dd3fc" alt="LinkedIn" /></a>
<a href="https://huggingface.co/kcsanjayj"><img src="https://img.shields.io/badge/Hugging_Face-0b1020?style=for-the-badge&logo=huggingface&logoColor=FFD21E" alt="Hugging Face" /></a>

</div>

<br/>

## 👋 Hi, I'm Sanjay

Early-career AI engineer. I build LLM systems, agents and models **end to end, then test them until I know exactly where they break.**

A wrong answer is normal. A system that is wrong **and looks fine** is the real risk, so I make failure visible and bounded.

<div align="center">

| 🦀 **63 + 6** | 🧪 **26** | 🍝 **87** | 🧠 **13.9M** | 🪶 **4** |
|:---:|:---:|:---:|:---:|:---:|
| Rust + Python tests<br/>in rapTOR | deterministic<br/>agent evals | tests in<br/>Spaghetti | params, trained<br/>from scratch | direct Rust<br/>dependencies |

</div>

<br/>

## 🚀 Projects

<table>
<tr>
<td width="33%" valign="top">

### 🦀 rapTOR
**Multi-agent orchestrator that fails honestly**

Plans a request into a validated dependency graph, runs tasks in parallel, and has a critic review and repair every result.

🔹 Found **8 defects in my own v1**, fixed all, gave each a regression test
🔹 Seeded fault injection makes recovery reproducible
🔹 Hard call budgets, counted retries, labelled partials

`Rust` `Python` `Ollama`

**[Repo →](https://github.com/kcsanjayj/rapTOR)**

</td>
<td width="33%" valign="top">

### 🍝 Spaghetti
**Private Q&A over your own documents**

Streaming chat with citations over PDFs and DOCX. Runs on your laptop. No cloud, no accounts, no API keys.

🔹 Relevance filter picked by ablation: **abstention 0.8 → 1.0**, no retrieval loss
🔹 Rust core with a Python twin and parity tests
🔹 19 browser E2E checks, **0 accessibility violations**

`Python` `Rust` `JavaScript`

**[Repo →](https://github.com/kcsanjayj/Spaghetti)** · **[Live UI →](https://spaghetti.kcsanjayj.workers.dev)**

</td>
<td width="33%" valign="top">

### 🧠 TinyGPT-X
**A GPT built from nothing**

Transformer, tokenizer and training loop written by hand. Trained from random init on one 6 GB laptop GPU. No pretrained weights.

🔹 Val. perplexity **6.05** in **11.3 min**
🔹 Export to Hugging Face is checked: logits must match the native model
🔹 Every README number is generated from the run

`PyTorch` `Hugging Face`

**[Repo →](https://github.com/kcsanjayj/TinyGPT-X)** · **[Model →](https://huggingface.co/kcsanjayj/TinyGPT-X)**

</td>
</tr>
</table>

<br/>

## 🔴 Silent failure vs 🟢 how I build it

| Situation | 🔴 Typical demo | 🟢 Mine |
|---|---|---|
| Weak model output | Shipped as if fine | Critic reviews it, repairs with targeted feedback |
| Transient errors | Crash, or invisible retry | Backoff, and every retry is counted |
| A task dies | Answer looks complete anyway | Dependents skipped, result labelled partial |
| Cost | Unbounded | Hard call budget plus a deadline |
| Eval numbers | Quoted without context | Each README says what they don't prove |

<br/>

## 💼 What I bring

- **Systems:** concurrent schedulers, DAG validation and bounded tools in Rust
- **Models:** transformers, tokenizers, training and evaluation in PyTorch
- **Retrieval:** BM25 pipelines, tuned by ablation instead of guesswork
- **Reliability:** fault injection, budgets, regression tests for every defect found
- **Shipping:** CI on Ubuntu and Windows, strict linting, accessibility and security checks
- **Honesty:** every repo has a limitations section. You hear it from me first

<br/>

<div align="center">

<img src="https://skillicons.dev/icons?i=py,rust,pytorch,js,html,css,git,github,githubactions,vscode,powershell&perline=11" alt="Python, Rust, PyTorch, JavaScript, HTML, CSS, Git, GitHub, GitHub Actions, VS Code, PowerShell" />

<br/>

<img src="https://img.shields.io/badge/Ollama-0b1020?style=flat-square&logo=ollama&logoColor=white" alt="Ollama" />
<img src="https://img.shields.io/badge/Hugging_Face-0b1020?style=flat-square&logo=huggingface&logoColor=FFD21E" alt="Hugging Face" />
<img src="https://img.shields.io/badge/pytest-0b1020?style=flat-square&logo=pytest&logoColor=0A9EDC" alt="pytest" />
<img src="https://img.shields.io/badge/Playwright-0b1020?style=flat-square&logo=playwright&logoColor=2EAD33" alt="Playwright" />
<img src="https://img.shields.io/badge/Agent-orchestration-0b1020?style=flat-square" alt="Agent orchestration" />
<img src="https://img.shields.io/badge/LLM-evaluation-0b1020?style=flat-square" alt="LLM evaluation" />

</div>

<br/>

## 🔭 Now

- Running rapTOR against real local models and tuning planner prompts
- Adding embedding-based retrieval to Spaghetti behind its existing ranking interface

<br/>

## 🤝 Let's talk

I'm looking for **AI and ML engineering roles** where reliability matters and someone would rather hear about a limitation from me than find it in production.

<div align="center">

<a href="mailto:kcsanjayj@gmail.com"><img src="https://img.shields.io/badge/kcsanjayj@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
<a href="https://linkedin.com/in/kcsanjayj"><img src="https://img.shields.io/badge/linkedin.com/in/kcsanjayj-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>

<br/><br/>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=16&pause=1000&color=34D399&center=true&vCenter=true&width=520&height=30&lines=Fail+honestly.+Recover+on+purpose." alt="Fail honestly. Recover on purpose." />

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=100&section=footer&animation=fadeIn" alt="" width="100%" />

</div>
