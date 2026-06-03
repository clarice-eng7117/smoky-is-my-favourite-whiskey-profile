# Spatial Data Science & Machine Learning Analysis of Scottish Whisky Flavor Profiles

This repository contains a spatial data science and machine learning project evaluating the relationship between traditional Scottish whisky regions and actual chemical flavor dimensions across 86 operational distilleries. 

By combining spatial statistics (Global Moran's I) with unsupervised clustering (K-Means) and supervised classification (Random Forests), this study evaluates whether historical geographic designations function as distinct, reliable sensory profiles or merely cultural marketing boundaries.

---

## 🗺️ Spatial Network & Regional Boundaries

Below is a map of Scotland marking the analyzed distilleries and their spatial connections generated using a 4-Nearest Neighbors approach:

<p align="center">
  <img src="scotland_whisky_map.png" alt="Map of Scotland Whisky Distilleries" width="75%">
  <br>
  <sub><i>Map source: Charles MacLean, "Understanding Scotch Malt Whisky" (The Council of Whiskey Masters)</i></sub>
</p>

---

# Spatial Data Science & Machine Learning Analysis of Scottish Whisky Flavor Profiles

This repository contains a spatial data science and machine learning project evaluating the relationship between traditional Scottish whisky regions and actual chemical flavor dimensions across 86 operational distilleries. 

By combining spatial statistics (Global Moran's I) with unsupervised clustering (K-Means) and supervised classification (Random Forests), this study evaluates whether historical geographic designations function as distinct, reliable sensory profiles or merely cultural marketing boundaries.

---

## 📁 Project Structure

```text
.
├── README.md               # Repository landing page with project summary
├── whisky_analysis.Rmd     # Core R Markdown script containing text and code chunks
├── whisky_analysis.html    # Compiled HTML report with interactive elements (TOC)
├── data/
│   └── whisky_distilleries.csv  # Cleaned dataset of the 86 Scottish distilleries
├── images/
│   └── scotland_whisky_map.png  # Map of Scotland with distillery spatial network
└── outputs/
    ├── kmeans_clusters.png # K-Means cluster output plot
    └── rf_importance.png   # Random Forest feature importance chart
```

---

## 📊 Summary of Key Findings

* **Flavor Overlap:** Unsupervised K-Means clustering ($k=5$) successfully isolated the heavily-peated Islay distilleries into a distinct spatial group. However, it completely merged Speyside and the Highlands into the same flavor clusters, proving their physical boundaries do not represent uniquely different flavor profiles.
* **Classification Performance:** A supervised Random Forest model trained to predict a distillery's region based strictly on its taste profile yielded a massive **51.16% Out-of-Bag (OOB) error rate**. The classifier consistently misclassified nearly half of all Highland and Speyside entries as each other, proving their taste profiles are functionally identical on a data level.
* **Primary Spatial Drivers:** Global Moran’s I and feature importance metrics confirm that `Smoky` and `Medicinal` are the only flavor characteristics carrying a strong, clustered regional signature. For all other traits (such as sweetness, fruitiness, or maltiness), Scottish whiskies function as a continuous, overlapping spectrum rather than isolated territories.

---

## 🥃 Project Conclusion

Traditional whisky regions are rich historical, cultural, and marketing designations rather than binding flavor blueprints. While purchasing an **"Islay"** bottle remains a highly reliable shortcut to expect heavy smoke, expecting a **"Highland"** malt to taste inherently different from a **"Speyside"** malt is an organoleptic misconception disproven by spatial data. Ultimately, a distillery’s unique engineering profile-such as still shapes, cut-points, and cask selection which dictates flavor far more heavily than geographic terroir.

---

## 🛠️ Tech Stack & Libraries Used
* **Language:** R
* **Spatial Processing:** `sf`, `spdep`
* **Machine Learning & Stats:** `randomForest`, `stats` (K-Means)
* **Visualization:** `ggplot2`, `factoextra`, `knitr`

---

## 🤖 AI Usage Disclosure
In alignment with academic transparency standards, generative AI assistance (Gemini) was utilized dynamically throughout this project for codebase troubleshooting (resolving environment errors, package syntax compatibility, and formatting R Markdown features) and structuring the layout of statistical tables. All core data cleaning, exploratory spatial modeling execution, qualitative interpretations, and text narratives were conducted and finalized strictly by the author.
