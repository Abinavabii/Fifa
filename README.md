<p align="center">
  <img src="banner.webp" alt="FIFA World Cup 26 - Players Banner" width="25%">
</p>
<h1 align="center"> FIFA World Cup 26 — Power BI Dashboard</h1>
<p align="center">
  <b>Players & Team Analysis</b> — An interactive Power BI report exploring player stats,
  team performance, and country-wise breakdowns for the FIFA World Cup.
</p>
<p align="center">
  <img src="https://img.shields.io/badge/Power%20BI-Desktop-yellow?logo=powerbi&logoColor=black">
  <img src="https://img.shields.io/badge/DAX-Measures-blue">
  <img src="https://img.shields.io/badge/Status-Completed-success">
</p>
---
 
## 📌 Overview
 
This project is an interactive **Power BI dashboard** built around FIFA World Cup 26 player and
team data. It covers three connected report pages — **Dashboard**, **Player Details**, and
**Country Details** — with drill-through navigation, tooltips, and custom DAX measures for
deeper analysis of player and country performance.
 
---
 
## 🖥️ Report Pages
 
### 1. 🏠 Dashboard (Home)
The main landing page with high-level KPIs and visual summaries:
- **KPI Cards:** Total Countries (48), Total Minutes (16K), Total Matches (182)
- **Goals** — Top scorers bar chart *(with custom tooltip enabled)*
- **Assists** — Top assist providers bar chart
- **Players by Position** — Donut chart (FWD / MID / DEF / GK breakdown, Total Players)
- **Shot on Target** — Country-wise ranked bar chart
- **Decomposition Tree** — Total Saves broken down by Country → Player → Position
### 2. 👤 Player Details
A detailed, sortable, and color-formatted table of every player, including:
- Full Name, Country, Position
- Pass Accuracy *(custom measure)*
- Goals, Tackles, Assists
- Total Minutes *(custom measure)*
- Conditional formatting (data bars / color scales) for quick visual comparison
### 3. 🌍 Country Details
A geographic and comparative view of country performance:
- **Map visual** showing participating countries
- **Clean Sheets** table by country
- **Goals** and **Assists** bar charts by country
---
 
## 🔗 Interactivity
 
- **Tooltip Page:** A custom tooltip was built and applied to the **Goals** bar chart on the
  Dashboard page, showing extra player/team detail on hover.
- **Drill-through:** Configured from the Dashboard's bar chart visuals to both the
  **Player Details** and **Country Details** pages, allowing users to right-click a player or
  country and jump straight to the detailed view.
- **Filters Panel:** Slicers for Position, Goals, and Players on the Dashboard page.
---
 
## 🧮 DAX Measures
 
Custom measures created for this report include:
 
| Measure | Description |
|---|---|
| `Pass_accuracy` | Calculated pass accuracy percentage per player |
| `Total Minutes` | Total minutes played, aggregated per player/country |
| `Total Goals` | Sum of goals scored |
| `Total Assists` | Sum of assists made |
| `Total Matches` | Total matches played |
| `Total Players` | Distinct count of players |
| `Goals per Match` | Goals scored divided by matches played |
 
 
---
 
## 🗂️ Data Model
 
The report is built on three core tables:
- **players** 
- **countries / country** — country reference and lookup data
- **statistics** — player-level statistics: `AKS`, `APP`, `AS`, `BL`, `CS`, `GS`, `INT`, `KP`, `MP`, `Pass_accuracy`
Along with player attributes: `firstName`, `lastName`, `full_name`, `playerid`, `position`,
`shortName`, `squadId`, `status`, `feedId`, `fifaId`.
 
---
 
## 🛠️ Tech Stack
 
- **Power BI Desktop** — report authoring
- **DAX** — custom measures & calculated columns
- **Power Query (M)** — data cleaning & transformation
- **Bing Maps visual** — country map on the Country Details page
---
 
