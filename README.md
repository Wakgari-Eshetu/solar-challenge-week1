# Solar Challenge — Week 1

This repository collects cleaned minute-resolution meteorological and solar sensor data from three West African sites (Benin — Malanville, Sierra Leone — Bumbuna, and Togo — Dapaong). It contains Jupyter notebooks for exploratory data analysis and cleaned CSVs under `notebooks/data/` to support solar resource assessment and prototype analyses.

Quick start
-----------
1. Create and activate a Python virtual environment (recommended):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Install dependencies:

```powershell
pip install --upgrade pip
pip install -r requirements.txt
```

3. Open and run the notebooks:

```powershell
# from the repository root
jupyter notebook
```

What you'll find here
---------------------
- `requirements.txt` — pinned Python packages used for analysis (pandas, numpy, etc.).
- `notebooks/` — Jupyter notebooks for EDA and comparisons between countries.
	- `notebooks/data/` — cleaned CSVs (benin_clean.csv, sierra_leone_clean.csv, togo_clean.csv).
- `REPORT.md` — concise project report summarizing the repository, datasets, quick findings, and next steps.

Data summary
------------
All cleaned CSVs share this schema (examples): `Timestamp, GHI, DNI, DHI, ModA, ModB, Tamb, RH, WS, WSgust, WSstdev, WD, WDstdev, BP, Cleaning, Precipitation, TModA, TModB, Comments`.

Notes & suggestions
-------------------
- Nighttime irradiance values may be negative or near-zero; treat these as sensor-offset/noise in analyses.
- `ModA`/`ModB` have many zero values in the early rows in the provided samples; confirm whether zeros indicate missing data or actual readings.
- Consider adding a `DATA_DICTIONARY.md` to document units and missing-data conventions, and a small data-validation script in `scripts/`.

Contributing
------------
If you'd like to contribute, please:
1. Open an issue describing the change.
2. Create a branch and include small, focused commits.

Contact / Next steps
--------------------
- See `REPORT.md` for a short analysis and suggested next steps.
- I can add a small data validation script and unit tests if you want — tell me which checks you'd like (schema, duplicate timestamps, basic ranges) and I will add them.

---
Generated: a concise README to help new contributors get started.

# solar-challenge-week1

