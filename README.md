# University ERP Analytics Dashboard (Power BI)

An end-to-end Power BI project built on a 17-table university ERP dataset (about 286K records): data cleaning in Power Query, a star/snowflake data model, 30+ DAX measures and a 5-page interactive dashboard.

> The dataset is a sample (synthetic) dataset, so many distributions are evenly spread. The project demonstrates the workflow and technical skills, not real-world findings.

## Tools
Power BI Desktop, Power Query (M), DAX, Mermaid (ER diagram)

## What I did
1. **Data cleaning (Power Query):** capped overpaid fee records and recalculated fee status, handled missing placement data, removed future-dated attendance, flagged inconsistent alumni graduation years, kept the latest hostel allocation per student, and created derived columns (balance due, CTC in LPA, grade, pass/fail, age group, CTC band).
2. **Data model:** Students as the central table, linked to 13 fact tables through Student_ID and to Departments, Faculty and Subjects through Department_ID; a DAX date table linked to Attendance. All relationships are many-to-one with single-direction filtering.
3. **DAX:** 30+ measures covering attendance %, pass %, fee collection %, outstanding fees, placement %, average CTC, scholarship coverage, hostel, library, internship, club and event KPIs.
4. **Dashboard:** five pages with synced slicers, KPI cards and page navigation.

## Dashboard pages
| Page | Focus |
|---|---|
| Overview | KPIs, placement by department, attendance trend, fee status, students by year and city |
| Academics | Attendance, exam results, grade distribution, course status |
| Finance | Fees billed, collected and outstanding, collection by department, scholarships |
| Placements | Placement status, CTC distribution, companies, internships, alumni |
| Campus Life | Hostel, transport, library, clubs, events |

![Overview](screenshots/01_Overview.png)
![Academics](screenshots/02_Academics.png)
![Finance](screenshots/03_Finance.png)
![Placements](screenshots/04_Placements.png)
![Campus Life](screenshots/05_Campus_Life.png)

## Data model
![ER diagram](docs/ERP_ER_Diagram.png)

## Files
- `dashboard/` Power BI report (.pbix, open with Power BI Desktop)
- `data/` source Excel dataset
- `docs/` ER diagram image and Mermaid source

## Author
Santhiya | Data analytics
