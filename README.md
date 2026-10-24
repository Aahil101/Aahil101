<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:1f3b73,100:2f81f7&height=190&section=header&text=Shaik%20Aahil%20Farhan&fontSize=44&fontColor=ffffff&fontAlignY=36&desc=Software%20Engineer%20%C2%B7%20Applied%20AI%20%C2%B7%20Distributed%20Systems&descSize=16&descAlignY=58&animation=fadeIn" alt="Shaik Aahil Farhan — Software Engineer, Applied AI, Distributed Systems" width="100%" />
</p>

<p align="center">
  <a href="https://github.com/Aahil101">
    <img src="https://readme-typing-svg.demolab.com?font=Inter&weight=500&size=18&duration=3200&pause=1200&color=58A6FF&center=true&vCenter=true&width=660&lines=Research+Intern+%40+CoDMAV%2C+PES+University;Video-KYC+fraud+detection+and+concept-drift+monitoring;Retrieval+systems+that+cite+their+sources;Fault-tolerant+distributed+systems" alt="Research Intern at CoDMAV, PES University. Video-KYC fraud detection and concept-drift monitoring. Retrieval systems that cite their sources. Fault-tolerant distributed systems." />
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/B.Tech%20CSE-PES%20University-1f3b73?style=flat-square" alt="B.Tech in Computer Science and Engineering, PES University" />
  <img src="https://img.shields.io/badge/CGPA-8.08-1f3b73?style=flat-square" alt="CGPA 8.08" />
  <img src="https://img.shields.io/badge/Based%20in-Bengaluru%2C%20India-1f3b73?style=flat-square" alt="Based in Bengaluru, India" />
  <img src="https://img.shields.io/badge/Open%20to-SWE%20%26%20Applied%20AI%20internships-2f81f7?style=flat-square" alt="Open to software engineering and applied AI internships" />
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/shaik-aahil-farhan"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge" alt="LinkedIn profile" /></a>
  <a href="mailto:shaikaahilfarhan@gmail.com"><img src="https://img.shields.io/badge/Email-Get%20in%20touch-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email Shaik Aahil Farhan" /></a>
  <a href="https://github.com/Aahil101"><img src="https://img.shields.io/badge/GitHub-Aahil101-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub profile" /></a>
</p>

---

## About

I am a Computer Science student at PES University and a research intern at CoDMAV, where I work on
video-KYC fraud detection and concept-drift monitoring. I build software that is reliable,
measurable, and easy to reason about, with an emphasis on evaluating every claim against a
baseline rather than relying on demos.

| Focus area | What that means in practice |
|---|---|
| **Applied AI and computer vision** | Vision Transformers, deepfake and liveness detection, explainable AI with LIME and SHAP |
| **Retrieval and LLM systems** | Hybrid retrieval, reranking, grounded answers with citations, LLM-as-a-judge, AI agents |
| **ML reliability** | Concept-drift detection, out-of-distribution detection, benchmark design, honest evaluation |
| **Distributed systems** | Raft consensus, Kafka and PySpark stream processing, fault tolerance |
| **Product engineering** | FastAPI services, React and TypeScript frontends, clean user-facing design |

---

## Experience

### Research Intern — CoDMAV, PES University
<sub>Bengaluru · Jun 2026 – Jul 2026 · Related repository: <a href="https://github.com/Aahil101/kyc-drift">TrustKYC</a></sub>

- Built an end-to-end **video-KYC fraud detection pipeline** combining face recognition, passive liveness detection, and a **Vision Transformer deepfake classifier** to verify identity from live video.
- Designed an **evidence-fusion decision engine** that merges deepfake probability, liveness, image quality, and temporal-stability signals into a single automated trust score.
- Developed a **concept-drift monitoring framework** that tracks shifts in brightness, blur, texture, noise, and compression artifacts using PCA, Mahalanobis distance, KNN, MMD, and C2ST.

---

## Selected Work

| Project | Description | Key result |
|---|---|---|
| [**TrustKYC**](https://github.com/Aahil101/kyc-drift) | Deepfake-aware video e-KYC with drift and zero-day detection | Novel-attack AUROC **0.914** |
| **Explainable Breast Cancer Detection** | Attention-based multiple instance learning for histopathology | **5-fold** ensemble with LIME and SHAP |
| [**PaperTrail**](https://github.com/Aahil101/papertrail) | Question answering over PDFs with page-level citations | hit@1 **84.9% → 95.0%** |
| [**Adaptive RAG Reliability Engine**](https://github.com/Aahil101/-Adaptive-RAG-Reliability-Engine) | Self-correcting RAG over SEC filings | Correctness **34.8% → 60.7%** |
| [**Finora MarketLens**](https://github.com/Aahil101/Finora-MarketLens) | AI financial advisory and sentiment analysis platform | FinBERT **fine-tuned with LoRA** |
| [**CanvasRAFT**](https://github.com/Aahil101/CanvasRAFT) | Fault-tolerant collaborative drawing on a 3-node Raft cluster | Survives **leader failure** |
| [**Real-Time Server Monitoring**](https://github.com/Aahil101/Real-Time-Server-Monitoring-Distributed-Pipeline-) | Distributed telemetry pipeline with Kafka and PySpark | **30 s / 10 s** sliding windows |
| [**Pulse**](https://github.com/Aahil101/fitness_tracker) | AI nutrition and fitness tracker | **2,854** reference foods |
| [**Namma Metro Live**](https://github.com/Aahil101/namma-metro-live-tracker-and-simulator) | Real-time Bengaluru metro simulation | **380** passing tests |

<sub>Select a project below to expand the engineering details.</sub>

<details>
<summary><b>TrustKYC</b> — video e-KYC that monitors itself</summary>
<br/>

- **Problem:** KYC models fail silently through concept drift and confidently misclassify new attack types.
- **Approach:** ArcFace identity matching, passive liveness, and a ViT-B/16 deepfake detector fused by a fail-closed decision engine, plus a drift monitor (PSI, KS, MMD, C2ST, ADWIN) and an open-set novelty detector using Mahalanobis and k-NN over forensic features.
- **Results:** deepfake detector accuracy 97.3%; novel-attack AUROC 0.914; zero-day recall of 89–98% across two synthesized attack families.
- **Stack:** PyTorch, ONNX Runtime, scikit-learn, FastAPI, React

</details>

<details>
<summary><b>Explainable Breast Cancer Detection</b> — multiple instance learning for histopathology</summary>
<br/>

- **Problem:** cancer classification from whole-slide histopathology needs to be both accurate and explainable to clinicians.
- **Approach:** an attention-based TransformerMIL pipeline for multi-class classification, using StainGAN normalization and dual Phikon + CTransPath pathology embeddings from overlapping tissue patches, with similarity-based learning across patches to capture spatial relationships.
- **Explainability:** LIME and SHAP provide cell-level morphological insights; generative AI features assist doctors and patients with insights and decision support.
- **Results:** 5-fold ensemble that aggregates model probabilities across folds.
- **Stack:** Transformers, deep learning, pretrained LLMs, LIME, SHAP, Firebase, MySQL

</details>

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
<summary><b>Finora MarketLens</b> — financial advisory and sentiment analysis</summary>
<br/>

- **Problem:** generic sentiment models misread headlines whose sentiment depends on the target company, and LLM analysis is unreliable without grounding.
- **Approach:** FinBERT fine-tuned with LoRA for financial sentiment, escalating to an LLM-as-a-judge layer that assesses quality, relevance, and consistency; a RAG workflow retrieves financial news and market context to ground analysis; an agentic assistant calls live price, news, and portfolio tools.
- **Results:** every figure is traced to a provider response or computed from one; modular market, ticker-news, and financial-analysis workflows; 105 backend tests.
- **Stack:** Python, FastAPI, FinBERT, LoRA, RAG, Firebase, Groq, Vite

</details>

<details>
<summary><b>CanvasRAFT</b> — fault-tolerant distributed system using Raft consensus</summary>
<br/>

- **Problem:** a shared canvas should keep working when the server coordinating it fails.
- **Approach:** a 3-node Raft cluster in Node.js implementing follower, candidate, and leader state transitions, term management, quorum calculation, RequestVote RPC, and heartbeat-driven coordination, with randomized election timeouts to prevent persistent split votes. A WebSocket gateway routes requests to the current leader, so clients never track it.
- **Results:** validated with leader-failure and re-election tests; restarted nodes rejoin and catch up through log sync. Team project of four.
- **Stack:** Node.js, JavaScript, HTTP/RPC, WebSockets, Docker Compose, Nginx

</details>

<details>
<summary><b>Real-Time Server Monitoring</b> — distributed telemetry pipeline</summary>
<br/>

- **Problem:** infrastructure alerts need metrics from many machines processed in near real time.
- **Approach:** Kafka producer and consumer services with topic-level flows decouple ingestion from processing across machines connected over ZeroTier; PySpark sliding-window analytics (30 s windows, 10 s slides) compute server-level statistics and peak usage.
- **Results:** rule-based anomaly and threshold detection generates real-time alerts for abnormal CPU, memory, disk, and network behaviour.
- **Stack:** Apache Kafka, PySpark, Python, Pandas, ZeroTier

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
| [Hector SLAM Mapping](https://github.com/Aahil101/HectorSlamMappingMAR) | Indoor mapping and localisation using LiDAR with ROS, Gazebo and RViz |
| [NeetCode Submissions](https://github.com/Aahil101/neetcode-submissions) | Data structures and algorithms practice |

</details>

---

## Technical Skills

<p align="center">
  <a href="#technical-skills">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=python,java,js,ts,c,cpp,html,css,bash&theme=dark&perline=9" />
      <img src="https://skillicons.dev/icons?i=python,java,js,ts,c,cpp,html,css,bash&theme=light&perline=9" alt="Python, Java, JavaScript, TypeScript, C, C++, HTML, CSS, Bash" />
    </picture>
  </a>
  <br/>
  <a href="#technical-skills">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=pytorch,sklearn,fastapi,nodejs,react,vite,kafka,spark,postgres&theme=dark&perline=9" />
      <img src="https://skillicons.dev/icons?i=pytorch,sklearn,fastapi,nodejs,react,vite,kafka,spark,postgres&theme=light&perline=9" alt="PyTorch, scikit-learn, FastAPI, Node.js, React, Vite, Kafka, Spark, PostgreSQL" />
    </picture>
  </a>
  <br/>
  <a href="#technical-skills">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=mysql,mongodb,redis,firebase,supabase,docker,githubactions,linux,git&theme=dark&perline=9" />
      <img src="https://skillicons.dev/icons?i=mysql,mongodb,redis,firebase,supabase,docker,githubactions,linux,git&theme=light&perline=9" alt="MySQL, MongoDB, Redis, Firebase, Supabase, Docker, GitHub Actions, Linux, Git" />
    </picture>
  </a>
</p>

<details>
<summary><b>Full skills list</b></summary>
<br/>

| Area | Skills |
|---|---|
| **Languages** | Python, Java, JavaScript, TypeScript, C/C++, SQL |
| **AI / ML** | Machine learning, deep learning, computer vision, Vision Transformers, LLMs, generative AI, RAG, prompt engineering, AI agents, explainable AI (LIME, SHAP), LoRA, multiple instance learning, concept-drift detection, anomaly detection |
| **Data and streaming** | Apache Kafka, Apache Spark (PySpark), Pandas, EDA, time series (ARIMAX), Markov chains |
| **Backend and systems** | Node.js, FastAPI, REST APIs, WebSockets, Raft consensus, distributed systems |
| **Databases and DevOps** | PostgreSQL, MySQL, MongoDB, Redis, Firebase, Supabase, Docker, GitHub Actions (CI/CD), Git, Linux |
| **Core CS** | Data structures and algorithms, OOP, design patterns, DBMS, operating systems, computer networks |

</details>

---

## Education

**PES University** — Bengaluru, India<br/>
Bachelor of Technology in Computer Science and Engineering · Aug 2023 – Aug 2027 (expected) · CGPA 8.08

## Awards and Certifications

- **Distinction Award (5×)** — PES University
- **AWS Certificate**
- **Microsoft Azure 101**
- **Python for Data Science and Machine Learning Bootcamp** — Udemy

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

<p align="center">
  <a href="https://www.linkedin.com/in/shaik-aahil-farhan"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge" alt="LinkedIn profile" /></a>
  <a href="mailto:shaikaahilfarhan@gmail.com"><img src="https://img.shields.io/badge/Email-Get%20in%20touch-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email Shaik Aahil Farhan" /></a>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:2f81f7,50:1f3b73,100:0d1117&height=100&section=footer&animation=fadeIn" alt="" width="100%" />
</p>
