# Phase 1: Lead Scraping & Deduplication
**Automated data extraction from LinkedIn & StartupJobs.cz with vector-based filtering.**

<br>

### 📊 Highlights
* **71% Noise Filtering:** Two-stage Regex targets only relevant listings and data for the database.
* **Direct XML/HTML Extraction:** 11-node custom parser extracts data directly from raw source code (0 cost and maintenance).
* **Semantic Deduplication:** 95% Cosine Similarity threshold (via pgvector) prevents duplicate leads across different sources.
* **Modular Structure:** Designed to accept new sources (e.g., Google Sheets) by mapping to a unified schema.

<br>

---

<br>

![](https://github.com/USER/REPO/raw/main/01_lead_scraper/assets/demo.gif)

<br>

---

<br>

### 🎥 Video Walkthrough (100 Seconds)

[![Video Walkthrough Preview](https://img.youtube.com/vi/P3Jgx5Q_dyU/0.jpg)](https://www.youtube.com/watch?v=P3Jgx5Q_dyU)

<br>

---

<br>

### 🖼️ n8n Workflow Screenshots

**LinkedIn scraper:**
![LinkedIn Scraper Preview](assets/screenshot_linkedin.png)

<br>

**Startupjobscz scraper:**
![Startupjobscz Scraper Preview](assets/screenshot_startupjobscz.png)

<br>

**Vector Deduplication Logic:**
![Deduplication Preview](assets/screenshot_dedupe.png)

<br>

---

<br>

### 📂 Technical Documentation
* [**Raw JSON Workflows**](workflows/)
* [**Detailed Technical README**](../README.md)

<br>

---
[← Return to Portfolio](https://linktr.ee/dpha05)
