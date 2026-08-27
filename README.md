

Themultivac readme · MD
# The Multivac
 
Independent evaluation infrastructure for frontier language models.
 
**Live:** [app.themultivac.com](https://app.themultivac.com) · **Site:** [themultivac.com](https://themultivac.com) · **Physics:** [multivacphysics.com](https://multivacphysics.com)
 
---
 
### What is here
 
**[multivac-evaluation](https://github.com/themultivac/multivac-evaluation)** — the evaluation engine and the full dataset, MIT licensed. 27,540 model to model judgments across 55 frontier models, 198 questions and 9 category pools, released with a datasheet and citation metadata for third party reproduction. Includes the execution graded coding benchmark, which runs candidate code in isolated subprocesses with networking disabled rather than asking a model whether the code looks right.
 
**multivac-app** — the platform itself. Next.js 15, React 19 and TypeScript on the front, FastAPI behind it, Postgres and Redis underneath. Closed source, live at [app.themultivac.com](https://app.themultivac.com).
 
**[multivacphysics](https://github.com/themultivac/multivacphysics)** — cross family adversarial evaluation of LLM physics reasoning.
 
### Why
 
Most model leaderboards use a single judge and do not disclose which one. Ask different frontier models to grade the same 22,254 responses and their average scores diverge by 2.5 points on a 10 point scale, so the choice of judge quietly moves the result more than the models differ.
 
And where correctness can be decided by execution, a judge should not get a vote at all. On one coding task with a race condition, every peer judge scored a functionally broken fix a perfect 10. Running it showed the fix overselling in 25 of 25 stress trials, identical to applying no fix. Looking correct and being correct diverge exactly where it matters.
 
Methodology, data and known limitations are public, including the bugs. Preprint self hosted, alongside the dataset.
 
---
 
Built by [Yash Darji](https://github.com/Yash2378).
