<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:1f3b73,100:2f81f7&height=190&section=header&text=Shaik%20Aahil%20Farhan&fontSize=44&fontColor=ffffff&fontAlignY=36&desc=Software%20Engineer%20%C2%B7%20Applied%20AI%20%C2%B7%20Distributed%20Systems&descSize=16&descAlignY=58&animation=fadeIn" alt="Shaik Aahil Farhan — Software Engineer, Applied AI, Distributed Systems" width="100%" />
</p>

<p align="center">
  <a href="https://github.com/Aahil101">
    <img src="https://readme-typing-svg.demolab.com?font=Inter&weight=500&size=18&duration=3200&pause=1200&color=58A6FF&center=true&vCenter=true&width=640&lines=Retrieval+systems+that+cite+their+sources;ML+pipelines+evaluated+against+real+baselines;Fault-tolerant+distributed+systems;Clean%2C+user-centric+product+engineering" alt="Retrieval systems that cite their sources. ML pipelines evaluated against real baselines. Fault-tolerant distributed systems. Clean, user-centric product engineering." />
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Based%20in-Bangalore%2C%20India-1f3b73?style=flat-square" alt="Based in Bangalore, India" />
  <img src="https://img.shields.io/badge/Open%20to-SWE%20%26%20Applied%20AI%20internships-2f81f7?style=flat-square" alt="Open to software engineering and applied AI internships" />
</p>

---

## About

I build software that is reliable, measurable, and easy to reason about. My work centres on
retrieval-augmented generation, machine-learning reliability, and distributed systems, with an
emphasis on evaluating every claim against a baseline rather than relying on demos.

| Focus area | What that means in practice |
|---|---|
| **Retrieval and LLM systems** | Hybrid retrieval, reranking, grounded answers with citations, self-correcting pipelines |
| **ML reliability** | Benchmark design, drift monitoring, out-of-distribution detection, honest evaluation |
| **Distributed systems** | RAFT consensus, Kafka and Spark stream processing, fault tolerance |
| **Product engineering** | FastAPI services, React and TypeScript frontends, clean user-facing design |

---

## Selected Work

| Project | Description | Key result |
|---|---|---|
| [**PaperTrail**](https://github.com/Aahil101/papertrail) | Question answering over PDFs with page-level citations | hit@1 **84.9% → 95.0%** |
| [**Adaptive RAG Reliability Engine**](https://github.com/Aahil101/-Adaptive-RAG-Reliability-Engine) | Self-correcting RAG over SEC filings | Correctness **34.8% → 60.7%** |
| [**TrustKYC**](https://github.com/Aahil101/kyc-drift) | Deepfake-aware video e-KYC with drift and zero-day detection | Novel-attack AUROC **0.914** |
| [**Finora MarketLens**](https://github.com/Aahil101/Finora-MarketLens) | Source-grounded market intelligence with an agentic assistant | **105** backend tests |
| [**CanvasRAFT**](https://github.com/Aahil101/CanvasRAFT) | Collaborative drawing board on a three-node RAFT cluster | Survives **leader failure** |
| [**Pulse**](https://github.com/Aahil101/fitness_tracker) | AI nutrition and fitness tracker | **2,854** reference foods |
| [**Namma Metro Live**](https://github.com/Aahil101/namma-metro-live-tracker-and-simulator) | Real-time Bengaluru metro simulation | **380** passing tests |

<sub>Select a project below to expand the engineering details.</sub>

<details>
<summary><b>PaperTrail</b> — grounded PDF question answering</summary>
<br/>

- **Problem:** answers over long documents are only useful if they can be traced back to a page.
- **Approach:** table-aware ingestion, hybrid BM25 + dense retrieval fused with RRF, and cross-encoder reranking; abstains with "not in this document" when unsupported.
- **Results:** hit@1 improved from 84.9% to 95.0% and MRR from 0.892 to 0.964 on a 129-question benchmark. Runs entirely on CPU at zero cost.
- **Stack:** Python, BM25, dense embeddings, cross-encoder reranking, Streamlit

</details>

<details>
<summary><b>Adaptive RAG Reliability Engine</b> — does self-correction actually help?</summary>
<br/>

- **Problem:** self-correcting RAG is widely recommended but rarely measured against a fair baseline.
- **Approach:** a LangGraph pipeline that grades its own retrieval, rewrites failed queries, verifies answers against evidence, and abstains when filings do not support an answer.
- **Results (150 questions, answer key built by code):**

  | Metric | Naive RAG | Adaptive RAG |
  |---|---|---|
  | Ground-truth correctness | 34.8% | **60.7%** |
  | Answer rate (answerable) | 43.7% | **76.3%** |
  | Abstention accuracy | 93.3% | **100%** |
  | LLM calls per query | **1.00** | 5.09 |

- **Stack:** Python, LangGraph, FAISS, FastAPI, React

</details>

<details>
<summary><b>TrustKYC</b> — video e-KYC that monitors itself</summary>
<br/>

- **Problem:** KYC models fail silently through concept drift and confidently misclassify new attack types.
- **Approach:** ArcFace identity matching, passive liveness, and a ViT-B/16 deepfake detector, plus a drift monitor (PSI, KS, MMD, ADWIN) and an open-set novelty detector using Mahalanobis and k-NN over forensic features.
- **Results:** deepfake detector accuracy 97.3%; novel-attack AUROC 0.914; zero-day recall of 89–98% across two synthesized attack families.
- **Stack:** PyTorch, ONNX Runtime, scikit-learn, FastAPI, React

</details>

<details>
<summary><b>Finora MarketLens</b> — market intelligence that shows its sources</summary>
<br/>

- **Problem:** generic sentiment models misread headlines whose sentiment depends on the target company.
- **Approach:** FinBERT + LoRA triage escalating to an LLM judge for target-aware sentiment; an agentic assistant that calls live price, news, and portfolio tools and streams every tool call to the UI; allocations from realised volatility, drawdown, and correlation.
- **Results:** no fabricated figures — every number is traced to a provider response or computed from one; 105 backend tests.
- **Stack:** Python, FastAPI, FinBERT, Groq, vanilla JavaScript, Vite

</details>

<details>
<summary><b>CanvasRAFT</b> — consensus-backed collaborative drawing</summary>
<br/>

- **Problem:** a shared canvas should keep working when the server coordinating it fails.
- **Approach:** a WebSocket gateway routes strokes to the current RAFT leader; replicas handle leader election, log replication, commit tracking, and catch-up sync for restarted nodes.
- **Results:** the board keeps accepting strokes through leader failure and re-election. Team project of four.
- **Stack:** Node.js, WebSockets, Docker Compose, Nginx

</details>

<details>
<summary><b>Pulse</b> — AI nutrition and fitness tracker</summary>
<br/>

- **Problem:** photo-based calorie estimates are only as good as the nutrition data behind them.
- **Approach:** meal photos produce an editable draft; calories are resolved through a ranked pipeline of 658 chain menu items, a curated table, 2,854 CoFID foods, and USDA data, with plausibility checks. Includes deficit tracking, weight forecasting, and an AI coach grounded in the user's own numbers.
- **Stack:** React, TypeScript, FastAPI, Supabase, Redis, Gemini

</details>

<details>
<summary><b>Namma Metro Live</b> — the Bengaluru metro, moving in real time</summary>
<br/>

- **Problem:** Namma Metro has no public real-time feed.
- **Approach:** runs published BMRCL GTFS timetables against the real clock on OpenStreetMap track geometry at 60 fps, with station boards, shareable train codes, and time controls.
- **Results:** 380 passing tests, zero runtime dependencies, no build step.
- **Stack:** JavaScript, GTFS, OpenStreetMap

</details>

<details>
<summary><b>Additional projects</b></summary>
<br/>

| Project | Description |
|---|---|
| [Real-Time Server Monitoring](https://github.com/Aahil101/Real-Time-Server-Monitoring-Distributed-Pipeline-) | Distributed Kafka and Spark pipeline with windowed analytics and threshold alerting across machines connected over ZeroTier |
| [Hector SLAM Mapping](https://github.com/Aahil101/HectorSlamMappingMAR) | Indoor mapping and localisation using LiDAR with ROS, Gazebo and RViz |
| [NeetCode Submissions](https://github.com/Aahil101/neetcode-submissions) | Data structures and algorithms practice |

</details>

---

## Technical Skills

<p align="center">
  <a href="#technical-skills">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=python,ts,js,html,css,bash,pytorch,sklearn&theme=dark&perline=8" />
      <img src="https://skillicons.dev/icons?i=python,ts,js,html,css,bash,pytorch,sklearn&theme=light&perline=8" alt="Python, TypeScript, JavaScript, HTML, CSS, Bash, PyTorch, scikit-learn" />
    </picture>
  </a>
  <br/>
  <a href="#technical-skills">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=fastapi,nodejs,postgres,supabase,redis,kafka,spark,react&theme=dark&perline=8" />
      <img src="https://skillicons.dev/icons?i=fastapi,nodejs,postgres,supabase,redis,kafka,spark,react&theme=light&perline=8" alt="FastAPI, Node.js, PostgreSQL, Supabase, Redis, Kafka, Spark, React" />
    </picture>
  </a>
  <br/>
  <a href="#technical-skills">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=vite,docker,nginx,linux,ros,git&theme=dark&perline=8" />
      <img src="https://skillicons.dev/icons?i=vite,docker,nginx,linux,ros,git&theme=light&perline=8" alt="Vite, Docker, Nginx, Linux, ROS, Git" />
    </picture>
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black" alt="Hugging Face" />
  <img src="https://img.shields.io/badge/ONNX%20Runtime-005CED?style=flat-square&logo=onnx&logoColor=white" alt="ONNX Runtime" />
  <img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangGraph" />
  <img src="https://img.shields.io/badge/FAISS-0467DF?style=flat-square&logo=meta&logoColor=white" alt="FAISS" />
</p>

---

## GitHub Activity

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api?username=Aahil101&show_icons=true&hide_rank=true&hide_border=true&include_all_commits=true&theme=github_dark&bg_color=0d1117&title_color=58a6ff&icon_color=58a6ff" />
    <img height="160" src="https://github-readme-stats.vercel.app/api?username=Aahil101&show_icons=true&hide_rank=true&hide_border=true&include_all_commits=true&title_color=2f81f7&icon_color=2f81f7" alt="GitHub statistics for Aahil101" />
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=Aahil101&layout=compact&langs_count=8&hide_border=true&theme=github_dark&bg_color=0d1117&title_color=58a6ff" />
    <img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Aahil101&layout=compact&langs_count=8&hide_border=true&title_color=2f81f7" alt="Most used languages" />
  </picture>
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://streak-stats.demolab.com?user=Aahil101&hide_border=true&theme=github-dark-blue&background=0D1117" />
    <img src="https://streak-stats.demolab.com?user=Aahil101&hide_border=true&theme=default" alt="Contribution streak for Aahil101" />
  </picture>
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Aahil101/Aahil101/output/github-snake-dark.svg" />
    <img src="https://raw.githubusercontent.com/Aahil101/Aahil101/output/github-snake.svg" alt="Animated snake moving across the contribution graph" width="100%" />
  </picture>
</p>

---

## Contact

<p align="center">
  <a href="https://github.com/Aahil101"><img src="https://img.shields.io/badge/GitHub-Aahil101-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub profile" /></a>
  <!-- Add when ready:
  <a href="https://www.linkedin.com/in/YOUR-LINKEDIN/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge" alt="LinkedIn profile" /></a>
  <a href="mailto:YOUR-EMAIL@example.com"><img src="https://img.shields.io/badge/Email-Get%20in%20touch-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  -->
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:2f81f7,50:1f3b73,100:0d1117&height=100&section=footer&animation=fadeIn" alt="" width="100%" />
</p>
