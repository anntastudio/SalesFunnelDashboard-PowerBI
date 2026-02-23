# Sales Funnel Analytics Power BI Dashboard
Sales funnel analytics dashboard tracking conversions, revenue, and user segments across acquisition channels with interactive filtering and dynamic formatting built in DAX.

<br>
Dashboard Preview

https://github.com/user-attachments/assets/baab0509-0423-483a-9a75-fb06f1ac9eea

<br>

## 🗂️ Data Modeling
- Designed a **star schema** with fact and dimension tables: `fact_funnel`, `fact_user_events`, `dim_user`, `dim_product`, `dim_date`, `dim_traffic_source`
- Established proper relationships across the model to support efficient, accurate cross-filtering and aggregation
  
<br>

## 📐 DAX Measure Development
- Created a dedicated `#Metrics` measures table with **15+ custom DAX measures**
- Measures include: `Revenue Rank`, `Conversion Rate`, `Total Orders`, `Total Revenue`, `Segment Share`, `Paid Revenue Share`, and conditional display measures for dynamic formatting
- Separated raw calculation logic from display logic to keep the model clean and maintainable
  
<br>

## 📊 Visualization Design
Built a multi-visual single-page dashboard featuring:
- **Conversion Funnel** bar chart tracks drop-off at each funnel stage
- **Decomposition Tree** drills into acquisition channel performance
- **Revenue Over Time** line chart with date hierarchy drill-through (Year → Quarter → Month → Day)
- **Subscriber Segmentation** breakdown by age group and user segment
- **KPI Summary Cards** at-a-glance headline metrics
- **App Subscriptions Table** product-level detail including tier, category, conversion rate, and revenue
  
<br>

## 🎛️ Interactivity & UX
- Implemented dynamic filtering with **10 slicers** covering channel, device, user segment, product, date range, category, and tier
- Built a custom label-switch slicer using a **field parameter pattern** (`LblSwitch`) to let users toggle between metric views without changing the underlying visuals, improving flexibility while keeping the layout clean
  
<br>

## 💼 Business Domain
- Subscription/SaaS funnel analytics covering traffic-to-conversion tracking, revenue performance, user segmentation, and product-tier analysis
- Metrics like `Avg LTV`, `Conversion Rate`, and `Paid Revenue Share` reflect a product analytics mindset and familiarity with how SaaS businesses measure growth and monetization efficiency
