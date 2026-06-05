Nigeria COVID-19 Early Pandemic EDA
Exploratory Data Analysis of Nigeria's First Wave (Feb 27 – Mar 30, 2020)
📌 Project Overview
This project performs an Exploratory Data Analysis (EDA) of Nigeria's earliest recorded COVID-19 cases, using data sourced from the Nigeria Centre for Disease Control (NCDC) via Kaggle.
The dataset captures the first 33 days of Nigeria's pandemic response — from the country's index case on February 27, 2020, through March 30, 2020. This period represents a critical window: the initial detection, spread, and early government response before national lockdown measures were introduced.
This analysis answers five core questions:
How did COVID-19 cases grow nationally in the first 33 days?
Which states bore the highest burden of infections and deaths?
What were the fatality and recovery rates at this early stage?
How did weekly case counts accelerate over time?
How large was the gap between suspected and confirmed cases?
📂 Dataset
Property
Detail
Source
NCDC via Kaggle (Ajibola Lawal)
Period
February 27, 2020 – March 30, 2020
Records
304 rows
States Covered
27 Nigerian states + FCT
Format
.xls / .csv
Columns
Column
Description
Date
Date of record
Location
Nigerian state
Suspected Cases
Suspected (unconfirmed) cases per state per day
Nr. Of New Cases
Newly confirmed cases per state per day
Total Confirmed Cases
Cumulative confirmed cases per state
Deaths
Deaths recorded
Recovered
Recoveries recorded
Long / Lat
Geographic coordinates of each state
Source
NCDC situation report URL (dropped in analysis)
Note: The raw dataset is preserved untouched. All cleaning and transformations are performed entirely in Python code.
🔍 Key Findings
Metric
Value
Total Confirmed Cases
132
Total Deaths
7
Total Recoveries
23
Case Fatality Rate
5.3%
Recovery Rate
17.4%
Worst-Hit State
Lagos (81 cases — 61% of national total)
Peak Single Day
20 new cases (March 30, 2020)
States Affected
27
Narrative Summary
Nigeria recorded its index case on February 27, 2020 in Ogun State — an Italian citizen. For the first two weeks, cases remained concentrated in Lagos and a handful of southern states. By mid-March, the virus had spread to FCT, Kano, Edo, and Rivers. The final week of March saw the sharpest acceleration, with 20 new cases recorded on March 30 alone — signalling the beginning of exponential growth that would lead to a national lockdown in April 2020.
Lagos accounted for 61% of all confirmed cases, reflecting its status as Nigeria's commercial hub and international gateway. The 5.3% case fatality rate during this period was above the global average, likely reflecting limited testing capacity and underreporting rather than true disease severity.
📊 Visualizations
1. National Daily & Cumulative Trend
�
Load image
2. State-Level Case & Death Breakdown
�
Load image
3. Outcome Distribution & Fatality Rate by State
�
Load image
4. Weekly Case Growth
�
Load image
5. Daily Cases Heatmap — Top 10 States
�
Load image
6. Suspected vs Confirmed Cases by State
�
Load image
🛠️ Tools & Libraries
Tool
Purpose
Python 3
Core programming language
pandas
Data loading, cleaning, transformation
matplotlib
Base charting
seaborn
Heatmap and styled visualizations
openpyxl / xlrd
Reading Excel files
🗂️ Project Structure
nigeria-covid19-eda/
│
├── covid19-nigeria-dataset.xls   # Raw dataset (original, unmodified)
├── nigeria_covid19_eda.py        # Full EDA script
├── 01_national_trend.png         # Daily & cumulative trend chart
├── 02_state_analysis.png         # State-level breakdown
├── 03_outcome_rates.png          # Fatality & recovery rates
├── 04_weekly_spread.png          # Weekly case growth
├── 05_heatmap_top10.png          # Top 10 states heatmap
├── 06_suspected_vs_confirmed.png # Suspected vs confirmed comparison
└── README.md                     # Project documentation
▶️ How to Run
1. Clone the repository
git clone https://github.com/akah-ebenezer/nigeria-covid19-eda.git
cd nigeria-covid19-eda
2. Install dependencies
pip install pandas matplotlib seaborn openpyxl
3. Run the EDA script
python nigeria_covid19_eda.py
All 6 charts will be generated and saved in the project folder.
⚠️ Limitations
This dataset covers only the first 33 days of Nigeria's pandemic — it does not represent the full pandemic arc (waves 2 and 3 occurred later in 2020–2021).
Suspected Cases column had 12 missing values, filled with 0 for analysis.
Early testing infrastructure in Nigeria was limited, meaning actual case counts were likely higher than recorded.
The high fatality rate (5.3%) should be interpreted in the context of low testing volume, not necessarily high disease lethality.
👤 Author
Akah Ebenezer Chukwuemeka
Data Analyst | Founder, Mekushandy Tech Academy | Abuja, Nigeria
GitHub: github.com/akah-ebenezer
LinkedIn: linkedin.com/in/akah-ebenezer
📄 License
This project is open source under the MIT License.
Dataset credit: Ajibola Lawal via Kaggle | Original data source: Nigeria Centre for Disease Control (NCDC)
