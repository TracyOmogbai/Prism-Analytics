# Prism-Analytics
An interactive Power BI dashboard that benchmarks digital marketing performance across companies, platforms, and audiences, turning a messy real-world dataset into a clear narrative about what works and what wastes budget.

# 📊 Prism Analytics — Where Marketing Spend Meets Strategy

![Overview Dashboard](https://raw.githubusercontent.com/TracyOmogbai/Prism-Analytics/main/screenshots/overview.png)

---

## Overview

Prism Analytics is an internal marketing intelligence dashboard commissioned by a holding company that owns and operates four brand divisions: **DataTech Solutions, NexGen Systems, Innovate Industries, and TechCorp**. Each brand runs its own independent digital marketing campaigns across multiple channels, audience segments, and geographic markets.

The dashboard consolidates all four brands' 2021 campaign data into a single unified view, enabling the holding company's marketing leadership to benchmark performance across divisions, identify which brands are spending efficiently, and surface actionable recommendations for budget reallocation.

**Author:** Tracy Omogbai
**Tools:** Power BI Desktop, Power Query, DAX
**Dataset:** Kaggle — Digital Marketing Campaign Performance 2021

---

## Business Problem

Each of the four brand divisions was running marketing campaigns independently with no unified view of performance across the group. The holding company's VP of Marketing needed to answer:

- Which brand divisions are acquiring customers most efficiently?
- Which channels deliver the best return on marketing spend across all brands?
- Which audience segments convert best and on which channels?
- Which specific campaigns and UTM sources are actually driving conversions?
- Where should budget be reallocated across divisions to maximise group-wide performance?

Without a consolidated dashboard, these questions could only be answered by manually comparing four separate reports — time-consuming, inconsistent, and prone to error.

---

## Key Findings

### Brand Division Performance

| Company | Total Spend | Conversions | CVR | CPA | vs Group Avg |
|---------|-------------|-------------|-----|-----|-------------|
| DataTech Solutions | $3,115K | 9,977 | 2.8% | $312 | -9.7% ✅ |
| NexGen Systems | $3,290K | 9,598 | 2.9% | $343 | -0.9% |
| Innovate Industries | $5,802K | 16,850 | 2.7% | $344 | -0.4% |
| TechCorp | $3,564K | 9,190 | 2.7% | $388 | +12.2% ❌ |

**Key Result:** DataTech Solutions is the most efficient brand division operating 9.7% below the group average CPA. TechCorp sits 12.2% above average and requires urgent budget and targeting review.

### Channel Performance

| Channel | Total Spend | Conversions | CVR | CPA |
|---------|-------------|-------------|-----|-----|
| Google Ads | $2,500,237 | 8,235 | 2.7% | $303.61 ✅ |
| Facebook Ads | $2,355,730 | 7,184 | 2.8% | $327.91 |
| YouTube | $2,905,100 | 8,277 | 3.0% | $350.98 |
| Instagram Ads | $2,589,059 | 6,950 | 2.6% | $372.53 |
| Website Ads | $2,141,396 | 5,723 | 2.7% | $374.17 ❌ |

**Key Result:** Google Ads delivers the lowest CPA at $303.61 across all brand divisions — 19% cheaper than Website Ads. Group-wide reallocation away from Website Ads toward Google Ads is recommended.

### Audience Performance

| Segment | CVR | Standout Insight |
|---------|-----|-----------------|
| Health & Fitness | 2.82% ✅ | Best converting segment across all brands |
| Fashionistas | 2.78% | 90% CTR on Email — underutilised combination |
| Tech Enthusiasts | 2.76% | Lowest CPA segment |
| Foodies | 2.75% | Consistent mid-tier performer |
| Outdoor Adventurers | 2.72% ❌ | Lowest CVR — creative refresh needed |

**Key Result:** Health & Fitness is the strongest converting segment group-wide. Fashionistas show outstanding 90% CTR on Email campaigns suggesting significant untapped potential in that channel-segment combination.

---

## Dashboard Pages

### Overview
Executive summary for holding company leadership showing group-wide KPIs, spend and conversion trends, conversion funnel, top campaigns, and a brand division comparison snapshot.

![Overview](https://raw.githubusercontent.com/TracyOmogbai/Prism-Analytics/main/screenshots/overview.png)

---

### Companies
Cross-brand benchmarking page showing the full division scorecard with all KPIs compared against the group average, CVR ranking, campaign type mix per brand, and a platform CVR heatmap across all divisions.

![Companies](https://raw.githubusercontent.com/TracyOmogbai/Prism-Analytics/main/screenshots/companies.png)

---

### Channels
Channel efficiency analysis across all brand divisions showing full channel scorecard, spend vs conversions scatter plot, and CTR vs CVR side-by-side comparison.

![Channels](https://raw.githubusercontent.com/TracyOmogbai/Prism-Analytics/main/screenshots/channels.png)

---

### Audiences
Audience segment performance analysis showing CVR ranking across all segments, segment × channel CTR heatmap, and a spend vs CPA bubble chart sized by total conversions.

![Audiences](https://raw.githubusercontent.com/TracyOmogbai/Prism-Analytics/main/screenshots/audience.png)

---

### Attribution
UTM tracking analysis showing which sources, mediums and campaign tags are driving conversions group-wide, including a conversion funnel by UTM medium and ranked campaign performance table.

![Attribution](https://raw.githubusercontent.com/TracyOmogbai/Prism-Analytics/main/screenshots/Attribution.png)

*Screenshot coming soon*

---

## Data Model

Built on a star schema in Power BI with a central Facts table connected to seven dimension tables:

| Table | Type | Description |
|-------|------|-------------|
| Facts | Fact table | One row per campaign — Spend, Clicks, Impressions, Conversions, UTM fields |
| Dim_Company | Dimension | Brand division names |
| Dim_Channels | Dimension | Marketing channel names |
| Dim_Segment | Dimension | Audience segment names |
| Dim_CampaignType | Dimension | Campaign type categories |
| Dim_UTM | Dimension | UTM source, medium and campaign tags |
| Dim_Language | Dimension | Language dimension |
| Date_Dim | Date table | Full calendar table for time intelligence |
| CalcMeasures | Measures table | All DAX measures |

---

## Data Cleaning

The original dataset required significant cleaning before analysis:

- Removed null date rows to ensure a clean time axis starting from January 2021
- Standardised numeric and currency columns
- Resolved column naming inconsistencies inherited from the flat source file
- Normalised UTM fields for consistent attribution analysis across all divisions

---

## Tools Used

- **Power BI Desktop** — data modelling, DAX measures, dashboard design
- **Power Query** — data cleaning and transformation
- **DAX** — calculated measures including TOPN patterns, SWITCH funnel visual, and vs Group Average benchmarking
- **PowerPoint** — wireframe design and layout planning
- **GitHub** — version control and portfolio hosting

---

## Connect

**LinkedIn:** [Tracy Omogbai](https://www.linkedin.com/in/tracyomogbai)

---

*Prism Analytics — Breaking down campaign data into clear, actionable insight.*
