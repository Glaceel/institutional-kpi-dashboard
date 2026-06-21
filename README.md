# Institutional KPI Dashboard (Research & Publication Performance)

An interactive Power BI dashboard engineered to evaluate, monitor, and optimize institutional research output, publication metrics, and funding efficiency. This dashboard serves as a strategic decision-making tool for academic institutions to track performance metrics against predefined targets across various departments and programs.

*Note: Due to data privacy policies and university regulations, the underlying source data has been omitted. The repository contains the Power BI Template (`.pbit`) showcasing the data model schema, relationships, and DAX calculations.*

---

## 🚀 Key Performance Indicators (KPIs) & Metrics

The dashboard monitors several critical operational and strategic pillars:

1. **Research & Publication Volume:** Tracking total publications, citations, and journals indexed in global databases (e.g., Scopus, Sinta).
2. **Target vs. Realization:** A dynamic visual comparison evaluating whether specific departments or program studies have met their annual publication quotas.
3. **Financial Efficiency Indicator:** Evaluating the economic impact and allocation of research grants.

### 📐 Featured DAX Formulas

Below is one of the core custom business logic measures developed for this dashboard to calculate the **Rasio Efisiensi Dana** (Fund Efficiency Ratio):

```dax
Rasio Efisiensi Dana = 
DIVIDE(
    [Total Publikasi], 
    SUM('Data Penelitian'[Total Dana Grant]), 
    0
)
