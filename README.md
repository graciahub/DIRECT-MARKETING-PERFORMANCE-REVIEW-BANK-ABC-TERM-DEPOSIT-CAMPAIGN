# FINAL PROJECT DELTA TEAM - DIRECT MARKETING PERFORMANCE REVIEW — BANK ABC TERM DEPOSIT CAMPAIGN

This project analyzes the performance of a term-deposit **direct marketing campaign** for a fictional bank (“Bank ABC”) using the well-known **Bank Marketing (Portugal)** dataset.  
The focus is on understanding which customer segments respond best, how campaign execution (timing, channel, duration, number of calls) affects results, and what **actionable strategies** can improve conversion.

---

Authors :
1. Risman Ariska Sultani
2. Andhika Raka
3. Deo Gracia M P

Also big appreciation to our mentor, @Andisetiaonto, for the valuable feedback, guidance, and insights throughout this project.

Language : Bahasa Indonesia

---

## 1. Overview

Bank ABC runs outbound campaigns to offer **time deposits** to existing customers.  
Despite large contact volumes, the overall **conversion rate is only ~11.3%**, meaning ~9 out of 10 calls do not result in a subscription.

This project performs an end-to-end **Exploratory Data Analysis (EDA)** and **segmentation study** to:

- Evaluate the current performance of direct marketing.
- Identify **conversion patterns across key customer segments** (e.g. age, job, education).
- Assess execution levers such as **month, day_of_week, contact channel, call duration, and number of calls (campaign)**.
- Translate findings into **concrete business recommendations**.

---

## 2. Objectives

1. **Profile respondents vs non-respondents** using demographics and financial attributes (age, job, education, housing/loan status, etc.).
2. **Quantify conversion patterns** across:
   - Age group, job, and education.
   - Contact month & day of week.
   - Communication channel (cellular vs telephone).
   - Call duration and number of contacts per customer.
3. **Detect inefficiencies** in targeting and campaign execution  
   (e.g., high-volume segments with poor conversion, over-contacted leads).
4. **Provide actionable recommendations** to:
   - Re-prioritize target segments.
   - Optimize communication strategy for under-performing segments.
   - Rebalance agent resources and calling strategy.

---

## 3. Methodology

1. **Data Cleaning & Preparation**
   - Standardized categorical values (e.g. grouping basic.4y/6y/9y → `middle.school` in `education`).
   - Handled missing / unknown categories by using the label `unknown` and checking its relationship to the target.
   - Validated numeric fields and ensured consistent data types.
   - Exported a cleaned dataset `bank_marketing_cleaned.csv` for reproducibility.

2. **Exploratory Data Analysis (EDA)**
   - Univariate & bivariate distributions for all key variables.
   - Conversion tables and visualizations by:
     - `age_group`, `job`, `education`, `marital`, `housing`, `loan`.
     - `month`, `day_of_week`, `contact` channel.
     - `duration` (seconds) and `campaign` (number of contacts).
   - Used **conversion rate**, **share of total leads**, and **share of total “yes”** as core metrics.

3. **Segmentation & Business Profiling**
   - Built semantic **age group buckets** (18–28, 29–40, 41–52, 53–64, 65+).
   - Ranked **occupations** and **education levels** by response performance.
   - Identified **under-performing but high-volume** segments vs **small but highly responsive** niches.

4. **Business Insights & Recommendations**
   - Summarized key patterns.
   - Designed recommendation framework:
     1. Prioritize vs deprioritize market segments.
     2. Optimize communication for under-performing segments.
     3. Evaluate direct marketing team resources & capabilities.
     4. Refine contact strategy (campaign frequency).
     5. Improve call quality (duration) and timing (month/day).

---

## 4. Key Findings (Short Summary)

- **Overall Conversion**
  - Only **11.3%** of contacted customers subscribe to term deposits; **88.7%** say “no”.

- **Age Segmentation (U-shaped pattern)**
  - **18–28 (Early Working Age):** 17.5% conversion from 4.2K customers.
  - **29–40 (Prime Working Age):** 10.1% conversion from 19.6K customers (largest but below average).
  - **41–52 (Late Working Age):** lowest conversion at 8.4% from 11.8K customers.
  - **53–64 (Pre-Retirement):** 12.4% conversion from 5.0K customers.
  - **65+ (Retirement):** highest conversion at ~47% from a small base (663 customers).  
  → **U-shaped relationship**: younger and older groups are more responsive than mid-age segments.

- **Occupation (Job)**
  - Top performers:  
    - `student` (~31%), `retired` (~25%), `unemployed` (~14%).
  - Low performers (but large volume):  
    - `blue-collar` (~6.9%), `services` (~8.1%), `housemaid` (~10%).  
  → Some big segments absorb a lot of call time but convert poorly.

- **Education**
  - `university.degree` & `professional.course` show better conversion than `middle.school`.
  - >50% of leads come from **middle/high school**, but with **sub-par conversion**, driving inefficiency.

- **Timing & Channel**
  - **Month:** Negative relationship between monthly volume and conversion; heavy months (e.g., May) show **low conversion**, lighter months (e.g., Mar, Dec) show **high conversion (≈45–50%)**.
  - **Day of Week:** Best results on **Tue–Thu**, weakest on **Mon**.
  - **Channel:** `cellular` (~14.7%) is ~2.8× more effective than `telephone` (~5.3%).

- **Campaign Frequency (Number of Contacts)**
  - Most conversions happen in the **first 1–3 calls**.
  - Beyond that, each additional contact yields **diminishing returns**; ≥8 contacts adds almost no incremental conversion.

- **Call Duration**
  - Calls **≤100s**: very frequent (~10K) but almost no sales (0.8% conversion).
  - **101–300s**: conversion ~7.2%.
  - **301–600s**: conversion jumps to ~18.6%.
  - **>600s**: highest conversion at **~48.6%** (half of long calls close).  
  → Very short calls are usually failed attempts; longer, consultative conversations are far more productive.

---

## 5. Business Recommendations (High-Level)

1. **Prioritize / Deprioritize Segments**
   - Prioritize: `student`, `retired`, `unemployed`, `admin.`, `management`, `technician`, higher education (`university.degree`, `professional.course`), and age **18–28** & **53+**.
   - Deprioritize or apply stricter filters: `blue-collar`, `services`, and **middle/high-school** education segments with low conversion but high call volume.

2. **Optimize Messaging for Under-Performing Segments**
   - Simplify product narrative, focus on **safety, predictability, and small starting amounts**.
   - Tailor scripts to job/education/age context instead of using a one-size-fits-all pitch.

3. **Rebalance Direct Marketing Resources**
   - Align agent capacity with realistic conversion expectations.
   - Use high-performing agents as benchmarks and trainers for others.

4. **Refine Contact Strategy (Campaign)**
   - **Cap number of calls per lead** (e.g., 3–4 attempts) to avoid waste and customer fatigue.
   - After the cap, move leads to **low-touch channels** (SMS, email, push).

5. **Improve Call Quality (Duration & Timing)**
   - Encourage **consultative calls** (≥300 seconds) for warm leads instead of many short calls.
   - Concentrate call windows on **Tue–Thu** and avoid overloading certain months.

---
