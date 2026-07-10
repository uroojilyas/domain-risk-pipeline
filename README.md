# Domain Legitimacy Scanner (n8n)

A robust n8n workflow for verifying company domain legitimacy. It replaces fragile web scraping with OSINT (RDAP lookups) and AI-driven analysis to assess domain risk.

## How it works

1. **Input:** Accepts a URL or Company Name (auto-resolves via SerpApi if only the name is provided).
2. **Enrichment:** Performs an **RDAP lookup** to get objective registration data.
3. **Intelligence:** **Google Gemini** analyzes the data for risks (age, registrar, naming).
4. **Storage:** Automatically logs the final verdict into **Airtable**.

## Setup Instructions

1. **Import:** Drag & drop the `workflow.json` into your n8n canvas.
2. **Configure Credentials:** Add your API keys for:
* Google Gemini (AI Analysis)
* SerpApi (Domain resolution)
* Airtable (Data logging)


3. **Map Airtable:** Ensure your Airtable columns match the mapping below.
4. **Activate:** Hit **"Activate"** to start the workflow.

## Airtable Schema

Ensure your Airtable Base has these exact columns:

| Column Name | Type |
| --- | --- |
| **Company Name** | Single line text |
| **Created Date** | Date |
| **Expiry Date** | Date |
| **Registrar** | Single line text |
| **Company URL** | URL |
| **Domain Age in days** | Number |
| **Verdict** | Single Select |
| **Analysis** | Long Text |
| **Risk Score** | Number |

---

*Note: Make sure to remove your personal API keys from the JSON file before sharing it publicly on GitHub.*
