
# 🦠 COVID-19 Dashboard Project

**Tools:** SQL, Tableau  
**Author:** Danny Landa  

This project analyzes COVID-19 data to uncover trends in infection rates, death rates, and population impact using SQL and Tableau.

---

## 📊 Tableau Dashboard
![COVID Dashboard Preview](Dashboard%201.png)

🔗 **Interactive Dashboard:** [View on Tableau Public](https://public.tableau.com/app/profile/danny.landa/viz/CovidDashboardproject_17608777724010/Dashboard1)

---

## 🧠 SQL Query Example
```sql
SELECT 
    location, 
    date, 
    total_cases, 
    total_deaths,
    (total_deaths / NULLIF(total_cases, 0)) * 100 AS death_percentage
FROM portfolio.`covid_deaths`
WHERE continent IS NOT NULL
ORDER BY location, date;
