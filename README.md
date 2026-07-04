# bike_shop_brasil_analytics
Interactive Power BI Dashboard for Sales Performance Analysis.
# Bike Shop Brasil - Strategic Performance & Credit Risk Dashboard 📊🚴‍♂️

An enterprise-grade Business Intelligence and Analytics solution developed in **Power BI** to support executive decision-making, historical data integration, and credit risk mitigation for an international bicycle and accessories retailer with operations across Brazil, the United States, and Europe.

> 🔗 **[Click here to access the Live Interactive Dashboard]

> **https://app.powerbi.com/view?r=eyJrIjoiODE1ZTk0MzctZWFmMC00ZTUxLWJlZmUtMzhiNzJlMzMwMDQ5IiwidCI6ImVkNWM4MDE1LWM0YzUtNGU2Yy04NGU0LWE5OTEwNDg4YTYyMiJ9)**
---

## 📷 Dashboard Preview

> 💡 **Tip:** Below you can find the dynamic visuals of the final corporate solution.

<img width="1235" height="689" alt="Captura de tela_2016" src="https://github.com/user-attachments/assets/ce54ebf4-a493-4d90-b0fc-0e5596d6b8f7" />

<img width="1235" height="693" alt="Captura de tela_2017" src="https://github.com/user-attachments/assets/58b5ec75-efbd-4a65-89d8-b3dec02bb6ce" />

<img width="1232" height="689" alt="Captura de tela_2018" src="https://github.com/user-attachments/assets/1d5c96fd-067e-40cf-bf74-3f6956dda9e0" />

<img width="1234" height="689" alt="Captura de tela_2019" src="https://github.com/user-attachments/assets/6757797e-91d1-4f2c-a99c-94b2796a641f" />

---

## 💼 The Business Challenge & Context

In August 2019, the executive board of Bike Shop Brasil was finalizing a highly aggressive 4-year strategic expansion plan. However, leadership faced a critical bottleneck: a severe lack of data visibility over the preceding 4 years (2016–2019) due to corporate restructuring, market expansions, and a **major system migration in September 2018**.

### The Technical Data Gap:
* **Pre-September 2018:** Historical data lived in a legacy system that was decommissioned. Due to technological incompatibilities, these transactions were never migrated to the new environment and existed only as a static relational export.
* **Post-September 2018:** Operational data was captured by a modern, high-volume ERP, with daily automated extracts pushed to a central Data Warehouse (DW).
* **The Bridge:** While transactional data structures were completely incompatible, the master registration tables (Customer IDs, Product Codes, Store Details) remained identical across both eras.

**The Mission:** Act as the strategic BI Analyst to ingest, sanitize, and model these fragmented data sources into a single, unified corporate memory from 2016 onwards, providing numbers-driven certainty to shareholders.

---

## 🛠️ Data Architecture & Implementation

### 1. Advanced ETL & Historical Consolidation (Power Query)
* Appended and unified the historical legacy transaction exports with the modern daily active DW streams.
* Resolved localized formatting discrepancies, managed missing values, and established strict data-type definitions to minimize data storage size and optimize memory footprint.

### 2. Star Schema Data Modeling
Designed a robust, relational **Star Schema** to decouple transactional facts from master dimensional attributes, ensuring sub-second query performance:
* **Fact Tables:** A consolidated `fSales` table merging the two system eras.
* **Dimension Tables:** Standardized master tables for `dCustomers`, `dProducts` (covering bikes, apparel, and accessories), `dStores` (Geographic distribution: Brazil, US, Europe), and a customized `dCalendar` table optimized for Time Intelligence calculations.

### 3. Advanced DAX & Analytics Performance Metrics
Engineered highly optimized measures to supply leadership with deep performance tracking:
* **Volume & Revenue Metrics:** Total Units Sold and Gross Revenue.
* **Portfolio Segmentation:** Dynamic calculation of product category share, sub-category performance rankings, and identification of flagship portfolio drivers.
* **Time Intelligence Storytelling:** Month-over-Month evolution coupled with complex **Same Period Last Year (SPLY)** and Year-over-Year (YoY) growth variance tracking.

---

## 🛡️ Special Feature: Credit Risk & Payment Terms Monitor

Due to a recent surge in delinquency rates and cash flow pressure, the executive board implemented strict strategic constraints regarding client payment credit windows. 

This repository implements a dedicated **Credit Risk Monitoring View** that groups payment terms into strategic clusters and evaluates performance against corporate compliance targets:

| Payment Windows | Strategic Classification | Corporate Target Share |
| :--- | :--- | :--- |
| **Up to 10 Days** | Short-Term (Curto Prazo) / Cash-like | **50%** Target Share |
| **Up to 20 Days** | Medium-Term (Médio Prazo) | **40%** Target Share |
| **Above 20 Days** | Long-Term (Longo Prazo) | Restricted / Minimize |

**Implementation:** Developed explicit segmentation logic in the data layer to dynamically classify transactions, allowing the finance and risk management teams to pinpoint exactly which product lines or geographic regions are exceeding credit safety thresholds.

---

## 📂 How to Explore this Project

1. **[Recommended]** Access the live interactive web version here:

**https://app.powerbi.com/view?r=eyJrIjoiODE1ZTk0MzctZWFmMC00ZTUxLWJlZmUtMzhiNzJlMzMwMDQ5IiwidCI6ImVkNWM4MDE1LWM0YzUtNGU2Yy04NGU0LWE5OTEwNDg4YTYyMiJ9**

2. Alternatively, you can download the `Bike_Shop_Brasil.pbix` file from this repository to review the backend Data Model, Power Query M code, and DAX measures.
3. Open the file using **Power BI Desktop**.

---

## 📬 Contact & Feedback

Developed by **Matheus Luz Alberti** 
* **LinkedIn:** www.linkedin.com/in/matheus-luz-alberti-3ba596170
* **Email:** matheus_luzalberti@hotmail.com
