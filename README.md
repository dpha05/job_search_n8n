# job_search_n8n

An end-to-end automation pipeline that filters raw job leads down to the top 10% matches using n8n, Supabase, and Cosine Similarity.

Key Highlights
Hydration Map Bypass: 11-node regex parser to extract data from XML sitemap without the overhead of JS scrapers and reducing cost and maintenance to 0.

Multi-Layer Filtering: two-stage pre-filter using Regex for structured XML, raw HTML extraction and Keyword-matching for API stream to funnel pre-vetted leads.

Vector-Based Deduplication: Cosine Similarity (95% threshold) to prevent database noise, ensuring 100% uniqueness across processed leads.
