# Blockchain AML Fraud Detection & Network Analysis

## Executive Summary
This repository contains an end-to-end data pipeline and heuristic detection engine designed to uncover money laundering networks on the blockchain. Utilizing the Elliptic Bitcoin Transaction Dataset, the pipeline transforms raw ledger data into a mathematical Directed Graph to isolate structural hubs and surface advanced Anti-Money Laundering (AML) evasion typologies.

## Key Features & Typologies Detected
Instead of relying on predictive black-box AI, this engine utilizes strict, defensible network metrics (Betweenness Centrality, PageRank, In/Out-Degree) to identify specific, automated criminal behaviors:
* **Layering (Mixers):** High-velocity hubs receiving and dispersing funds simultaneously.
* **Fan-Out (Evasion):** Automated splitting of large sums across 10+ destinations instantly.
* **Peeling Chains:** Long, low-volume chains acting as continuous obfuscation bridges.
* **Funnelling (Smurfing):** Consolidation wallets gathering funds from 20+ unique sources.
* **Cold Storage:** Accumulation endpoints acting as pre-cash-out holding vaults.

## Tech Stack
* **Data Processing:** `pandas`, `numpy`
* **Graph Theory & Network Topography:** `networkx`
* **Interactive Visualization:** `pyvis`, `plotly`
* **Reporting:** `fpdf` (Automated PDF generation)
* **Environment:** Google Colab / Jupyter Notebook

## Deliverables Generated
When executed, the pipeline automatically compiles and exports the following deliverables:
1. `cleaned_merged_data.csv` - The sanitized master dataset.
2. `dashboard.html` - A self-contained, interactive HTML/JS dashboard featuring a 3D network map and transaction velocity charts.
3. `compliance_report.pdf` - An executive memorandum detailing the highest-risk nodes and actionable AML recommendations.
4. `data_decisions.log` - An automated audit trail of all data cleansing and imputation decisions.

## How to Run Locally
1. Clone this repository: `git clone https://github.com/yourusername/blockchain-aml-analysis.git`
2. Install dependencies: `pip install pandas numpy networkx pyvis plotly fpdf kaggle`
3. Ensure your `kaggle.json` API token is configured in your local environment to download the Elliptic dataset.
4. Execute the Jupyter Notebook or Python script to generate the deliverables in your working directory.