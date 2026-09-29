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

1. What share of physical and financial targets has actually been accomplished, overall and by province?
2. Which programs/categories are ahead of or behind target?
3. How does accomplishment vary between the four provinces and their districts?
4. Which LGUs are outperforming or lagging their peers?


**Core KPIs:** Target Physical Accomplishment, Actual Physical Accomplishment, % Physical Accomplished; Target Financial Accomplishment, Actual Financial Accomplishment, % Financial Accomplished. Each sliceable by Province, Program, Category, and District.
 
## Process
1. Consolidated per-program records into one workbook, standardizing program and category labels
2. Cleaned the data — left target fields blank (not zero) where a program has no per-LGU target set, so it wouldn't distort the % calculations
3. Loaded into Power BI and built DAX measures for % Physical and % Financial Accomplished (using DIVIDE() to safely handle blanks/zeros)
4. Built 8 report pages — Overview plus one per category/program group — with a shared visual language
5. Added a custom icon-based navigation bar and a glossary page for non-technical viewers
6. QA'd totals against source data and tested cross-filtering across all pages

