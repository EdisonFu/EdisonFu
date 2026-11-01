<h1 align="center">EdisonFu</h1>

<p align="center">
  <b>Quantitative trading research & infrastructure.</b><br>
  Quant research · LLM agent systems · AI infra · cloud native
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" alt="Go">
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch">
  <img src="https://img.shields.io/badge/LLM%20Agents-6E56CF?style=flat-square" alt="LLM Agents">
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI">
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white" alt="Kubernetes">
  <img src="https://img.shields.io/badge/Istio-466BB0?style=flat-square&logo=istio&logoColor=white" alt="Istio">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker">
</p>

---

### What I work on

My work spans two ends of the same problem. **Above:** quantitative research —
factor mining, signal construction, strategy validation, live execution.
**Below:** the infrastructure that holds it up — making the research loop run
itself, run fast, and return results worth believing.

The current focus is **rebuilding that research loop around LLM agents.** The
chain from reading a paper to a validated factor used to be strung together by
hand; it now decomposes into agents that specialize — retrieval, hypothesis
extraction, code generation, sandboxed execution, quality gating — and run
end to end. The bottleneck in research was never a shortage of ideas; it was
how fast you can disprove them. That is what the pipeline attacks.

On the engineering side I've built Go microservices, custom Kubernetes
controllers, and service-mesh observability. That experience feeds straight
back into AI infrastructure: concurrency orchestration, sandbox isolation,
cost control and failure visibility in an agent system are still distributed
systems problems — the unit of execution is just a model call instead of a
process.

```
Quant research   factor mining · signal construction · validation · execution
LLM agents       multi-agent orchestration · codegen · sandboxing · gating
AI infra         concurrency scheduling · cost control · observability
Cloud native     Go microservices · Kubernetes controllers · service mesh
```

---

### Selected work

| | |
|---|---|
| **[autoalpha](https://github.com/EdisonFu/autoalpha)** | Multi-agent factor mining pipeline. Takes a research direction, retrieves papers across arXiv/OpenAlex/Crossref, extracts factor hypotheses, generates and sandboxes the code, then gates on two-stage IS/OOS. Web console over FastAPI + SSE. <br> `Python` `FastAPI` `LLM agents` |
| **[auto-trade](https://github.com/EdisonFu/auto-trade)** | Automated order placement for the macOS build of a Chinese retail brokerage terminal, driven by the macOS Accessibility API — no Windows VM, no OCR, no simulated clicks. The native Cocoa UI reads back as a structured control tree, so state is verifiable instead of guessed. <br> `Python` `macOS AX` `automation` |
| **[ICEEMDAN-TCN-FU](https://github.com/EdisonFu/ICEEMDAN-TCN-FU)** | Time-series forecasting by ICEEMDAN decomposition, with a TCN fit per intrinsic mode. <br> `Python` `TCN` |
| **[autopaper](https://github.com/EdisonFu/autopaper)** | Turns financial papers and research notes into backtestable strategies, then derives variants to build an IS/OOS-validated alpha library. <br> `Python` `LLM agents` |
| **[stock-alpha](https://github.com/EdisonFu/stock-alpha)** | Full-stack alpha pipeline: minute-bar feature synthesis, IC-based factor selection, GRU + XGBoost hybrid for return prediction. <br> `Python` `PyTorch` `XGBoost` |
| **[stock_prediction_cnn](https://github.com/EdisonFu/stock_prediction_cnn)** | Predicting stock direction with convolutional networks over price-series inputs. <br> `Python` `CNN` |

---

### Contact

Open to conversations about quant research, LLM agent systems, and AI infrastructure.

<p align="center">
  <a href="mailto:fuzhendong1995@gmail.com">
    <img src="https://img.shields.io/badge/fuzhendong1995%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
  </a>
  <a href="https://github.com/EdisonFu">
    <img src="https://img.shields.io/badge/@EdisonFu-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
  </a>
</p>

---

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=EdisonFu&show_icons=true&hide_border=true&include_all_commits=true&count_private=true&theme=github_dark&hide_title=true" height="150" alt="GitHub stats">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=EdisonFu&layout=compact&hide_border=true&langs_count=8&theme=github_dark&hide_title=true" height="150" alt="Top languages">
</p>
