# Sales Funnel Analytics Power BI Dashboard
Sales funnel analytics dashboard tracking conversions, revenue, and user segments across acquisition channels with interactive filtering and dynamic formatting built in DAX.

<br>
Dashboard Preview

https://github.com/user-attachments/assets/baab0509-0423-483a-9a75-fb06f1ac9eea

<br>

## Overview

- Tracks a full **sales/subscription funnel**: Page Views → Sign-ups → Orders → Revenue
- Segments users by **age group, tier (free/paid), device**, and **traffic source**
- Designed for teams tracking **acquisition, conversion, and monetisation** performance

<br>

## Data Model

- **Star schema** with 2 fact tables: `fact_funnel` (funnel steps) and `fact_user_events` (user activity)
- **4 dimension tables**: `dim_user`, `dim_product`, `dim_date`, `dim_traffic_source`
- All calculated measures live in a dedicated `#Metrics` table

<br>

## DAX Measures
All measures are centralised in a dedicated `#Metrics` table, organised into **7 folders** for maintainability:

| Folder | Key Measures | Purpose |
|---|---|---|
| 01. Core Revenue KPIs | `Total Revenue`, `Revenue per User`, `Avg Order Value`, `Avg LTV`, `Paid Revenue Share` | Top-line revenue health and per-user monetisation |
| 02. Funnel Metrics | `Total Users`, `Total Page Views`, `Total Orders`, `Conversion Rate` | Volume and drop-off at each funnel stage |
| 03. Time Intelligence | `Selected Period` | Period-aware calculations that respond to date slicer selections |
| 04. Product Category | `Avg List Price`, `Revenue Rank Display` | Product-level performance and ranking |
| 05. Customer Segment | `Segment Share`, `Avg LTV` | Breakdown of users by tier, age group, and behaviour |
| 06. Channel Acquisition | `Total Page Views`, `Conversion Rate` | Traffic source effectiveness and acquisition efficiency |
| 07. Dynamic Visuals | `LblSwitch`, `Orders Display`, `Revenue Display`, `Middle Lbl Dynamic`, `Right Lbl` | Advanced DAX that drives conditional formatting and label toggling — switching visuals between raw counts and percentages at runtime without duplicating charts |

<br>

## Visuals

| Visual | Purpose |
|---|---|
| 5× KPI Cards | Headline metrics at a glance |
| 1× Bar Chart | Users by age group, segment, and other breakdowns |
| 1× Line Chart | Revenue / activity trends over time |
| 1× Decomposition Tree | Drill-down root cause analysis |
| 1× Funnel Chart | Customised Bar Chart into Funnel with comparison to previous stages |
| 1xTable | Supporting detail and labels with dynamic formatting |
| Custom SVG Background | Branded layout backdrop |

<br>

##  Interactivity

- **10 slicers** filter by date, region, device, channel, segment, tier, product, and more
- **Bookmark navigator + action buttons** for switching between filter groups
- **Cross-filtering** enabled clicking one visual filters the rest
- **Toggle switch** (`LblSwitch`) to flip between raw counts and percentages
