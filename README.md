<div align="center"> <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&pause=1000&color=2F81F7&center=true&vCenter=true&width=700&height=60&lines=%3E+whoami;Sanjay+J+%C2%B7+AI+Engineer;%3E+cat+mission.txt;Make+LLM+systems+that+fail+honestly" alt="terminal intro" /> </div>
rust
struct Sanjay {
    role:      "AI Engineer (fresher)",
    focus:     ["agents", "RAG", "models from scratch"],
    languages: ["Python", "Rust", "JavaScript"],
    habit:     "build it, break it, measure it",
    believes:  "a clear partial result beats a confident wrong answer",
    shipped:   3,   // each with tests, evals and written-down limits
}
<div align="center">

<a href="mailto:kcsanjayj@gmail.com"><img src="https://img.shields.io/badge/Email-kcsanjayj@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white"/></a> <a href="https://linkedin.com/in/kcsanjayj"><img src="https://img.shields.io/badge/LinkedIn-kcsanjayj-0A66C2?style=flat-square&logo=linkedin&logoColor=white"/></a> <a href="https://huggingface.co/kcsanjayj"><img src="https://img.shields.io/badge/Hugging%20Face-kcsanjayj-FFD21E?style=flat-square&logo=huggingface&logoColor=black"/></a>

</div>
🗂️ Case files

Three projects, each written up the same way: the problem, what I built, and the proof.

<table> <tr> <td valign="top" width="33%">
🦅 rapTOR

Agent orchestrator · Rust

Problem Agent demos work once, then fail silently behind a plausible answer.

Built A validated task graph, parallel workers, a critic that reviews every result, and honest partial results.

Proof 63 Rust tests · 26 evals · 8 bugs from my own v1, each with a regression test

Open repo →

</td> <td valign="top" width="33%">
🍝 Spaghetti

Private RAG · Python + Rust

Problem Chatting with your documents usually means sending them to a cloud.

Built A local-first app: PDF/DOCX in, cited streaming answers out, with a small model on your laptop.

Proof 87 tests · 28-case eval harness · abstention 0.8 → 1.0 by ablation

Open repo → · Live UI →

</td> <td valign="top" width="33%">
🧠 TinyGPT-X

GPT from scratch · PyTorch

Problem I wanted to understand a transformer, not just call one.

Built A 13.9M-parameter decoder-only model, trained from random weights on a 6 GB laptop GPU.

Proof Perplexity 6.05 · ~11 min training · exported logits verified against my own code

Open repo → · Model →

</td> </tr> </table>
🔬 How I think about LLM systems
text
1. The model is the easy part.        The machinery around it decides if it works.
2. Failure should be visible.         Count retries. Label partial results. Cap budgets.
3. Numbers need a caveat.             Say what an eval proves, and what it doesn't.
4. Fewer moving parts.                Small dependency lists, readable code.
🧰 Toolbox
<p align="center"> <img src="https://skillicons.dev/icons?i=py,rust,js,pytorch,git,github,githubactions&perline=7" alt="Toolbox" /> <br/> <img src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white"/> <img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black"/> <img src="https://img.shields.io/badge/RAG-6E56CF?style=flat-square"/> <img src="https://img.shields.io/badge/Multi--Agent-111827?style=flat-square"/> <img src="https://img.shields.io/badge/LLM%20Evals-2F81F7?style=flat-square"/> </p>
📡 Now
🧪 Running rapTOR's evals against real local models and tuning the planner prompts
🔎 Adding embedding-based retrieval to Spaghetti behind the same ranking interface
📬 Open to work

Looking for an AI / ML engineering role where reliability matters as much as the demo. Email me at kcsanjayj@gmail.com or find me on LinkedIn.

<div align="center"> <picture> <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/kcsanjayj/kcsanjayj/output/github-snake-dark.svg" /> <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/kcsanjayj/kcsanjayj/output/github-snake.svg" /> <img alt="Contribution snake" src="https://raw.githubusercontent.com/kcsanjayj/kcsanjayj/output/github-snake.svg" /> </picture> </div>
