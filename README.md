# Clarkston Real Estate Market Analysis

Real estate market analysis for Clarkston, GA, prepared in support of **Project PMA**. The work links demographic demand signals to multifamily, office, retail, and for-sale housing market conditions.

## Project objective

Evaluate whether supply–demand dynamics support the proposed mixed-use development program.

## Key market findings (summary)

The points below condense the sector work in the full memorandum. They are drawn from **ESRI, CoStar, BLS, and ARC**; detailed pulls and methods sit in the numbered notebooks. Milestone years in the source table include **2029** and **2030** for demand and pricing checkpoints. **Time-series absorption forecasts in this repo emphasize the period through 2028** (see **Forecasting horizon**), while these benchmarks describe the broader supply–demand framing.

**Senior housing (IL + AL)** — Existing assisted-living stock is on the order of **3,777** units (CoStar), with pipeline near **151** units (roughly **1%** annual delivery pace). Demand is estimated at about **4,565** units (2029), implying a shortage of roughly **637** units versus the supply path. Rents are bracketed near **$3,400–$4,000** per unit (2025), with a 2029 target band near **$3,700–$3,936** (about **$5.25–$6.17** PSF). Modeled rent growth is about **5%**; the workup cites a capture rate near **14%**.

**Multifamily (Class A)** — Against roughly **9,834** existing units and about **1,994** units in pipeline (deliveries, under construction, and planned), addressable renters near **22,739** (2029) imply a shortage on the order of **10,911** units. Rents near **$2.33** PSF trend toward **$2.41** PSF with rent growth about **1.2%**. Vacancy is about **11.6%** currently, with a long-run reference near **10%**; capture rate about **3%**.

**Retail (Class A)** — Inventory is roughly **2.86M SF**, with notable pipeline including about **320,000 SF** (Lulah Hills). Demand is sized near **826,717 SF** by **2030**, with incremental new demand about **95,178 SF** (2025–2030). NNN rents move from about **$32** toward **$36** PSF with rent growth near **4%**. Current vacancy near **6.3%** sits below a long-run reference near **7.45%**; capture rate about **7.3%**.

**Office (Class A)** — Inventory is very large (about **22.1M SF**) with minimal near-term deliveries (about **25,195 SF**) against new demand about **994,890 SF** (2026–2029), but available supply by **2029** is on the order of **5.4M SF** in the same framing—i.e., a structurally loose market. Rent growth is modest (about **1.4%**); all-class and Class A gross rents near **$36.62** and **$41.54** PSF appear alongside a roughly **$36.98** PSF gross reference. Current vacancy is elevated (about **29.1%**) versus a long-run reference near **16.5%**; capture rate about **5.7%**.

**Read-across for Project PMA** — The sector stack supports relatively stronger demand pressure for **senior and Class A multifamily**, **supportive retail fundamentals** (especially where grocer and daily needs anchor traffic), and **conservative treatment of office** at the aggregate Class A level—even if a discrete medical or community-office slice still merits a location-specific narrative.

## Project PMA: principles and analytical standards

The analysis is organized around four operating principles. Each principle is paired with a concrete anchor—either a measurable feature of the program or a traceable step in the workbook sequence—so readers can see how judgment is supported by evidence.

**1. Data-driven decisions**

Conclusions are tied to observable market and demographic inputs, not to narrative alone. Where proprietary sources cannot be shared, the notebook sequence still documents the logic, filters, and outputs that follow from those inputs.

- **Anchor:** Demand-side segmentation and growth context are established first (`01_demand_side_demographics.ipynb`); supply and sector checks build on that baseline in later notebooks.

**2. User- and stakeholder-centric framing**

The development program is expressed as specific household scenarios and service needs (multigenerational townhomes, senior IL/AL, young-professional units, Section 8, grocer-anchored retail, medical/community office). Analysis choices are meant to answer whether those uses have a plausible market path, not whether a generic “mixed-use” label fits.

- **Anchor:** The program table below names **target segments** and **scenarios** for each product; notebooks test whether external indicators are consistent with that mix.

**3. Scalability and flexibility of the work product**

The repository is structured so additional geographies, time windows, or stress cases can be re-run without rewriting the core flow. Notebooks are ordered so outputs from earlier steps feed later ones.

- **Anchor:** Recommended run order (demographics → multifamily supply → office → retail → for-sale → appreciation) matches how institutional reviewers typically expect a market story to compound.

**4. Sustainability and ethics of presentation**

Assumptions that materially affect conclusions—such as exclusion windows in time series, forecast horizon, or hold/sale timing—are stated plainly so the analysis can be scrutinized and updated.

- **Anchor:** For-sale townhomes are modeled separately from hold-to-year-10 rental and commercial; forecasting for absorption scenarios is capped at **2028** (see **Forecasting horizon** below).

---

## Program structure (analysis workflow)

This is the analytical analogue of a phased program: each phase has an objective, a primary artifact, and a place in the sequence.

| Phase | Objective | Key activities | Primary notebooks |
| :--- | :--- | :--- | :--- |
| **Foundational** | Establish demand and demographic context | Segment review, growth and composition checks, linkage to proposed unit types | `01_demand_side_demographics.ipynb` |
| **Intermediate — residential supply** | Ground-truth competitive and pipeline pressure | Multifamily supply inventory and delivery context | `02_multifamily_supply.ipynb` |
| **Intermediate — employment & office** | Relate jobs and office geography to office program | GIS/jobs linkage, office supply–demand framing | `03_office_gis_jobs.ipynb`, `04_office_supply_demand_analysis.ipynb` |
| **Intermediate — retail** | Test retail and grocer feasibility against trade-area dynamics | Retail demand/supply and competitive context | `05_retail_market_analysis.ipynb` |
| **Advanced — for-sale & value** | Stress-test ownership product and long-run value context | For-sale absorption / pricing context, home-value outlook | `06_for_sale_housing_market.ipynb`, `07_home_value_appreciation_forecast.ipynb` |

---

## Data points used to evaluate the program

These are the main categories of evidence the notebooks assemble. They function as evaluation criteria: the program is more credible when multiple independent checks point in the same direction.

| Evaluation lens | What we ask of the data | Program tie-in |
| :--- | :--- | :--- |
| **Demographic depth** | Are the proposed segments (e.g., seniors, young professionals, multigenerational households) visible in the market story? | Segment labels in the program table |
| **Residential scale** | Does competitive supply suggest room for **275** units and the stated mix? | Unit counts by product |
| **Commercial scale** | Does the trade area support roughly **120,000** leaseable SF of retail + office (before load factors)? | Retail and office rows |
| **Ownership velocity** | Does for-sale housing behavior support townhome absorption assumptions? | For-sale townhome block |
| **Long-horizon prudence** | Are forward views bounded to a horizon where models remain interpretable? | Forecasts through **2028** where applicable |

---

## Proposed development program

**Rationale**

The layout is built around households that do not fit a single typical unit profile. The townhome block is sized for **multigenerational living**—seniors sharing a home with adult children and grandchildren—with bedroom counts and square footages tied to named scenarios. The rental stack forms a **continuum**: independent and assisted living for seniors (Segment 1), market-rate housing for young professionals, and a dedicated **Section 8** component so affordable demand is explicit in the program, not an afterthought.

Retail and office are included so the site supports **daily needs and services**: ground-floor retail with a grocer and office space oriented to medical and community uses. That supports a walkable mixed-use district and diversifies income beyond residential rent.

**Capital logic** is explicit: townhomes are **for sale**; multifamily, retail, and office are modeled as **hold with a sale in year 10**, reflecting different liquidity profiles for for-sale equity versus stabilized operating assets.

**1. Proposed development program**

| Product | Target segment | Scenario | Units | SF / unit | Leaseable SF | Gross SF | % of total | Parking (min) | Exit strategy |
| --- | --- | --- | ---: | ---: | ---: | ---: | ---: | ---: | --- |
| Townhome — 3BR, 2BA | Segment 5 | Senior + Daughter + 2 Kids | 30 | 1,800 | 54,000 | 54,000 | 10.0% | 30 | For Sale |
| Townhome — 4BR, 3BA | Segment 5 | Senior + Daughter + 3 Kids | 30 | 2,200 | 66,000 | 66,000 | 12.2% | 30 | For Sale |
| Townhome — 4BR, 3BA | Segment 5 | Senior + Couple + 3 Kids | 20 | 2,500 | 50,000 | 50,000 | 9.2% | 20 | For Sale |
| Townhome — 5BR, 3.5BA | Segment 4 | Senior Couple + Adult Couple + 3 Kids | 15 | 2,800 | 42,000 | 42,000 | 7.8% | 15 | For Sale |
| Senior IL (1BR) | Segment 1 | Senior Independent Living | 40 | 750 | 30,000 | 37,500 | 6.2% | 30 | Hold / Yr 10 Sale |
| Senior AL (1BR) | Segment 1 | Senior Assisted Living | 50 | 600 | 30,000 | 40,000 | 7.4% | 38 | Hold / Yr 10 Sale |
| Multifamily — Young Prof (1BR) | Young Professional | Young Professional Single | 40 | 750 | 30,000 | 33,333 | 6.9% | 40 | Hold / Yr 10 Sale |
| Multifamily — Young Prof (2BR) | Young Professional | Young Professional Couple | 20 | 1,000 | 20,000 | 22,222 | 3.9% | 20 | Hold / Yr 10 Sale |
| Multifamily — Affordable (4BR) | Sec. 8 | Affordable / Section 8 | 30 | 1,800 | 54,000 | 60,000 | 11.7% | 30 | Hold / Yr 10 Sale |
| Retail | Retail | Ground Floor Retail + Grocer | — | — | 60,000 | 63,158 | 11.7% | 300 | Hold / Yr 10 Sale |
| Office Space | Office | Office Space (Medical + Community) | — | — | 60,000 | 70,588 | 13.0% | 300 | Hold / Yr 10 Sale |
| **Total** | | | **275** | | **496,000** | **538,802** | **100%** | **853** | |

---

## Forecasting horizon (2028)

Forward-looking views in this repository intentionally emphasize the period through **2028** rather than pushing a single unified forecast deep into 2029. Real estate markets absorb policy, financing, and migration shocks unevenly; time-series and structural models both lose precision as the horizon lengthens. Capping the primary absorption and scenario work at 2028 keeps the outputs tied to a planning window where assumptions can still be stress-tested and communicated clearly to **Project PMA** stakeholders. Where notebooks still display sensitivity or longer tails, the **2028** framing remains the reference case for decision-grade summary metrics.

---

## Repository structure

- `data/` — source and intermediate files used by notebooks
- `notebooks/` — step-by-step analysis notebooks in recommended run order

## Recommended notebook order

1. `notebooks/01_demand_side_demographics.ipynb`
2. `notebooks/02_multifamily_supply.ipynb`
3. `notebooks/03_office_gis_jobs.ipynb`
4. `notebooks/04_office_supply_demand_analysis.ipynb`
5. `notebooks/05_retail_market_analysis.ipynb`
6. `notebooks/06_for_sale_housing_market.ipynb`
7. `notebooks/07_home_value_appreciation_forecast.ipynb`

## Data

Raw CoStar extracts used in parts of this work cannot be redistributed here. For questions on data, contact elyasmunye@gmail.com.

## Notes

- File paths use project-relative references for portability.
- Data files retained in-repo support reproduction where licensing allows.
