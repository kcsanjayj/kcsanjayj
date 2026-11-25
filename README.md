<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,100:2f81f7&height=190&section=header&text=Sanjay%20J&fontSize=52&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=AI%20Engineer&descSize=20&descAlignY=60" alt="Sanjay J, AI Engineer" />

<a href="https://github.com/kcsanjayj">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1400&color=2F81F7&center=true&vCenter=true&width=700&lines=Most+agent+demos+fail+silently.+Mine+fail+honestly.;I+trained+a+GPT+from+random+weights+on+a+laptop.;I+built+a+RAG+app+that+never+leaves+your+machine.;Build+it.+Break+it.+Measure+it." alt="Typing intro" />
</a>

<br/><br/>

<a href="mailto:kcsanjayj@gmail.com"><img src="https://img.shields.io/badge/Hire%20me-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
<a href="https://linkedin.com/in/kcsanjayj"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="https://huggingface.co/kcsanjayj"><img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black"/></a>

</div>

---

## ⚡ The pitch

Anyone can make an LLM demo that works once.
I build the part that comes after: **the machinery that keeps it honest when things go wrong.**

Retries that are counted. Bad answers that get caught and repaired. Partial results that are labelled as partial. And every claim in my READMEs is backed by a test or an eval I can show you.

I'm a fresher, so I can't point to years of experience. What I can point to is three repos where I did the work, measured it, and wrote down where it falls short.

---

## 📊 By the numbers

<div align="center">

| 🧪 **63** | ✅ **26** | 🔍 **87** | 🧠 **13.9M** | ⏱️ **~11 min** |
|:---:|:---:|:---:|:---:|:---:|
| Rust tests in rapTOR | deterministic agent evals | tests in Spaghetti | parameters, trained from scratch | to train TinyGPT-X on a laptop GPU |

</div>

---

## 🚀 What I've built

### 🦅 [rapTOR](https://github.com/kcsanjayj/rapTOR)
> **"A multi-agent orchestrator you can actually trust to fail honestly."**

I built a first version, reviewed it honestly, and found **8 silent bugs** hiding behind plausible answers: tasks that never received their dependencies' output, a critic that skipped the last step, a calculator that one prompt could hang forever. Then I rewrote the core in Rust, and each of those bugs now has a regression test that fails if it comes back.

- 🕸️ Plans a request into a validated task graph and runs independent branches in parallel
- 🧑‍⚖️ A critic reviews every result and weak output is repaired with specific feedback
- 💥 A seeded simulator injects 503s, bad drafts and dead tasks, so recovery is reproducible
- 🔒 Runs fully offline, with only 4 direct dependencies

`Rust` `Python` `Ollama`

---

### 🍝 [Spaghetti](https://github.com/kcsanjayj/Spaghetti)
> **"Chat with your own documents, privately, on your own laptop."**

No cloud. No accounts. No API keys. Drop in a PDF or DOCX and ask questions. A small local model answers with citations, and when the documents don't contain the answer, it says so instead of making one up.

- 📉 I tuned the relevance filter with an ablation and not a guess: abstention went **0.8 → 1.0** with no retrieval loss
- 🦀 The fast core is Rust, with a pure-Python twin and parity tests proving they agree
- ♿ 0 accessibility violations, 19 browser end-to-end checks

`Python` `Rust` `JavaScript` `Ollama` · [**▶ Live UI**](https://spaghetti.kcsanjayj.workers.dev)

---

### 🧠 [TinyGPT-X](https://github.com/kcsanjayj/TinyGPT-X)
> **"No pretrained weights. No shortcuts. Just a GPT, from random initialization."**

A decoder-only transformer written by hand in PyTorch and trained on a 6 GB laptop GPU. It reaches a validation perplexity of **6.05** on TinyStories, and then it's published on [Hugging Face](https://huggingface.co/kcsanjayj/TinyGPT-X) in the standard GPT-2 format, with the exported logits verified against my own implementation.

- 📐 Tests prove the attention is causal and that my math matches the fused kernel
- 📈 Every number in the README is generated from the real training run, never typed by hand

`PyTorch` `Hugging Face` `Python`

---

## 🧭 How I work

| | |
|---|---|
| **1. Build it** | Start from first principles, keep dependencies few, and keep the code readable. |
| **2. Break it** | Fault injection, adversarial inputs and a v1 review I wrote against myself. |
| **3. Measure it** | Evals and tests first, and then I say what the numbers do and don't prove. |

---

## 🧰 Toolbox

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"/>
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white"/>
  <br/>
  <img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black"/>
  <img src="https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logo=ollama&logoColor=white"/>
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white"/>
  <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white"/>
</p>

---

## 🤝 Let's talk

Hiring for an AI or ML role, or want to build something where **reliability matters more than the demo?**

📧 [kcsanjayj@gmail.com](mailto:kcsanjayj@gmail.com) · 💼 [linkedin.com/in/kcsanjayj](https://linkedin.com/in/kcsanjayj)

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/kcsanjayj/kcsanjayj/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/kcsanjayj/kcsanjayj/output/github-snake.svg" />
  <img alt="Contribution snake" src="https://raw.githubusercontent.com/kcsanjayj/kcsanjayj/output/github-snake.svg" />
</picture>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2f81f7,100:0d1117&height=100&section=footer" alt="" />

</div>
