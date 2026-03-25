# APPS Coding Experiments

Notebook exploring LLM-based code evaluation on the APPS benchmark, with two experiments:

**Experiment 1 — Evidence Provider BoN Sweep**
An LLM evidence provider selects passing unit tests to show a judge. The judge decides correctness *without seeing the code*. Best-of-N (BoN=k) means the evidence provider makes k independent LLM calls and submits the selection that most convinces the judge.

**Experiment 2 — Labeled Batch Sweep**
The judge is shown labeled examples (problem + evidence + verdict) before deciding. We sweep:
- **State types**: `fraction` (pass rate), `code` (actual code), `code_fraction` (both)
- **Evidence types**: `tests` (full I/O pairs), `count` (number of passing tests only)
- **Modes**: `logprob` (score = P(A) from token logprobs), `cot` (chain-of-thought, score = 0/1)

## View the notebook

[Open in nbviewer](https://nbviewer.org/github/yyyyykh/apps-results-notebook/blob/main/apps_results.ipynb)
