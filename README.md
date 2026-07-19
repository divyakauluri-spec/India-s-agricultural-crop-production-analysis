# 🌾 India's Agricultural Crop Production Analysis

**Interactive Tableau dashboard analyzing 25 years of India's agricultural crop production (1997–2021) — built for farmers, policy analysts, and investors to uncover trends and make data-driven agricultural decisions.**

Agricultural data in India is publicly available but exists mainly in static government reports. This project transforms 345,407 raw records into an interactive Tableau solution — 9 visualizations, 4 role-specific dashboards, and a guided Story — published free on Tableau Public for anyone to explore without installing software or creating an account.

---

## 🔗 Quick Links

| Resource | Link |
|---|---|
| 📊 **Live Dashboard (Overview)** | [public.tableau.com/.../IndiaAgricultureanalysisproject](https://public.tableau.com/app/profile/divya.kauluri/viz/IndiaAgricultureanalysisproject) |
| 📖 **Guided Story Walkthrough** | [.../IndiasAgricultureJourney](https://public.tableau.com/app/profile/divya.kauluri/viz/IndiaAgricultureanalysisproject/IndiasAgricultureJourney?publish=yes) |
| 💻 **This Repository** | [github.com/divyakauluri-spec/India-s-agricultural-crop-production-analysis](https://github.com/divyakauluri-spec/India-s-agricultural-crop-production-analysis) |

---

## 📌 Overview

Agricultural crop data in India is publicly available but scattered across static government reports, making it difficult for different stakeholders to draw insights:

- **Farmers** cannot easily see seasonal trends for their region
- **Policy analysts** cannot quickly compare production across states
- **Investors** have no simple way to identify high-growth, lower-risk crops or regions

This project addresses that gap by transforming the raw dataset into a single interactive Tableau workbook tailored to all three audiences — covering the full workflow from raw data cleaning to dashboard design, storytelling, and performance testing.

**Dataset coverage:** 36 states/union territories · 57 crop types · 6 growing seasons · 25 years (1997–2021) · 345,407 records

---

## 🎯 Key Features

- **KPI Summary Panel** — instant national baseline (Average Yield, total Area, total Production)
- **State-wise Production Map** — geographic view of regional disparities
- **Trend of Agricultural Yield** — 25-year productivity trend line
- **Cultivated Area by Crop** — national land-use benchmarking
- **State-wise Cultivated Area Comparison** — regional land-base ranking
- **Leading States by Production** — top-producing states
- **Year-wise Total Production** — national growth trajectory
- **Production Distribution by Unit Type** — exposes mixed-unit (Tonnes/Bales/Nuts) distortion in raw rankings
- **Season-wise Production** — aligns with India's cropping calendar
- **3 Role-Specific Dashboards** — Farmer's View, Policy Analyst's View, Investor's View
- **5-Point Guided Story** — "India's Agricultural Journey: Insights from 25 Years of Data"

---

## 👥 Who This Is For

| Persona | Question They Need Answered | How the Dashboard Helps |
|---|---|---|
| 🧑‍🌾 **Rajesh** — Small-scale farmer, Uttar Pradesh | Which crops/seasons perform best in my region? | Farmer's View: Season-wise Production, Yield Trend, Cultivated Area by Crop |
| 🏛️ **Ananya** — Government policy analyst | Which regions are low-yield and need resource allocation? | Policy Analyst's View: Production Map, Cultivated Area Comparison, Yield Trend |
| 💼 **Vikram** — Agribusiness investor | Which states/crops are high-growth and lower-risk? | Investor's View: Total Production Trend, Leading States, Unit-Type Distribution |

---

## 🛠️ Technology Stack

| Layer | Technology |
|---|---|
| Data Source | CSV — Government crop production extract, 1997–2021 |
| Data Cleaning | Python 3.12, Pandas |
| Visualization & Dashboards | Tableau Desktop / Tableau Public |
| Geographic Mapping | Tableau built-in Mapbox |
| Publishing | Tableau Public (free hosting) |
| Version Control | GitHub |

---

## 🧹 Data Preparation

The raw government CSV (345,407 rows) was cleaned and enriched using Python/Pandas before connecting to Tableau:

1. Removed duplicate and blank rows
2. Standardized State and Crop name spellings
3. Derived `Crop_Year_Numeric` from the text-based year field for continuous time-axis charts
4. Calculated `Yield` = Production ÷ Area
5. Calculated `Production_Normalized` to reduce distortion from mixed measurement units (Tonnes, Bales, Nuts)
6. Scaled Area and Production to millions for readable chart axes
7. Exported the cleaned dataset as `skillwallet_crop_cleaned.csv`

**Known limitation:** 2021 figures are partial-year, since government year-end reporting was incomplete at the time of data collection — visible as a dip at the end of trend charts.

Full preprocessing steps and data dictionary: [`document/7. Project Development Phase/`](./document/7.%20Project%20Development%20Phase/)

---

## 📁 Repository Structure

All project deliverables are organized inside the `document/` folder, following the 7-phase project structure:

```
document/
├── 1. Ideation Phase/              → Problem Statement, Empathy Map, Brainstorming
├── 2. Requirement Analysis/        → Customer Journey Map, Solution Requirement,
│                                      Data Flow Diagram, Technology Stack
├── 3. Project Design Phase/        → Problem-Solution Fit, Proposed Solution,
│                                      Solution Architecture
├── 4. Project Planning Phase/      → Product Backlog, Sprint Planning
├── 5. Performance Testing/         → Performance Testing Report
├── 6. Documentation and Demo/      → Final Report, Demonstration Video
└── 7. Project Development Phase/   → Preprocessing Steps & Business Questions,
                                       Dashboard & Story Screenshots,
                                       Dataset Description
```

Other files in the repository root:
- `India Agriculture analysis project.twb` — Tableau workbook source file
- `skillwallet_crop_cleaned.xlsx` — cleaned dataset used by the workbook

---

## 📊 Business Questions Answered

| # | Question | Answered By |
|---|---|---|
| 1 | What is India's overall agricultural performance at a glance? | KPI Summary panel |
| 2 | Has national crop yield improved or declined over 25 years? | Trend of Agricultural Yield |
| 3 | Which states/regions produce the most, and where should investment focus? | State-wise Production Map |
| 4 | Which crops occupy the most cultivated land nationally? | Cultivated Area by Crop |
| 5 | Which states have the largest agricultural land base? | State-wise Cultivated Area Comparison |
| 6 | Which states generate the highest production volume? | Leading States by Production |
| 7 | How has total national production grown year over year? | Year-wise Total Production |
| 8 | Are production rankings distorted by mixed measurement units? | Production Distribution by Unit Type |
| 9 | Which growing season should be prioritized for a given crop? | Season-wise Production |

Full detail with screenshots: [`document/7. Project Development Phase/1. Preprocessing Steps and Business Questions.pdf`](./document/7.%20Project%20Development%20Phase/)

---

## 🎬 Demonstration Video

A full screen-recorded walkthrough of all dashboards and the Story, with narration, is available in:
[`document/6. Documentation and Demo/`](./document/6.%20Documentation%20and%20Demo/)

---

## 👤 Author

**Divya Kauluri**
[GitHub](https://github.com/divyakauluri-spec) · [Tableau Public Profile](https://public.tableau.com/app/profile/divya.kauluri)

---

## 📄 License

This project uses publicly available government agricultural data for educational and analytical purposes.
