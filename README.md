# 💻 2024 Stack Overflow Developer Survey Analysis

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Jupyter](https://img.shields.io/badge/Tool-Jupyter_Notebook-orange)
![Pandas](https://img.shields.io/badge/Library-Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Plotly](https://img.shields.io/badge/Library-Plotly-239120?style=for-the-badge&logo=plotly&logoColor=white)

## 📖 Project Overview

This project is a **comprehensive data analysis** of the **2024 Stack Overflow Annual Developer Survey**. The survey, which captures the sentiments, technologies, and career paths of developers globally, provides a rich dataset for exploring current industry trends.

Executed entirely within a **Jupyter Notebook**, this analysis aims to transform the raw survey responses into clear, actionable insights, covering all aspects of the questionnaire from salary and technology preference to AI usage and work environment.

---

## 🎯 Project Objectives & Scope

The primary objective was to deliver a complete, high-fidelity analysis of the entire 2024 dataset. The analysis focused on achieving the following:

* **Comprehensive Coverage:** Analyse **every question** posed in the survey, ensuring no data dimension is overlooked.
* **Replicable Visuals:** Develop visualisations that capture the aesthetic and informative style of the charts presented on the official Stack Overflow survey results website.
* **Interactive Insight:** Utilise interactive charting libraries to allow for deeper, granular exploration of the data (e.g., viewing language trends over time or filtering by experience level).

---

## ⚙️ Technical Stack & Dependencies

The analysis relies on Python's robust data science ecosystem.

### Libraries Installed and Imported

| Library | Primary Use |
| :--- | :--- |
| **Pandas** | Data ingestion, cleaning, manipulation, and complex aggregations. |
| **NumPy** | High-performance numerical operations and array processing. |
| **Matplotlib / Seaborn** | Creation of static, high-quality statistical charts and visualisations. |
| **Plotly / Cufflinks** | Creation of advanced, interactive visualisations (e.g., interactive bar charts, scatter plots with hover text). |

### Installation Instructions

All necessary libraries can be installed using `pip`:

```bash
pip install pandas numpy matplotlib seaborn plotly cufflinks
```

## 📐 Analysis Methodology

The core methodology was designed for efficiency and scalability, specifically addressing the highly repetitive nature of many survey questions (e.g., "Which language have you used?" vs. "Which tool have you used?").

### 1. Modular Function Development (DRY Principle)
Instead of writing dedicated code blocks for each of the 80+ columns, the analysis hinges on **reusable Python functions**.
* **Function Focus:** Functions were developed to handle common survey data structures, such as multi-select columns (where respondents can pick multiple answers) and single-choice categorical data.
* **Flexibility:** The same core functions are used by simply passing different column names (e.g., `LanguageWorkedWith`, `DatabaseWorkedWith`, `WebframeWorkedWith`) to produce consistent analysis and charting.
  
<img width="2030" height="890" alt="image" src="https://github.com/user-attachments/assets/58ca6233-18fe-4885-a724-e79264c8459f" />

<img width="1884" height="1020" alt="image" src="https://github.com/user-attachments/assets/849f012a-24a7-4521-a156-0d527f4e98c6" />



### 2. Visualization Strategy
Visualisations were strategically split based on the requirement for interaction:

* **Static Charts (Matplotlib/Seaborn):** Used for standard distributions, simple counts, and comparisons where interactivity is not required (e.g., Age Distribution, Gender Breakdown).
  
  <img width="1196" height="608" alt="image" src="https://github.com/user-attachments/assets/6d0ad291-2a45-498f-8b87-484f00b93024" />

  <img width="2152" height="897" alt="image" src="https://github.com/user-attachments/assets/88531681-c620-48c2-a22d-5d8c49eae74a" />


* **Interactive Charts (Plotly/Cufflinks):** Essential for ranking top technologies, visualising salary distributions, and allowing drill-down on large datasets. These charts are crucial for exploring relationships between variables.

<img width="1106" height="812" alt="image" src="https://github.com/user-attachments/assets/99c76a2f-4ab9-47f6-b0a5-7e6e5085393c" />

<img width="1112" height="874" alt="image" src="https://github.com/user-attachments/assets/143800ac-e393-4d93-9e6e-b7292ea7cf62" />



---

## 📊 Key Insights & Deliverables

The output is a single, executable Jupyter Notebook containing the full pipeline from raw data import to final visualisation.

### Key Analysis Areas Covered:

1.  **Demographics:** Age, Gender, Education, and Years of Professional Coding Experience.
2.  **Technology Stack:** Ranking of the most popular programming languages, frameworks, databases, and tools.
3.  **Work & Compensation:** Analysis of annual compensation, job satisfaction, and remote work trends.
4.  **AI Adoption:** Insights into how developers are currently using and perceiving AI tools in their workflow.

---

## 🤝 Acknowledgments

This project was built upon the foundation provided by the annual data collection efforts of the Stack Overflow team.

* **Data Source & Inspiration:** The dataset and the inspiration for the analysis methodology and visualisation style are credited to the **Stack Overflow Developer Survey**.
* **Official Survey Link:** [https://survey.stackoverflow.co/](https://survey.stackoverflow.co/)
