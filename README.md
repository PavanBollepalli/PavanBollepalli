<div align="center">

# Hey, I'm Pavan 👋

[![Typing SVG](https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&weight=600&size=24&duration=2500&pause=800&color=00D8FF&center=true&vCenter=true&width=700&height=50&lines=Full-Stack+Developer+%7C+AI%2FML+Engineer;RAG+Pipelines+%7C+Hybrid+Vector+Search;Google+Cloud+%26+AWS+Certified;Open+Source+Contributor+%40+Wikimedia)](https://git.io/typing-svg)

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

**I build AI-powered systems with production-grade backend architecture.**
*Currently shipping RAG pipelines, hybrid vector search, and real-time market intelligence.*

<br>

[![Portfolio](https://img.shields.io/badge/🌐_Portfolio-pavanbollepalli.me-00D8FF?style=for-the-badge)](https://pavanbollepalli.me)
[![LinkedIn](https://img.shields.io/badge/💼_LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/PavanBollepalli)
[![Email](https://img.shields.io/badge/📧_Email-Reach_Out-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:pavanvenkatanagamanoj@gmail.com)

</div>

---

## 🧠 About Me

```python
class Pavan:
    role      = "Full-Stack Developer & AI/ML Engineer"
    education = "B.Tech CS (AI & ML) — VVIT, Graduating May 2026"
    
    certifications = [
        "Google Cloud Associate Cloud Engineer",
        "AWS Certified Cloud Practitioner",
    ]
    
    achievements = [
        "1st Place — ACM Programming Contest (200+ participants)",
        "Open Source Contributor — Wikimedia Foundation",
    ]
    
    currently_building = "AI-powered GitHub Repository Analyzer"
    
    fun_fact = "I optimized a RAG pipeline from 9.6s to 0.48s and it felt better than any game win"
```

---

## 🚀 Flagship Project

<div align="center">

### ⚡ [SkillVector](https://github.com/PavanBollepalli/SkillVector) — AI Career Intelligence Platform

<img src="https://img.shields.io/badge/Next.js-16-black?style=flat-square&logo=next.js" />
<img src="https://img.shields.io/badge/React-19-61DAFB?style=flat-square&logo=react" />
<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
<img src="https://img.shields.io/badge/PostgreSQL+pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/Llama_3.3_70B-purple?style=flat-square" />
<img src="https://img.shields.io/badge/Mistral_Embed-FF7000?style=flat-square" />
<img src="https://img.shields.io/badge/O*NET_29.0-orange?style=flat-square" />
<img src="https://img.shields.io/badge/Three.js-black?style=flat-square&logo=three.js" />

</div>

A full-stack system that generates personalized, multi-phase learning paths using RAG, hybrid vector search, and U.S. labor market data. Not a wrapper around ChatGPT — a complete AI pipeline with measured performance.

<details>
<summary><b>🔍 Technical Deep Dive (click to expand)</b></summary>

<br>

#### 3-Layer RAG Retrieval Cache

```
L0  In-Memory (Python dict)     →  ~0ms     — role + query tuple key
L1  pgvector Hybrid Search       →  1 DB trip — HNSW cosine + B-tree metadata filter
L2  Tavily Live Web Fetch        →  1-3s     — only for cache misses, parallelized
```

**Measured Performance:**
| Scenario | RAG Latency | Total Generation |
|----------|-------------|-----------------|
| Cold start (0 cache hits) | 9.6s | 18.1s |
| Warm (L0 in-memory hit) | 0.48s | 10.1s |
| **Improvement** | **95% reduction** | **44% reduction** |

#### Hybrid Vector Search (pgvector)
- 1024-dim Mistral embeddings with **HNSW cosine index**
- B-tree metadata filter on `target_role` partitions search space per role
- N vector lookups batched into **1 SQL query** via `UNION ALL`
- Language-aware cache bypass: non-English queries always fetch fresh results

#### Concurrency & Safety
- `pg_try_advisory_xact_lock(user_id)` prevents duplicate generation from concurrent requests
- Per-user locking — 100 users generate paths fully in parallel
- Server-side test answers — MCQ correct answers never sent to frontend

#### O*NET Market Intelligence
- Fuzzy matches roles to SOC codes across 900+ occupations
- Extracts Hot Technology skills, knowledge domains, work activities
- LLM fallback for modern roles absent from O*NET

</details>

---

## 📂 Other Projects

| Project | What it does | Stack |
|---------|-------------|-------|
| [**NextVentures**](https://github.com/PavanBollepalli/nextventures) | Startup discovery platform with SSR, GitHub OAuth, and real-time CMS sync | Next.js 14, TypeScript, Sanity, NextAuth |
| [**HandShake**](https://github.com/PavanBollepalli/handshake) | Real-time ASL gesture recognition — CNN + MediaPipe hand landmark detection | TensorFlow, OpenCV, MediaPipe, Flask |
| [**PrepWise**](https://github.com/PavanBollepalli/prepwise) | AI interview prep with real-time speech analysis and feedback | Node.js, FastAPI, React, Socket.io |

---

## 💼 Experience

### Open Source Contributor — Wikimedia Foundation
**Jul 2024 – Sep 2025 · Remote**

- Built community insights dashboard (Python + Streamlit + MySQL) surfacing editor contribution trends
- Reduced SQL query execution time **~25%** via composite indexing on replicated production datasets
- Authored reusable Python query modules with unit tests, eliminating ad-hoc analysis scripts
- Contributions merged after international code reviews under Wikimedia engineering standards

---

## 🛠️ Tech Stack

<div align="center">

#### Languages
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)

#### Backend
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=for-the-badge&logoColor=white)

#### Frontend
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Tailwind](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=for-the-badge&logo=three.js&logoColor=white)

#### Data & AI
![PostgreSQL](https://img.shields.io/badge/PostgreSQL+pgvector-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)

#### Cloud & DevOps
![GCP](https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

</div>

---

## 🏆 Certifications & Recognition

<div align="center">

![GCP](https://img.shields.io/badge/Google_Cloud-Associate_Cloud_Engineer-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-Certified_Cloud_Practitioner-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)

**🥇 1st Place** — ACM Programming Contest (200+ participants)

</div>

---

## 📊 GitHub Stats

<div align="center">

<img height="180" src="https://github-readme-stats-sigma-five.vercel.app/api?username=PavanBollepalli&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true&hide_border=true&bg_color=0D1117&title_color=00D8FF&icon_color=00D8FF&text_color=FFFFFF"/>
<img height="180" src="https://github-readme-stats-sigma-five.vercel.app/api/top-langs/?username=PavanBollepalli&layout=compact&langs_count=8&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00D8FF&text_color=FFFFFF"/>

<img src="https://github-readme-streak-stats.herokuapp.com/?user=PavanBollepalli&theme=tokyonight&hide_border=true&background=0D1117&stroke=00D8FF&ring=00D8FF&fire=00D8FF&currStreakLabel=FFFFFF&sideLabels=FFFFFF&currStreakNum=00D8FF&sideNums=00D8FF"/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=PavanBollepalli&theme=tokyo-night&hide_border=true&bg_color=0D1117&color=00D8FF&line=00D8FF&point=FFFFFF"/>

</div>

---

<div align="center">

**Building things that work at scale — not just things that compile.**

<img src="https://komarev.com/ghpvc/?username=PavanBollepalli&color=00D8FF&style=flat-square&label=Profile+Views"/>

</div>
