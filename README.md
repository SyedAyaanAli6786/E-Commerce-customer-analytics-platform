# E-Commerce Business Intelligence & Customer Analytics Platform

## 🎯 Project Overview
A **complete, production‑ready analytics portfolio** that showcases the end‑to‑end workflow of a modern data analyst:
- **Ingest** raw CSV exports from an e‑commerce platform.
- **Clean & transform** data with Pandas (handling missing values, outliers, data types).
- **Feature engineering** to compute RFM scores, customer lifetime value, and cohort identifiers.
- **Persist** cleaned data to PostgreSQL via SQLAlchemy.
- **Run advanced SQL** (CTEs, window functions, sub‑queries) for sales, product, and delivery analysis.
- **Perform** customer segmentation, cohort analysis and churn prediction in Python.
- **Visualise** insights in Jupyter notebooks and Power BI (DAX measures, data model, dashboard design).
- **Automated testing** with pytest to ensure data‑pipeline reliability.

The repository is structured to be easily cloned, set‑up, and extended – perfect for a Computer Science student applying for data‑analyst internships.

---

## 🛠️ Tech Stack
| Layer | Technologies |
|-------|---------------|
| **Programming** | Python 3.11, Pandas, NumPy, SQLAlchemy |
| **Database** | PostgreSQL (local or Docker) |
| **SQL** | Advanced PostgreSQL (CTEs, window functions) |
| **BI** | Power BI, DAX |
| **Visualization** | Matplotlib, Seaborn, Plotly |
| **Testing** | pytest |
| **Version Control** | Git (10 atomic commits) |
| **Documentation** | Markdown, README, docstrings |

---

## 📦 Installation & Setup
1. **Clone the repo**
   ```bash
   git clone git@github.com:SyedAyaanAli6786/E-Commerce-customer-analytics-platform.git
   cd E-Commerce-customer-analytics-platform
   ```
2. **Create a virtual environment**
   ```bash
   python -m venv .venv
   source .venv/bin/activate   # Linux/macOS
   .venv\Scripts\activate    # Windows
   ```
3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
4. **Configure environment variables**
   - Copy `.env.example` to `.env` and fill in your PostgreSQL credentials.
5. **(Optional) Start PostgreSQL via Docker**
   ```bash
   docker run --name pg-ecom -e POSTGRES_PASSWORD=postgres -p 5432:5432 -d postgres:15
   ```
6. **Run the pipeline**
   ```bash
   python main.py run-all   # Executes data load → clean → feature eng → DB load → analysis
   ```

---

## 📂 Repository Structure
```
E-Commerce-Analytics-Dashboard/
├── data/                     # Raw, processed, and exported CSVs
│   ├── raw/
│   ├── processed/
│   └── exports/
├── notebooks/                # Jupyter notebooks for each analysis stage
├── src/                      # Python package (core ETL & analytics)
│   ├── __init__.py
│   ├── config.py
│   ├── database.py
│   ├── data_loader.py
│   ├── data_cleaning.py
│   ├── feature_engineering.py
│   ├── customer_segmentation.py
│   ├── cohort_analysis.py
│   ├── analysis.py
│   └── utils.py
├── sql/                      # SQL schema + analytical queries (01‑09)
├── powerbi/                  # DAX measures, data‑model doc, dashboard guide
├── tests/                    # pytest suite for ETL & analytics functions
├── main.py                   # CLI entry‑point
├── requirements.txt
├── .env.example
├── .gitignore
└── README.md                 # (this file)
```

---

## 🚀 Quick Start Guide
```bash
# Load raw CSVs (if you have your own data, place them in data/raw/)
python main.py download-data
# Run the full ETL & analysis pipeline
python main.py run-all
# Open a notebook to explore results
jupyter notebook notebooks/01_data_exploration.ipynb
```
The final analytical outputs are stored in `data/exports/` (CSV) and the PostgreSQL database, ready to be consumed by Power BI.

---

## 📊 Power BI Integration
1. Import the CSV files from `data/exports/` into Power BI.
2. Apply the data‑model described in `powerbi/data_model.md`.
3. Use the ready‑made DAX measures in `powerbi/dax_measures.dax` for:
   - Total Revenue, Gross Margin, Average Order Value
   - RFM‑based segment KPIs
   - Cohort retention curves
4. Follow the step‑by‑step dashboard build guide in `powerbi/powerbi_build_guide.md`.

---

## 🧪 Testing
Run the automated test suite to ensure the pipeline works as expected:
```bash
pytest -v tests/
```
The tests cover data cleaning edge cases, feature‑engineering correctness, and basic SQL‑query validation.

---

## 🤝 Contributing
Feel free to fork the repo and submit pull requests. Please follow these steps:
1. Create a feature branch.
2. Make atomic commits (max 10 as per project guideline).
3. Ensure all tests pass.
4. Open a PR with a concise description.

---

## 📄 License
This project is licensed under the **MIT License** – see the `LICENSE` file for details.

---

## 📞 Contact
Created by **Syed Ayaan Ali** – [GitHub Profile](https://github.com/SyedAyaanAli6786)

---

*Happy analysing!*
