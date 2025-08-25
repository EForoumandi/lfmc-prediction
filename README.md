# LFMC Prediction with Daymet & SOLUS

Predict **Live Fuel Moisture Content (LFMC)** by fusing meteorological variables from **Daymet** and soil attributes from **SOLUS** in a workflow.

- **Notebook**: `LFMC_prediction.ipynb`  
- **Environment**: Python 3.10+ (tested with Jupyter)  
- **Data folder**: `./data` (inputs)

---

## 1) Quickstart

### A. Clone and install
```bash
git clone https://github.com/EForoumandi/lfmc-prediction.git
cd lfmc-prediction
```

### B. Run
```bash
jupyter lab   # or: jupyter notebook
```
Open `LFMC_prediction.ipynb` and run **top-to-bottom**.  
The notebook uses **relative paths** only.

---

## 2) Inputs & Data

This project expects:

- **Daymet**: daily Daymet variables (e.g., Tmin, Tmax, precipitation, VPD, shortwave radiation).  
- **SOLUS**: soil attributes (e.g., texture, depth, hydrologic group, derived properties).

---

## 3) Project Structure
```
.
├─ LFMC_prediction.ipynb    # Main, submission-ready notebook
├─ requirements.txt         # Python dependencies
├─ data/                    # Small sample inputs (not large/raw data)
└─ README.md
```

---

## 4) Modeling Overview

- **Target**: LFMC  
- **Features**:
  - *Dynamic*: Daymet (Tmin/Tmax/precip/VPD/etc.)
  - *Static*: SOLUS (texture/depth/hydrologic group)
- **Split**: Prefer **spatiotemporal splits** (train/validation/test) to avoid leakage.

---

## 5) Citation & License

Please cite **Daymet** and **SOLUS** when using this workflow.  
