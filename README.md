# job_search_automation_n8n

An end-to-end autonomous qualification pipeline designed to identify high-signal career opportunities. This system transforms high-volume raw data into a curated 'Rare' match bucket (Top 7%) using hybrid semantic scoring, state-machine logic, and zero-maintenance parsing.

---

## 🚀 Phase 1: High-Precision Ingestion & Deduplication
*Focus: Low-latency data acquisition and database integrity.*

**Technical Architecture:**
- **JS Hydration Bypass:** A custom 11-node regex-based engine extracts data directly from XML sitemaps. By bypassing headless browsers (Puppeteer), infrastructure overhead and execution costs are reduced to near-zero.
- **Unified Schema Normalization:** Implements a "Schema Bridge" via Set Nodes, merging disparate sources (LinkedIn API, XML Parsers, Manual G-Sheet Entry) into a standardized PostgreSQL structure.
- **Semantic State Protection:** Uses **95% Cosine Similarity** (via `pgvector`) on job descriptions to detect "multi-posted" roles across different boards, ensuring 100% database uniqueness.

## 🧠 Phase 2: The Hybrid Qualification Engine
*Focus: Semantic understanding paired with consistent, zero-hallucination logic.*

**Technical Architecture:**
- **Two-Stage Filtering:**
    - **Stage 1 (Technical Guardrail):** A 70/30 hybrid pass using Cosine Similarity against a "Technical Anchor" to auto-reject non-technical or low-level roles.
    - **Stage 2 (The Deep Dive):** A parallel 3-branch scoring architecture evaluating Similarity, Core Pillars (Mission/Responsibilities), and Benefits.
- **Dual-Strategy Hallucination Prevention:**
    - **High-Context Prompting:** Uses **Gemini 1.5 Flash** with detailed scoring tiers and few-shot examples for mission-critical pillars like **Strategic Autonomy**.
    - **Boolean Logic Extraction:** Offloads high-volume benefit checks (30+ questions) to **Llama 3 (Groq)**, feeding raw booleans into a **Boring Code Node** for weighted scoring with zero AI-drift.
- **State-Driven Self-Healing:** A daily 9:00 AM "State Sync" workflow identifies leads stuck in transient statuses (e.g., `passed_title`) and re-routes them back into the processing pipeline for 100% fault tolerance.

## 🛠️ Tech Stack
- **Orchestration:** n8n (Self-hosted)
- **Database:** Supabase (PostgreSQL + `pgvector`)
- **AI Models:** Gemini 3.0 Flash, Llama 4 Maverick on Groq
- **Vector Embeddings:** Gemini embedding 1 (1536D)
- **Notifications:** Pushover API (Asynchronous Priority Alerts)

---

## 📈 System Performance
| Metric | Result |
| :--- | :--- |
| **Noise Reduction** | 71% Auto-Rejected |
| **High/Rare Matches** | TOP 7-8% |
| **Mid and Low Matches** | 10-12% each |
| **Manual Effort Saved** | ~1 Hour Daily |

## 📄 License
This project is licensed under the **MIT License**.
