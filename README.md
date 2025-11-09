# Solar Data Discovery Challenge

## Overview
Repository for the 10 Academy Solar Data Discovery interim challenge. Focus: Git setup, EDA on solar farm data from Benin, Sierra Leone, and Togo to inform MoonLight Energy Solutions' investment strategy.

## Setup Instructions
To reproduce the environment locally:

1. **Clone the Repo:**  
   ```
   git clone https://github.com/Samuel-0228/solar-challenge-week1.git
   cd solar-challenge-week1
   ```

2. **Set Up Virtual Environment:**  
   ```
   python -m venv .venv
   # Activate:
   # Mac/Linux: source .venv/bin/activate
   # Windows: .venv\Scripts\activate
   ```

3. **Install Dependencies:**  
   ```
   pip install -r requirements.txt
   ```

4. **Run Notebooks:**  
   Install Jupyter if needed: `pip install jupyter` (temporary—add to requirements later).  
   ```
   jupyter notebook  # Opens browser; navigate to notebooks/
   ```

5. **Test CI Locally (Optional):**  
   Install `act` CLI for GitHub Actions simulation: Follow [act docs](https://github.com/nektos/act).  
   ```
   act
   ```

## Folder Structure
- **.github/workflows/**: CI/CD pipelines (e.g., ci.yml for dep installs & checks).
- **notebooks/**: Jupyter notebooks for EDA (e.g., benin_eda.ipynb for profiling, cleaning, and plots like GHI histograms).
- **src/**: Core Python scripts (e.g., data cleaning functions—placeholder for now).
- **scripts/**: Utility scripts (e.g., data export—placeholder).
- **tests/**: Unit tests (e.g., for outlier detection—add pytest later).
- **data/**: Local CSVs (e.g., benin_clean.csv)—ignored in .gitignore; never commit!

## Usage
- **EDA Example:** Open `notebooks/benin_eda.ipynb` → Run cells for data summary & quick viz (uses fake data placeholder).
- **Dashboard (Bonus):** Once app/ ready: `streamlit run app/main.py`.
- **Commits:** Use conventional: `feat:`, `fix:`, `docs:`, etc.

## Challenges & Notes
- **CI Status:** Runs on push/PR—installs deps, checks Python version. Debugged pywin32 issue for cross-platform.
- **Data:** Place CSVs in data/ locally (e.g., from challenge download). Focus: GHI/DNI trends for solar potential.
- **Next:** Full EDA branches (eda-sierra-leone, eda-togo); cross-country compare.

For questions: Check tutorials or community Slack. Built with Python 3.12.

**Author:** Samuel Yeshambel  
**Last Updated:** November 09, 2025
