# job_search_automation_n8n

An end-to-end automation pipeline designed to identify high-signal career opportunities by filtering raw data into the top 10% 'Rare' matches. 

---

## 🚀 Phase 1: Lead Scraper
This phase focuses on high-volume, low-cost acquisition of pre-vetted data and consistency.

**Key Highlights**
- **Hydration Map Bypass:** 11-node regex parser to extract data from XML sitemap without the overhead of JS scrapers and reducing cost and maintenance to 0.
- **Multi-Layer Filtering:** two-stage pre-filter using Regex for structured XML, raw HTML extraction and Keyword-matching for API stream to funnel pre-vetted leads.
- **Vector-Based Deduplication:** Cosine Similarity (95% threshold) to prevent database noise, ensuring 100% uniqueness across processed leads.

## 🧠 Phase 2: Lead Qualifier

---

## 🛠️ Tech Stack
- **Orchestration:** n8n
- **Database:** Supabase (PostgreSQL + pgvector)
- **Sources:** LinkedIn API (Apify), StartupJobs.cz (Custom XML Parser)

## 📄 License
This project is licensed under the **MIT License** - feel free to use it for your own job search automation.