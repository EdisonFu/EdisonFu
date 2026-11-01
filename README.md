<h1 align="center">EdisonFu</h1>

<p align="center">
  <b>Quantitative research & trading infrastructure.</b><br>
  Factor mining · multi-agent LLM pipelines · Go backends
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" alt="Go">
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch">
  <img src="https://img.shields.io/badge/XGBoost-337AB7?style=flat-square" alt="XGBoost">
  <img src="https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white" alt="pandas">
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI">
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white" alt="Kubernetes">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker">
</p>

---

### What I work on

I build the machinery that turns a research idea into a factor you can actually
trade — and the discipline that stops it from lying to you.

Most of my work sits on one principle: **a backtest is a claim about the future,
so the pipeline has to be built to fail loudly.** Point-in-time data, structural
IS/OOS separation, thresholds derived from sample size instead of hardcoded,
transaction costs in from day one. An elegant result that leaked is worth less
than a mediocre one that didn't.

```
research direction  →  literature retrieval  →  factor hypothesis
                    →  code generation  →  IS/OOS gating  →  factor library
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

### Things I've learned the expensive way

- **Silent degradation is the costliest bug class.** A fallback that returns an
  empty value doesn't read as "parsing failed" — it reads as "the feature is
  gone." Failures have to be visible.
- **Hardcoded thresholds carry hidden couplings.** A cutoff tuned on 24 symbols
  was 2.3× too strict at 117, and nothing in the code recorded the dependency.
  Derive from the data.
- **Leakage survives any statistical correction.** The only real defense is
  structural: the split holds the data, not the caller's good intentions.
- **When the numbers look clean, suspect the harness.** A benchmark script that
  silently connected to a stale instance produced perfectly plausible,
  completely meaningless results — twice.

---

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=EdisonFu&show_icons=true&hide_border=true&include_all_commits=true&count_private=true&theme=github_dark&hide_title=true" height="150" alt="GitHub stats">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=EdisonFu&layout=compact&hide_border=true&langs_count=8&theme=github_dark&hide_title=true" height="150" alt="Top languages">
</p>
