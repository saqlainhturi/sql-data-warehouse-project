# Data Warehouse & Analytics Portfolio Project

This repository walks through the full lifecycle of building a data warehouse and turning it into usable business insight — starting from raw CSV exports and ending with SQL-driven reporting on customer behavior, product performance, and sales trends. I put this together as a hands-on portfolio piece to practice and demonstrate core data engineering and analytics skills.

---

## 🏗️ How the Data Flows (Medallion Architecture)

The warehouse is organized in three layers, each with a specific job:

![Data Architecture](docs/data_architecture.png)

| Layer | Purpose |
|---|---|
| **Bronze** | Raw ingestion — CSV files loaded as-is into SQL Server, no transformation applied |
| **Silver** | Cleaning layer — standardizing formats, fixing data quality issues, normalizing structure |
| **Gold** | Business layer — data reshaped into a star schema, ready for reporting and analysis |

---

## 📖 What's Inside

The project covers four main pieces of work:

1. **Architecture design** — structuring the warehouse across Bronze/Silver/Gold layers
2. **ETL scripting** — pulling data from source systems, transforming it, and loading it into the warehouse
3. **Data modeling** — building fact and dimension tables optimized for querying
4. **Reporting & analytics** — writing SQL to surface actionable business metrics

This makes it a useful reference point for anyone working toward roles like SQL Developer, Data Engineer, ETL Developer, Data Modeler, or Data Analyst.

---

## 🚀 Project Scope

### Part 1 — Building the Warehouse (Data Engineering)

**Goal:** Consolidate sales data from two separate source systems into one SQL Server warehouse that supports clean, reliable reporting.

**What that involved:**
- Pulling in CSV exports from both an ERP and a CRM system
- Identifying and resolving data quality issues before anything hit the analytics layer
- Merging both sources into a single, analysis-friendly model
- Working only with the most current snapshot of data (no historical tracking in this version)
- Documenting the model clearly enough for both technical and non-technical stakeholders to follow

### Part 2 — Turning Data Into Insight (Analytics & Reporting)

**Goal:** Use SQL to answer real business questions around:
- Customer behavior
- Product performance
- Sales trends

Full breakdown of requirements: [docs/requirements.md](docs/requirements.md)

---

## 📂 Repo Layout

```
data-warehouse-project/
│
├── datasets/                           # Raw ERP + CRM source files
│
├── docs/                               # Architecture docs and diagrams
│   ├── etl.drawio                      # ETL methods and techniques used
│   ├── data_architecture.drawio        # Overall system architecture
│   ├── data_catalog.md                 # Field-level dataset documentation
│   ├── data_flow.drawio                # End-to-end data flow diagram
│   ├── data_models.drawio              # Star schema / data model diagram
│   ├── naming-conventions.md           # Naming standards for tables/columns/files
│
├── scripts/                            # All SQL logic, split by layer
│   ├── bronze/                         # Raw extraction & load scripts
│   ├── silver/                         # Cleaning & transformation scripts
│   ├── gold/                           # Final analytical model scripts
│
├── tests/                              # Data quality / validation scripts
│
├── README.md
├── LICENSE
├── .gitignore
└── requirements.txt
```

---

## 🛡️ License

Released under the [MIT License](LICENSE) — free to use, adapt, and share with attribution.

---

## 🙏 Credit

The overall structure of this project (Medallion architecture, layer breakdown, repo layout) follows the Data Warehouse project format taught by **Data With Baraa**. I built and implemented everything in this repo myself as a learning exercise, adapting the approach along the way.

---

## 👤 About Me

I'm **Saqlain Haider** — currently working in data operations on a large-scale logistics system at Qiddiya (250+ contracting companies, 2,000+ daily vehicle movements tracked), and building a career in BI and analytics. 

- 📧 saqlainhturi@gmail.com
