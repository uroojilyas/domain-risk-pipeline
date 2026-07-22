# Domain Legitimacy Scanner (n8n)

The Domain Legitimacy Scanner is an n8n automation pipeline designed to assess company domain risk by replacing fragile web scraping with objective OSINT data and AI analysis.

**Pipeline Overview:**

* **Input & Resolution:** Accepts a company URL or name, automatically resolving names to URLs via SerpApi if needed.
* **Data Enrichment:** Performs an RDAP lookup to gather objective domain registration data (such as creation and expiry dates).
* **AI Intelligence:** Leverages Google Gemini to analyze the registration details for potential risks (evaluating age, registrar, and naming patterns).
* **Data Storage:** Automatically logs the final verdict, risk score, detailed analysis, and registration details into Airtable.
