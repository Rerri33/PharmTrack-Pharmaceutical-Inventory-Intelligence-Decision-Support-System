# 💊 PharmTrack – Pharmaceutical Inventory Intelligence & Decision Support System

### Power BI | SQL | Power Query | DAX | Healthcare Business Intelligence

**Project Status:** Active Development | Portfolio Project | BI Prototype

PharmTrack is a pharmaceutical inventory intelligence and decision support system designed to improve pharmacy inventory visibility, monitor expiry exposure, analyse medication demand, and support data-driven purchasing decisions.

Inspired by firsthand experience in pharmacy operations, the project applies business intelligence and data analytics to address inventory challenges such as medication stockouts, expiry-related losses, and inefficient stock monitoring.

---

## 📌 Table of Contents

1. [Business Problem](#-business-problem)
2. [Project Objectives](#-project-objectives)
3. [Dataset Overview](#-dataset-overview)
4. [Technology Stack](#-technology-stack)
5. [System Architecture](#-system-architecture)
6. [Core Analytical Features](#-core-analytical-features)
7. [Inventory Intelligence Logic](#-inventory-intelligence-logic)
8. [Key Business Findings](#-key-business-findings)
9. [Dashboard Preview](#-dashboard-preview)
10. [Business Recommendations](#-business-recommendations)
11. [Project Limitations](#-project-limitations)
12. [Future Development](#-future-development)
13. [Skills Demonstrated](#-skills-demonstrated)
14. [Author](#-author)

---

## 🔍 Business Problem

Pharmacy inventory management often relies on manual monitoring and reactive purchasing decisions.

This creates operational challenges, including:

- Critical medications becoming unavailable.
- Pharmaceutical products approaching expiry without timely intervention.
- Poor visibility into inventory movement.
- Inefficient purchasing and replenishment decisions.
- Difficulty identifying fast-moving and slow-moving medications.

During my experience in pharmacy operations, I observed situations where critical medications were unavailable while other products remained on shelves until they expired.

PharmTrack was developed to address these challenges through structured data analysis, inventory intelligence, and interactive business intelligence reporting.

---

## 🎯 Project Objectives

The primary objective is to develop a data-driven pharmaceutical inventory monitoring and decision support system.

The project focuses on:

- Improving inventory visibility.
- Identifying products approaching expiry.
- Monitoring low-stock and reorder conditions.
- Analysing pharmaceutical sales and demand patterns.
- Evaluating product and category performance.
- Supporting better purchasing and inventory management decisions.
- Reducing potential inventory waste and medication shortages.

---

## 📊 Dataset Overview

The current analytical model consists of structured pharmaceutical product, sales, and inventory datasets.

### Product Dataset

| Attribute | Description |
|---|---|
| Total Products | 234 |
| Therapeutic Categories | 22 |
| Inventory Classifications | 7 |
| Product ID | Custom product identifiers |
| Product Information | Product names and classifications |

Inventory classifications include bulk tablets, topicals and orals, cold-chain biologics, controlled drugs, and consumables and OTC hygiene products.

### Transaction Dataset

| Attribute | Description |
|---|---|
| Data Period | 2022–2024 |
| Data Type | Sales and inventory transaction records |
| Purpose | Sales, demand, and inventory analysis |

The datasets were structured and transformed to support relational data modelling and business intelligence reporting.

---

## 🛠️ Technology Stack

| Technology | Application |
|---|---|
| Microsoft Excel | Source data preparation |
| Power Query | Data cleaning and ETL |
| SQL | Relational database schema design |
| Power BI | Dashboard development and analytics |
| DAX | Business logic and KPI calculations |

---

## 🏗️ System Architecture

PharmTrack follows a structured analytical architecture.

### 1. Data Processing Layer – Power Query

Power Query was used to:

- Clean inconsistent records.
- Standardize product information.
- Transform raw datasets.
- Structure inventory and transaction data.
- Prepare datasets for relational modelling.

### 2. Database Layer – SQL

A relational database structure was designed around three core tables:

- Sales
- Inventory
- DimProduct

Custom product identifiers and relational links were introduced to improve data organization and support future database integration.

### 3. Business Intelligence Layer – Power BI

Power BI serves as the current analytical engine.

DAX calculations and interactive visualizations were developed to monitor inventory performance, sales trends, expiry exposure, and reorder conditions.

---

## 📈 Core Analytical Features

PharmTrack currently provides:

| Feature | Business Purpose |
|---|---|
| Sales Analysis | Monitor revenue performance |
| Unit Sales Analysis | Understand medication demand |
| Expiry Risk Monitoring | Identify products approaching expiry |
| Reorder Monitoring | Identify products below safety thresholds |
| Product Performance | Compare fast-moving and slow-moving products |
| Category Analysis | Evaluate therapeutic category contributions |
| Inventory Health | Monitor inventory conditions |
| Trend Analysis | Understand monthly sales and demand patterns |

---

## ⚠️ Inventory Intelligence Logic

### 1. Expiry Risk Monitoring

A rolling 60-day expiry monitoring approach was implemented.

Products approaching their expiration dates within the defined 60-day window are classified as **At Risk**.

This helps identify inventory requiring timely operational attention.

### 2. Reorder Intelligence

Product-specific reorder thresholds were established based on inventory classifications.

| Product Classification | Reorder Threshold |
|---|---:|
| Bulk Tablets | 500 units |
| Topicals & Orals | 50–100 units |
| Cold-Chain Biologics | 20 units |
| Controlled Drugs | 40 units |
| Consumables & OTC Hygiene | 30 units |

Products falling below their respective thresholds are flagged for reorder monitoring.

These thresholds represent predefined operational rules rather than automatically optimized forecasting recommendations.

---

## 🔎 Key Business Findings

The current analysis identified several important patterns:

**1. Revenue Contribution**

Supplement products contributed approximately 32% of overall revenue.

**2. Therapeutic Category Performance**

Antihypertensive products accounted for over 20% of category sales.

**3. High-Demand Products**

Insulin Glargine, Apixaban, and Lisinopril demonstrated relatively high demand.

**4. Low-Performing Products**

Acetaminophen 325mg and Albuterol Inhaler recorded minimal sales movement, highlighting potential slow-moving inventory and expiry exposure.

**5. Inventory Risk**

Several products were identified within the rolling 60-day expiry-risk window, demonstrating the importance of proactive expiry monitoring.

---

## 📸 Dashboard Preview

The PharmTrack Power BI dashboard contains two analytical views.

### 1. Inventory Intelligence Overview

Provides a high-level summary of:

- Total sales revenue.
- Units sold.
- Inventory at risk.
- Inventory value.
- Reorder count.
- Products approaching expiry.

![PharmTrack Inventory Overview](dashboard/pharmtrack-overview.png)

### 2. Detailed Performance Analytics

Provides deeper insights through:

- Monthly sales trends.
- Monthly unit sales trends.
- Top-performing products.
- Lowest-performing products.
- Therapeutic category contribution.
- Inventory risk monitoring.

![PharmTrack Performance Analytics](dashboard/pharmtrack-analytics.png)

---

## 💡 Business Recommendations

Based on the analytical findings, PharmTrack supports the following operational recommendations:

1. Prioritize products approaching expiry for timely review and possible redistribution.
2. Review purchasing quantities for products with consistently low demand.
3. Monitor critical medications approaching their reorder thresholds.
4. Use historical demand patterns to support replenishment decisions.
5. Monitor product category performance to improve purchasing priorities.
6. Introduce automated inventory alerts to improve proactive stock management.

---

## ⚙️ Project Limitations

The current solution is a Business Intelligence prototype and not yet a fully automated pharmacy management system.

Important considerations:

- The analytical model covers transaction records from 2022–2024.
- Expiry monitoring currently uses a predefined rolling 60-day threshold.
- Reorder thresholds are rule-based.
- Predictive demand forecasting has not yet been implemented.
- SQL schema design has been developed, but full end-to-end database integration remains in development.
- The dashboard does not currently provide live inventory synchronization.

---

## 🚀 Future Development

Planned enhancements include:

- Python-based demand forecasting.
- Predictive inventory intelligence.
- Automated reorder recommendations.
- Streamlit-based pharmacy data entry interface.
- Batch-level inventory tracking.
- Automated expiry and stock alerts.
- Expanded SQL automation workflows.
- End-to-end pharmacy data pipeline integration.

The long-term objective is to evolve PharmTrack into a more integrated pharmaceutical inventory intelligence and decision support platform.

---

## 🧠 Skills Demonstrated

**Business Intelligence & Analytics**
- Power BI
- DAX
- KPI Development
- Dashboard Design
- Data Visualization
- Healthcare Operations Analytics

**Data Processing & Engineering**
- Power Query ETL
- SQL Schema Design
- Relational Data Modelling
- Data Cleaning
- Data Transformation

**Business & Operational Analysis**
- Pharmaceutical Inventory Analytics
- Expiry Risk Monitoring
- Demand Analysis
- Reorder Logic Design
- Business Decision Support

---

## 👩‍💻 Author

**Rerri Rukevwe**

Pharmaceutical Data Analyst | Healthcare BI & Inventory Intelligence

- LinkedIn: https://www.linkedin.com/in/rerri-rukevwe-bb56122a7
- Portfolio: https://datascienceportfol.io/rerrirukwe

---

### Project Note

PharmTrack is an independent portfolio project inspired by real-world pharmacy operational challenges.

It demonstrates the application of business intelligence and data analytics to pharmaceutical inventory management.

**Built with a focus on improving inventory visibility, reducing potential waste, and supporting better healthcare operational decisions.**
