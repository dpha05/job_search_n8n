# Phase 1: Lead Scraping & Deduplication
**n8n Automated data extraction from LinkedIn & StartupJobs.cz with vector-based filtering.**

---

![System Demo](assets/demo.gif)

---

### 📊 Highlights
* **71% Noise Filtering:** Two-stage Regex targets only relevant listings and data for the database.
* **Direct XML/HTML Extraction:** 11-node custom parser extracts data directly from raw source code (0 cost and maintenance).
* **Semantic Deduplication:** 95% Cosine Similarity threshold (via pgvector) prevents duplicate leads across different sources.
* **Modular Structure:** Designed to accept new sources (e.g., Google Sheets) by mapping to a unified schema.

---

### 🎥 Video Walkthrough (100 Seconds)

[![Video Walkthrough Preview](https://img.youtube.com/vi/P3Jgx5Q_dyU/0.jpg)](https://www.youtube.com/watch?v=P3Jgx5Q_dyU)

---

### 🖼️ n8n Workflow Screenshots

**LinkedIn scraper:**
![LinkedIn Scraper Preview](assets/screenshot_linkedin.png)

**Startupjobscz scraper:**
![Startupjobscz Scraper Preview](assets/screenshot_startupjobscz.png)

**Vector Deduplication Logic:**
![Deduplication Preview](assets/screenshot_dedupe.png)

---

### 📂 Technical Documentation
* [**Raw JSON Workflows**](01_lead_scraper/workflows/)
* [**Detailed Technical README**](README.md)

---
[← Return to Portfolio](https://linktr.ee/dpha05)
