# India-s-agricultural-crop-production-analysis
Interactive Tableau dashboard analyzing India's agricultural crop production (1997–2021) across states, seasons, and crops. Built for farmers, policy analysts, and investors to uncover trends and make data-driven agricultural decisions. Includes data preprocessing, dashboards, and a Tableau Story.

Live Dashboard: https://public.tableau.com/app/profile/divya.kauluri/viz/IndiaAgricultureanalysisproject

An interactive Tableau dashboard analyzing Indian crop production data from 1997 to 2021, covering 36 states, 57 crops, and 345,407 records. The project covers the full workflow from raw data cleaning to dashboard design, storytelling, and performance testing.

## Overview

Agricultural crop data in India is publicly available but exists mainly in static government reports. This makes it difficult for different stakeholders to draw insights:

- Farmers cannot easily see seasonal trends for their region
- Policy analysts cannot quickly compare production across states
- Investors have no simple way to identify high-growth crops

This project addresses that by transforming the raw dataset into an interactive dashboard suited to each of these use cases.

## Data Preparation

The raw dataset contained 345,407 rows with no relational structure. It was cleaned using Python and Pandas:

- Removed duplicate and blank records
- Standardized state and crop names to prevent inconsistencies in the map visualization
- Derived a numeric Crop Year field for trend analysis
- Added two calculated fields:
  - Yield: Production divided by Area
  - Production Normalized: adjusts for crops measured in different units (tonnes, bales, nuts)
- Scaled Area and Production into millions for readability on chart axes

Cleaned dataset file: `skillwallet_crop_cleaned.xlsx`

## Worksheets

| # | Worksheet | Description |
|---|-----------|--------------|
| 1 | KPI Summary | National-level averages for yield, area, and production |
| 2 | Trend of Yield | Yield trend from 1997 to 2021, peaking around 2018 |
| 3 | State Map | State-wise production shown geographically |
| 4 | Cultivated Area by Crop | Rice and wheat account for the largest cultivated area |
| 5 | State-wise Cultivated Area | Uttar Pradesh and Madhya Pradesh lead in cultivated area |
| 6 | Leading States by Production | Ranks states by total production |
| 7 | Year-wise Production | National production trend over time |
| 8 | Production by Unit Type | Breaks down production by measurement unit; shows Kerala's ranking is driven by coconuts measured in nuts rather than tonnage |
| 9 | Season-wise Production | Production distribution across growing seasons |

## Dashboards

- Overview: combines all nine worksheets into a single view
- Farmer's View: season-wise production, yield trend, and cultivated area by crop
- Policy Analyst's View: state map, cultivated area comparison, and yield trend
- Investor's View: year-wise production and leading states, paired with the unit-type breakdown for accurate interpretation

## Story

A five-part guided Tableau Story is included, covering an overview followed by three scenario walkthroughs (farmer, policy analyst, investor), concluding with a summary of the dataset's value across audiences.

## Performance Testing

Eight performance tests were conducted prior to publishing:

- Filter response time: approximately 1.1 seconds for the map, under 1 second for the yield trend chart (target was under 3 seconds)
- All charts, dashboard actions, and story transitions were tested across Chrome, Edge, and Safari with no defects found

## Repository Structure
India-s-agricultural-crop-production-analysis/

├── README.md

├── India Agriculture analysis project.twb

├── India's Agricultural Crop Production Analysis(1997-2021).xlsx

├── skillwallet_crop_cleaned.xlsx

└── document/

├── 1. Ideation Phase/

├── 2. Requirement Analysis/

├── 3. Project Design Phase/

├── 4. Project Planning Phase/

├── 5. Performance Testing/

├── 6. Documentation and Demo/

│   ├── Final_Report.docx

│   └── demo audio.mp4

└── 7. Project Development Phase/

├── 1. Preprocessing Steps and Business Questions.pdf

├── 2. Dashboard and Story Screenshots.pdf

└── 3. Dataset Description.pdf

## Tech Stack

- Tableau Public for dashboard design and publishing
- Python (Pandas) for data cleaning and preprocessing
- Excel for raw and cleaned data storage

## Demo

A complete walkthrough of the project is available as a video in `document/6. Documentation and Demo/`.
