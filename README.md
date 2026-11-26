<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1200&color=34D399&center=true&vCenter=true&width=760&height=48&lines=%24+whoami;Sanjay+J+%C2%B7+AI+engineer;%24+cat+philosophy.txt;Most+LLM+systems+fail+silently.;Mine+fail+honestly." alt="$ whoami: Sanjay J, AI engineer. Most LLM systems fail silently. Mine fail honestly." />

</div>

<br/>

```text
$ ./sanjay --self-test

PASS  plans, parallelizes, critiques and repairs agent work        rapTOR
PASS  private document Q&A with measured retrieval                 Spaghetti
PASS  transformer from random init on a 6 GB laptop GPU            TinyGPT-X
PASS  audits its own v1, regression-tests every defect found       8 / 8 fixed
PASS  writes the limitations section before being asked            every repo
SKIP  production scale, multi-user hosting                         not yet, and I say so

5 passed · 1 skipped · 0 hidden
```

<br/>

## 🧾 Build log

| | Project | What it proves | Proof |
|---|---|---|---|
| 🦀 | **[rapTOR](https://github.com/kcsanjayj/rapTOR)** | Orchestration you can trust to fail honestly: validated DAG, parallel workers, critic-gated repair | 63 Rust tests · 6 Python tests · 26 evals · 4 direct dependencies |
| 🍝 | **[Spaghetti](https://github.com/kcsanjayj/Spaghetti)** · [live UI](https://spaghetti.kcsanjayj.workers.dev) | Private RAG over your own PDFs and DOCX, no cloud, no API keys | 87 tests · abstention 0.8 → 1.0 via ablation · 0 a11y violations |
| 🧠 | **[TinyGPT-X](https://github.com/kcsanjayj/TinyGPT-X)** · [model](https://huggingface.co/kcsanjayj/TinyGPT-X) | A GPT written by hand and trained with no pretrained weights | 13.9M params · val. perplexity 6.05 · 11.3 min on an RTX 3050 |

<br/>

## 🐛 A bug report I filed on myself

My first rapTOR looked fine and was broken. I reviewed it, rewrote it, and gave every defect a test that fails if it returns.

| What was silently wrong | Why it hid | Now |
|---|---|---|
| Tasks never got their dependencies' outputs | Final answer still looked plausible | Data-flow eval |
| Critic skipped the last step | Review existed in the diagram, not the code | Critic covers 100% of LLM nodes |
| Bad plan fell back to a canned demo | Ask about Rome, get Python vs Rust | Neutral fallback, rejected plans sent back with the reason |
| `9**9**9` hung the calculator | One prompt could pin a CPU | Bounded calculator, fails fast |

<br/>

## 🧰 Stack

<div align="center">

<img src="https://skillicons.dev/icons?i=rust,py,pytorch,js,html,css,git,githubactions,powershell&perline=9" alt="Rust, Python, PyTorch, JavaScript, HTML, CSS, Git, GitHub Actions, PowerShell" />

<br/>

<img src="https://img.shields.io/badge/Ollama-0b1020?style=flat-square&logo=ollama&logoColor=white" alt="Ollama" />
<img src="https://img.shields.io/badge/Hugging_Face-0b1020?style=flat-square&logo=huggingface&logoColor=FFD21E" alt="Hugging Face" />
<img src="https://img.shields.io/badge/Playwright-0b1020?style=flat-square&logo=playwright&logoColor=2EAD33" alt="Playwright" />
<img src="https://img.shields.io/badge/LLM-evaluation-0b1020?style=flat-square" alt="LLM evaluation" />

</div>

<br/>

## 📡 Status

```text
now     rapTOR vs real local models, planner prompt tuning
next    embedding retrieval in Spaghetti · model-graded evals with variance
open    AI / ML engineering roles where reliability matters
```

<div align="center">

<a href="mailto:kcsanjayj@gmail.com"><img src="https://img.shields.io/badge/kcsanjayj@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
<a href="https://linkedin.com/in/kcsanjayj"><img src="https://img.shields.io/badge/linkedin.com/in/kcsanjayj-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
<a href="https://huggingface.co/kcsanjayj"><img src="https://img.shields.io/badge/Hugging_Face-0b1020?style=for-the-badge&logo=huggingface&logoColor=FFD21E" alt="Hugging Face" /></a>

</div>
