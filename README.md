# Target-vs.-Actual-Performance-Dashboard-for-DSWD-Region-VII-2025
Built a multi-page Power BI dashboard tracking physical/financial accomplishment across 15+ DSWD Region VII programs (4Ps, AICS, AKAP, KALAHI, DRMD, Protective Centers). Shows Target vs. Actual by province and district, with glossary and simple navigation. Used by LGU officials for congressional briefers, replacing manual reports

## Project Objective
To consolidate program accomplishment data for 129 cities/municipalities across four provinces into a single interactive Power BI dashboard, replacing scattered per-program spreadsheets with one live view of Target vs. Actual performance, physical and financial, by province, district, program, and category.

## Dataset Used

The dashboard is built from [`Neda RSC Data.xlsx`](Neda%20RSC%20Data.xlsx), which contains **2,112 records** covering **129 LGUs × 16 programs** across the provinces of **Bohol, Cebu, Negros Oriental, and Siquijor**.

### Fields

The dataset contains the following fields:

* **10-digit PSGC Code**
* **Province**
* **City/Municipality**
* **Correspondence Code**
* **Geographic Level**
* **City Class**
* **Income Classification**
* **District**
* **Program**
* **Category**
* **Target Physical Accomplishment**
* **Target Financial Accomplishment**
* **Actual Physical Accomplishment**
* **Actual Financial Accomplishment**

### Geographic Coverage

The dataset covers:

* **Bohol**
* **Cebu**
* **Negros Oriental**
* **Siquijor**

It includes LGUs across the **1st–7th Districts**, as well as **Lone Districts**.

### Program Categories

The **16 programs** are grouped into four categories:

| Category               | Programs                                              |
| ---------------------- | ----------------------------------------------------- |
| **Promotive**          | 4Ps, SLP, KALAHI                                      |
| **Protective**         | AICS, AKAP, RRTP, Social Pension, SFP, TBTP, PAG-ABOT |
| **Protective Centers** | RRCY, RSCC, HAVEN, HFG, AVRC II                       |
| **Innovation**         | Food Stamp Program                                    |

## Questions (KPI)

* What share of physical and financial targets has actually been accomplished, overall and by province?
* Which programs/categories are ahead of or behind target?
* How does accomplishment vary between the four provinces and their districts?
* Which LGUs are outperforming or lagging their peers?


**Core KPIs:** Target Physical Accomplishment, Actual Physical Accomplishment, % Physical Accomplished; Target Financial Accomplishment, Actual Financial Accomplishment, % Financial Accomplished. Each sliceable by Province, Program, Category, and District.
