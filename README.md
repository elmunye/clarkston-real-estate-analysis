# Clarkston Real Estate Market Analysis: Data-Driven Development Strategy

This repository contains the comprehensive market analysis and strategic development program for **Project PMA**, a 500,000+ SF mixed-use project in **Clarkston, GA**. This work was completed as a core component of a **Capstone project for the Master’s in Real Estate Development (MRED) at Georgia Tech**.

The analysis leverages Python-based data science workflows to evaluate market feasibility, moving beyond traditional static reports to provide dynamic, high-conviction development recommendations.

## 📍 Market Area Definitions
Recognizing that different asset classes draw from distinct geographic pools, the analysis utilizes specific primary market areas (PMA) to measure demand:

* **Multifamily & Residential:** Analyzed using **2-mile and 5-mile radii** to capture immediate neighborhood demand and the broader commuter base.
* **Senior Housing:** Evaluated within a **5-mile to 8-mile radius** to account for the larger catchment area required for specialized independent and assisted living services.
* **Retail:** Focused on a localized **trade area** driven by grocer-anchored daily-needs traffic and local spending patterns.
* **Office:** Measured against an **8-mile regional radius** to capture major employment clusters and competitive Class A inventory within the Northlake and Stone Mountain submarkets.

---

## 📈 Analytical Workflow & Notebooks
The repository is organized by specific asset classes and analytical goals. Each notebook documents the methodology for calculating capture rates, vacancy trends, and supply-demand equilibrium.

### 01. Demographic Segmentation (`01_demand_side_demographics.ipynb`)
Identifies high-conviction target cohorts based on localized growth. Performs linear interpolation of household age and income distributions (2025–2030) to identify specific "addressable renter" pools for multifamily and senior products.

### 02. Multifamily Supply & Pipeline Analysis (`02_multifamily_supply.ipynb`)
Stress-tests the proposed unit mix against existing and future inventory. Analyzes pipeline data to calculate capture rates, identifying a structural shortage of **10,911 Class A units** against a pipeline of only ~2,000.

### 03. Employment-Driven Office Dynamics (`03_office_gis_jobs.ipynb` & `04_office_supply_demand_analysis.ipynb`)
Uses GIS linkage to connect regional job growth to local office space demand. Findings revealed a structurally loose market (**29.1% vacancy**), leading to a strategic recommendation to pivot from speculative office to a **medical/community-office** niche.

### 04. Retail Market & Feasibility (`05_retail_market_analysis.ipynb`)
Validates demand for **826,000+ SF of retail by 2030**, supporting the feasibility of a grocer-anchored district with sub-7% current vacancy.

### 05. For-Sale Housing & Appreciation Forecasting (`06_for_sale_housing_market.ipynb` & `07_home_value_appreciation_forecast.ipynb`)
Evaluates home ownership trends and deploys **Prophet time-series modeling** to forecast home value appreciation through 2028, projecting a long-run CAGR of **5.59%** for for-sale townhome products.

---

## 🏗️ Proposed Development Program
The following program was optimized through the data-driven insights found in this analysis, addressing specific, unmet community needs.

**Total Residential Units:** 275 | **Total Leaseable Area:** ~496,000 SF

| Product Type | Target Segment | Strategic Rationale | Exit Strategy |
| :--- | :--- | :--- | :--- |
| **Townhomes (3-5BR)** | Multigenerational Families | Sized for seniors living with adult children. | For Sale |
| **Senior (IL/AL)** | Segment 1 Seniors | Fills a projected **637-unit shortage** by 2029. | Hold / Yr 10 Sale |
| **Multifamily (1-2BR)** | Young Professionals | Captures the region's rising young professional base. | Hold / Yr 10 Sale |
| **Multifamily (4BR)** | Affordable/Sec. 8 | Explicit inclusion of documented affordable demand. | Hold / Yr 10 Sale |
| **Retail + Grocer** | Local Trade Area | Anchors the district for daily-needs traffic. | Hold / Yr 10 Sale |
| **Office (Medical)** | Community Services | Targeted niche to avoid broad Class A office vacancy. | Hold / Yr 10 Sale |

---

## 📂 Repository Structure
```text
├── notebooks/
│   ├── 01_demand_side_demographics.ipynb
│   ├── 02_multifamily_supply.ipynb
│   ├── 03_office_gis_jobs.ipynb
│   ├── 04_office_supply_demand_analysis.ipynb
│   ├── 05_retail_market_analysis.ipynb
│   ├── 06_for_sale_housing_market.ipynb
│   └── 07_home_value_appreciation_forecast.ipynb
├── requirements.txt         # Necessary Python libraries for replication
└── README.md                # Project documentation