# Venu Dattathreya Vemuru

MS Computer Science at the University of Georgia, graduating December 2026. I build backend and full-stack systems, and I benchmark ML inference when I want to know whether an optimization actually pays for itself.

[LinkedIn](https://www.linkedin.com/in/venuvemuru/) &nbsp;·&nbsp; [Google Scholar](https://scholar.google.com/citations?user=a3CSqKAAAAAJ&hl=en) &nbsp;·&nbsp; [Resume](https://github.com/venu284/Resume/blob/main/resume.pdf) &nbsp;·&nbsp; venudattathreya@gmail.com

## What I am working on

I am the sole developer on the scheduling application for [SER-CAT](https://sercat.franklinresearch.uga.edu), a 20+ institution synchrotron consortium at Argonne National Laboratory's Advanced Photon Source. It replaced a decade-old manual process and now runs in production, scheduling beam time funded by $2 to $3 million in annual member share revenue. Two full runs have gone through it.

The interesting part was the allocation engine. There was no spec, only a fairness mandate from the consortium directors, so I wrote a deterministic greedy allocator on a 1,325-line zero-dependency core. Schedules come out accepted as generated: fewer than 3 change requests against 100+ assignments. Swapping weighted-sum priority scoring for a leximin objective, which maximizes the worst-served institution rather than the average, cut non-preferred placements from 35% to 30% and narrowed the satisfaction spread across institutions by 26%. I validated that against a completed production run, not a simulation.

Around it: a React SPA with member and admin portals across 20 routes, 44 serverless endpoints, and an 18-table Postgres schema on Vercel.

Before that I moved SER-CAT's public site off a legacy host, which took its cost from $10K a year to zero and put content ownership back with the consortium's own directors. It is still in production on Drupal 11.

## Tools I reach for

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)

## Projects worth reading

**[LLM_Comparison](https://github.com/venu284/LLM_Comparison)** &nbsp;·&nbsp; Python, PostgreSQL, Docker

A benchmark harness that runs LLM-generated code against real test suites in isolated containers. 65 hand-authored web development tasks with reference solutions and deliberately buggy fixtures, evaluated across 5 open-weight models, scored on whether the tests pass rather than on how the answer reads.

I pre-registered four hypotheses before collecting any data, and the model-routing hypothesis lost. A perfect oracle router capped out at +8.6% against the +15% the idea needed to be worth building. Reporting that is more useful than quietly dropping it.

**[llm-inference-benchmark](https://github.com/venu284/llm-inference-benchmark)** &nbsp;·&nbsp; PyTorch, TensorRT, CUDA

PyTorch Eager against torch.compile against TensorRT on a single RTX 3090, measuring latency, throughput, GPU memory, compilation overhead, and utilization. The point is the effort-to-payoff curve on consumer hardware: torch.compile is one line, TensorRT is a build step, and the numbers say when the build step earns its keep. Includes a 14-paper literature review.

## Publications

[Enhancing Image Deblurring Algorithm Selection and Performance Evaluation for CCTV](https://ieeexplore.ieee.org/document/10369555), IEEE, January 2024.

Dimensionality Reduction Improves Genomic Prediction, co-author, under submission. I built the deep learning side: 20 chromosome-wise autoencoders in PyTorch compressing 4,104 SNP markers to 640 dimensions, after diagnosing the single full-genome model as an ill-posed p >> n problem. That track raised top-quartile hit rate for identifying top performers by up to 30%.

## Reach me

Athens, GA. Graduating December 2026 and looking for software engineering roles.
[venudattathreya@gmail.com](mailto:venudattathreya@gmail.com) &nbsp;·&nbsp; [linkedin.com/in/venuvemuru](https://www.linkedin.com/in/venuvemuru/)
