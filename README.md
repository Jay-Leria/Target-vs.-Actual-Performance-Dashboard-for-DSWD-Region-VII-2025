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
1. Consolidated per-program records into one workbook, standardizing program and category labels.
2. Cleaned the data. Left target fields blank (not zero) where a program has no per-LGU target set, so it wouldn't distort the % calculations.
3. Loaded into Power BI and built DAX measures for % Physical and % Financial Accomplished (using DIVIDE() to safely handle blanks/zeros).
4. Built 8 report pages, Overview plus one per category/program group, with a shared visual language.
5. Added a custom icon-based navigation bar and a glossary page for non-technical viewers.
6. QA'd totals against source data and tested cross-filtering across all pages.

## Dashboard Overview
A persistent icon sidebar lets users jump directly between Overview, Protective, Protective Centers, Promotive, Innovation, AKAP, and AICS pages. Each page carries slicers (province, district) that filter every visual on that page at once. Clustered column charts show Target vs. Actual side by side by province or program; donut charts on category pages break down Actual (and Target, where available) by province for each individual program. KPI cards up top summarize totals, and clicking any bar or donut segment cross-filters the rest of the page. A dedicated glossary page defines each program acronym for viewers unfamiliar with DSWD program names.
![Dashboard Overview](./Overview%20Screenshot.png)

### Project Insight

Overall, the data shows **75.5% physical** and **69.4% financial** accomplishment (**854,055 → 644,440** target-to-actual physical; **₱6.24B → ₱4.33B** target-to-actual financial). Breaking that down by province reveals a much bigger story than the overall number suggests:

| Province | Physical % | Financial % |
|----------|-----------:|------------:|
| Bohol | 52.6% | 35.1% |
| Cebu | 77.1% | 77.0% |
| Negros Oriental | 102.7% | 93.2% |
| Siquijor | 68.7% | 94.9% |

Bohol lags well behind the other three provinces on both measures. Negros Oriental exceeded its physical target (102.7%), while Siquijor's financial accomplishment (94.9%) is far ahead of its physical progress (68.7%), suggesting funds have been disbursed faster than the associated physical activities were completed there.

## Final Conclusion
This dashboard turns a fragmented, program-by-program reporting process into one consolidated, filterable tool that surfaces actionable gaps, like Bohol's underperformance, that would be easy to miss in raw spreadsheets. Beyond the reporting value, the project demonstrates the full BI workflow end to end: data cleaning and standardization, relational data modeling, DAX measure design, and dashboard/UX design built for non-technical stakeholders.
