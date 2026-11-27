# Hi, I'm Bowen 👋

I'm a computational scientist working at the intersection of **machine learning, software engineering, agentic AI, and GPU computing**.

I turn complex data into faster answers, building **ML-accelerated image reconstruction** and **AI agents** end to end, from **data pipelines** and model training to **tested APIs** and **MLOps**.

## 🔬 What I work on

<table>
  <tr>
    <td width="40%"><img src="assets/ml_imaging.png" alt="AI/ML for production scientific imaging" width="100%"></td>
    <td width="60%" valign="top">

### AI/ML for production scientific imaging (online soon in IUCrJ)

Integrated ML-accelerated ptychographic reconstruction into the **production workflow at an ALS beamline**, achieving a **2× speedup with improved quality** over legacy methods.

**Python · PyTorch · Deep Learning · Computer Vision · CUDA · Multi-GPU · Prefect · Docker**

📄 First-author paper in **IUCrJ**: *Machine Learning–Augmented Acceleration of Iterative Ptychographic Reconstruction* ([DOI](https://doi.org/10.1107/S2052252526010419))

<details>
<summary><b>Details</b></summary>

- Developed a **U-Net fast-forward operator** in [CDTools](https://github.com/cdtools-developers/cdtools) that is applied once after a short warm-up, then hands back to the physics-based solver. Inference takes about **3.7 ms**, 0.2–0.3% of a single iteration.
- Trained on **32 NVIDIA A100 GPUs** at NERSC using **7,446 experimental datasets** from the Advanced Light Source.
- Tested on **100 samples from different years** than the training data, achieving comparable or improved reconstruction quality with faster convergence (**1.5–2× speedup** per reconstruction).
- Benchmarked **multi-GPU reconstruction**: **2.6× speedup on 4 GPUs** (65% parallel efficiency), with only 1.5–4.2% ML overhead relative to the standard solver.
- Deployed to production with **Prefect**-based, GPU-aware orchestration: shared data ingestion for standard and ML pipelines, **Docker**-based reconstruction tasks, and GPU queuing with file-based locking.
- Cut ptycho-tomography time per projection from **~153 s to ~41 s (~4×)** on a 74-projection dataset, compared with the default 200-iteration workflow.

</details>

</td>
  </tr>
  <tr>
    <td width="40%"><img src="assets/reason_rag.png" alt="Reasoning-LLM Agent for Enterprise RAG" width="100%"></td>
    <td width="60%" valign="top">

### Reasoning-LLM Agent for Enterprise RAG

An LLM agent that chooses what to search and read raised the score over single-shot RAG from **0.529 to 0.745** on 500 [EnterpriseRAG-Bench](https://github.com/onyx-dot-app/EnterpriseRAG-Bench) questions (2,723-document subset).

**Python · FAISS · Ollama · FastAPI · React · TypeScript · MLflow · DVC · Docker · GitHub Actions**

🔗 Code: [TechRAG](https://github.com/BOWENmeZHENG/TechRAG)

<details>
<summary><b>Details</b></summary>

- 95% bootstrap CI for the gain: +0.176 to +0.256, at about 1.6× the time per question. The same local model answered and judged.
- Built a bounded **agentic search loop** with `search` and `read_doc` tools and step, context, and duplicate-call limits, without an agent framework.
- Implemented **dense, BM25, and hybrid retrieval**, served through a FastAPI API and a React web UI.
- Added **MLflow** run tracking, tests, CI, and Docker packaging, with **DVC** data and index versioning on the [`dvc-version`](https://github.com/BOWENmeZHENG/TechRAG/tree/dvc-version) branch.

</details>

</td>
  </tr>
  <tr>
    <td width="40%"><img src="assets/agentic_platform.png" alt="Agentic Data Platform" width="100%"></td>
    <td width="60%" valign="top">

### Agentic Data Platform

An AI-enabled workbench for browsing, analyzing, and reasoning over **GIWAXS/SAXS experimental data**.

**React · TypeScript · FastAPI · Tiled · LangGraph · MCP · Docker · Ollama/vLLM**

🔒 Internal ALS Computing project

<details>
<summary><b>Details</b></summary>

- Integrated a **Tiled scientific data catalog** with interactive GIWAXS/SAXS visualization and analysis tools.
- Built a **LangGraph-based AI assistant** for natural-language interaction with data and tools, exposing scientific tools through the **Model Context Protocol (MCP)**.
- Integrated **knowledge-graph construction, querying, and visualization** across samples, materials, and publications.
- Developed a modular full-stack architecture connecting the React frontend with FastAPI services for data access, analysis, and AI agents.
- [TBD: scale or impact, such as datasets cataloged, users, or time saved]

</details>

</td>
  </tr>
  <tr>
    <td width="40%"><img src="assets/federated_agent.png" alt="Federated Agent Deployment" width="100%"></td>
    <td width="60%" valign="top">

### Federated Agent Deployment

A distributed workflow that runs **LLM-based scientific term extraction** on GPU resources at remote HPC systems, contributed to [FAIR2WISE](https://github.com/fair2wise/FAIR2WISE).

**Python · LLMs · LangGraph · Distributed Computing · Academy Agents · Globus Compute**

🔗 Code: [`bowen/academy_agent`](https://github.com/fair2wise/FAIR2WISE/tree/bowen/academy_agent) branch

<details>
<summary><b>Details</b></summary>

- Integrated the LangGraph term-extraction pipeline with **Academy Agents and Globus Compute**, building local and remote agents for **execution, task coordination, and status monitoring**.
- Implemented real-time streaming of logs and CPU, memory, and GPU metrics from remote jobs.
- Enabled concurrent processing of scientific documents and aggregation of extracted terminology for downstream knowledge-representation workflows.
- [TBD: deployment across sites, such as NERSC and Argonne]
- [TBD: your role in the retrieval and paper-download agents that update the knowledge graph]
- [TBD: scale or performance, such as publications processed or throughput]

</details>

</td>
  </tr>
</table>

## 🛠 Skills

- **Languages:** Python · TypeScript · SQL
- **Machine learning:** PyTorch · Deep Learning · Computer Vision · Optimization · CUDA · Multi-GPU Computing
- **LLMs and agents:** Agentic AI · RAG · LangGraph · MCP · FAISS · LLM Evaluation · vLLM · Ollama
- **Software engineering:** FastAPI · REST APIs · React · Concurrency Control · pytest · Git
- **MLOps and infrastructure:** Production ML Deployment · Data Pipelines · Workflow Orchestration · Prefect · Containerization · Docker · GPU Scheduling · Edge Computing · GitHub Actions · MLflow · DVC · Linux · Slurm
