# Shaik Aahil Farhan

**Computer Science Student · Software Engineer · Applied AI**

Bangalore, India

---

I build software that is reliable, measurable, and easy to reason about. My work centres on
retrieval-augmented generation, machine-learning reliability, and distributed systems, with an
emphasis on evaluating every claim against a baseline rather than relying on demos.

**Areas of focus**

- **Retrieval and LLM systems** — hybrid retrieval, reranking, grounded answers with citations, self-correcting pipelines
- **ML reliability** — benchmark design, drift monitoring, out-of-distribution detection, honest evaluation
- **Distributed systems** — consensus (RAFT), stream processing with Kafka and Spark, fault tolerance
- **Full-stack product engineering** — FastAPI services, React and TypeScript frontends, clean user-facing design

---

## Selected Work

| Project | Description | Key result |
|---|---|---|
| [**PaperTrail**](https://github.com/Aahil101/papertrail) | Question answering over PDFs with page-level citations, using table-aware ingestion, hybrid BM25 + dense retrieval (RRF) and cross-encoder reranking. Runs on CPU at zero cost. | hit@1 improved from **84.9% to 95.0%** on a 129-question benchmark |
| [**Adaptive RAG Reliability Engine**](https://github.com/Aahil101/-Adaptive-RAG-Reliability-Engine) | Self-correcting RAG over SEC filings that grades retrieval, rewrites failed queries, verifies answers against evidence and abstains when unsupported. Built with LangGraph. | Correctness improved from **34.8% to 60.7%** vs. a naive baseline across 150 questions |
| [**TrustKYC**](https://github.com/Aahil101/kyc-drift) | CPU-deployable video e-KYC: face verification, liveness and deepfake detection, with concept-drift monitoring and an open-set zero-day attack detector. | Novel-attack detection AUROC of **0.914**; deepfake detector accuracy **97.3%** |
| [**Finora MarketLens**](https://github.com/Aahil101/Finora-MarketLens) | Market intelligence platform with target-aware financial sentiment (FinBERT + LoRA escalating to an LLM judge), an agentic tool-using assistant and volatility-based portfolio allocation. | Every figure traceable to a live data source; **105 backend tests** |
| [**CanvasRAFT**](https://github.com/Aahil101/CanvasRAFT) | Collaborative drawing board replicated across a three-node RAFT cluster, with a WebSocket gateway and Docker Compose deployment. Team project. | Continues accepting strokes through **leader failure and re-election** |
| [**Pulse**](https://github.com/Aahil101/fitness_tracker) | AI nutrition and fitness tracker with photo-based meal logging, a layered nutrition-data pipeline, calorie-deficit tracking and weight forecasting. | Nutrition lookup across **658 menu items** and **2,854 reference foods** |
| [**Namma Metro Live**](https://github.com/Aahil101/namma-metro-live-tracker-and-simulator) | Real-time simulation of the Bengaluru metro network from published GTFS timetables on real track geometry, built without frameworks or runtime dependencies. | **380 passing tests**; zero runtime dependencies |

<details>
<summary><b>Additional projects</b></summary>
<br/>

| Project | Description |
|---|---|
| [Real-Time Server Monitoring](https://github.com/Aahil101/Real-Time-Server-Monitoring-Distributed-Pipeline-) | Distributed Kafka and Spark pipeline with windowed analytics and threshold-based alerting across machines connected over ZeroTier. |
| [Hector SLAM Mapping](https://github.com/Aahil101/HectorSlamMappingMAR) | Indoor mapping and localisation using LiDAR with ROS, Gazebo and RViz. |
| [NeetCode Submissions](https://github.com/Aahil101/neetcode-submissions) | Data structures and algorithms practice. |

</details>

---

## Technical Skills

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)

**Machine Learning and AI**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![ONNX](https://img.shields.io/badge/ONNX%20Runtime-005CED?style=flat-square&logo=onnx&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![FAISS](https://img.shields.io/badge/FAISS-0467DF?style=flat-square&logo=meta&logoColor=white)

**Backend and Data**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Apache%20Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![Apache Spark](https://img.shields.io/badge/Apache%20Spark-E25A1C?style=flat-square&logo=apachespark&logoColor=white)

**Frontend, Infrastructure and Tools**

![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![ROS](https://img.shields.io/badge/ROS-22314E?style=flat-square&logo=ros&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

---

## Contact

[![GitHub](https://img.shields.io/badge/GitHub-Aahil101-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Aahil101)
<!-- Add when ready:
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Shaik%20Aahil%20Farhan-0A66C2?style=flat-square)](https://www.linkedin.com/in/YOUR-LINKEDIN/)
[![Email](https://img.shields.io/badge/Email-Contact-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:YOUR-EMAIL@example.com)
-->

Open to software engineering and applied AI internship opportunities.
