# -Formula-1-Crash-Analysis

# 🚦 NYC Traffic Fatalities Analysis: A Data-Driven Exploration of Risk Factors

> **"Every crash has a context — our goal is to decode it through data."**

This project conducts an in-depth analysis of traffic-related fatalities in New York City using Vision Zero crash data. By exploring the **who**, **where**, and **when** of fatal incidents, the study aims to identify systemic patterns and high-risk zones that can inform smarter urban policy and safer infrastructure planning.

---

## 📌 Project Overview

**🎯 Objective:**  
To uncover how geographic, temporal, and behavioral factors contribute to traffic fatalities across NYC neighborhoods. The goal is to identify vulnerable areas and groups, and evaluate the effectiveness of interventions like the **Vision Zero** initiative.

---

## 🗃️ Repository Structure

```
├── nycfatalities.ipynb        # Main Jupyter notebook with analysis and visualizations
├── data/                      # (Optional) Folder for raw and cleaned datasets
├── figures/                   # (Optional) Folder for exported charts/maps
├── README.md                  # Project overview and documentation
└── requirements.txt           # Dependencies (optional but recommended)
```

---

## 🧭 Data Sources

- **NYC Vision Zero Crash Data**  
  [Motor Vehicle Collisions - NYC Open Data](https://data.cityofnewyork.us/Transportation/Motor-Vehicle-Collisions-Vehicle-Information/bm4k-52h4)

- Supplemental datasets from:
  - NYC Department of Transportation (DOT)
  - NYPD Open Data Portals
  - Census Tract demographic overlays *(optional enhancement)*

---

## 🛠️ Tools & Techniques

**Programming Language:**  
Python (Jupyter Notebook)

**Core Libraries:**
- `pandas`, `numpy` – Data processing
- `matplotlib`, `seaborn` – Visualizations
- `geopandas` – Mapping and spatial analysis
- `statsmodels`, `scipy` – Statistical tests and regression modeling

**Analysis Methods:**
- Descriptive statistics
- Spatial clustering (heatmaps)
- Temporal trend analysis
- Hypothesis testing (t-tests, chi-square)
- OLS regression modeling

---

## 📊 Sample Code Snippet

```python
# Flagging fatal crashes
df['fatal_crash'] = df['NUMBER OF PERSONS KILLED'] > 0

# Grouping by borough to identify fatality hotspots
borough_fatalities = df[df['fatal_crash']].groupby('BOROUGH').size().sort_values(ascending=False)

# Visualizing the results
borough_fatalities.plot(kind='bar', title='Fatal Crashes by Borough', color='crimson')
```

---

## 📈 Key Insights

- 🚧 **Brooklyn and Bronx** emerged as boroughs with the highest concentration of fatal crashes.
- 🌙 Fatalities peak during **late night hours and weekends**, often tied to alcohol use and low visibility.
- 🧍 Pedestrians account for a **disproportionate share** of deaths, especially in intersections lacking crosswalks.
- 📉 While Vision Zero launched in 2014 aimed to reduce fatalities, **progress has been uneven** across neighborhoods.

---

## 💡 Reflections & Future Work

**Challenges Faced:**
- Addressing missing geospatial coordinates and borough fields
- Normalizing time formats and inconsistent incident descriptions

**What I’d Do Differently:**
- Integrate demographic and income layers to assess equity
- Test machine learning models (e.g., Random Forests) to predict high-risk zones

---

## 🚀 How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/nyc-traffic-fatalities.git
   cd nyc-traffic-fatalities
   ```

2. **(Optional) Create a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # or venv\Scripts\activate on Windows
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch the notebook:**
   ```bash
   jupyter notebook nycfatalities.ipynb
   ```

---

## 📎 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

## 👤 Author

**Sai Hemanth Varma**  
Graduate Student, Business Analytics – SUNY Albany  
📧 [hemanthv196@gmail.com] |  

---

## ⭐ Acknowledgments

- NYC Open Data  
- Vision Zero NYC Initiative  
- Course: *Data Science for the Public Good – Spring 2025*

---

## 📍Preview

> ![Heatmap of NYC Fatalities](figures/nyc_heatmap.png)  
> *Visualizing high-risk zones using crash coordinates and borough boundaries.*
