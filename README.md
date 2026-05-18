# US-Employee-Benefits-Dashboard

# Healthcare Coverage Divide: Who Has Benefits in America and Who Doesn't

An interactive Tableau dashboard exploring 15 years of U.S. employee benefits data from the Bureau of Labor Statistics National Compensation Survey (2010–2025).

> *From healthcare to retirement, most U.S. workers have some benefits. But few have all of them and many have none.*

---

## Live Dashboard
<img width="1170" height="752" alt="image" src="https://github.com/user-attachments/assets/ddfed00b-01a1-4639-ad51-922f2f8e2924" />
https://public.tableau.com/views/TheHealthcareCoverageDivideWhoHasBenefitsinAmericaandWhoDoesnt/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

## What This Project Is About

At Willis Towers Watson, I work as part of the Financial, Actuarial and Analytics team and we spend a lot of time benchmarking clients against industry incumbents. While we work on our own proprietary survey data, I wanted to explore the public side of that same question: what does benefits access actually look like across America? So I chose to work with National Compensation Survey by the U.S. Bureau of Labor Statistics as it provides a comprehensive snapshot of employee benefits access across the country by industry, wage tier, and ownership type over the span of 50 years. 

---

## Key Findings
1. Medical care is the most common benefit but still misses 20% of workers.

2. Retirement is shifting risk to employees (401K over pensions).

3. Modern workplace flexibility benefits (remote work, flexible schedules) are formally offered at shockingly low rates (7-12%).

4. Childcare remains a massive blind spot at just 18%, despite being one of the biggest barriers to workforce participation.

5. The 13% with zero benefits represent a vulnerable population likely concentrated in part-time, gig, or low-wage work.

---

## Data Source

**Bureau of Labor Statistics - Employee Benefits in the United States**
National Compensation Survey (NCS)
Release: September 25, 2025
Coverage: 2010–2025

- Full publication: https://www.bls.gov/ebs/publications/employee-benefits-in-the-united-states-march-2025.htm

---

## Data Preparation

The raw BLS dataset (76.4 MB, 768,207 rows) was reduced to 14,285 rows for Tableau performance. The following were removed:

**Rows removed:**
- All Datatypes except `Access rate` — the only metric used across all charts
- All Occupations except `All occupations`
- All Characteristic categories except `All workers` and `Average wage category`
- Provisions not used in any dashboard chart (1,087 total → 25 retained)
- Industries outside the 11 selected for analysis

**Columns removed:**
- 14 BLS internal reference columns (survey codes, series IDs, standard errors, footnote flags)

**Columns retained:**
`Year` · `Ownership` · `Industry` · `Characteristic` · `Estimate category` · `Provision` · `Estimate`

---

## Data Notes
- Data filtered to Civilian Workers, All Industries, 2025
- Metrics represent access to benefits, not enrollment
- Some totals may not sum to 100% due to rounding

---

## Tools Used

- **Tableau Public** — Visualisation
- **Microsoft Excel** — Data preparation
