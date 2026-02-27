# EDE-N — Project Instructions

## Project
Data analysis capstone following the Google Data Analytics framework (Ask → Prepare → Process → Analyze).

**Business task:** Design marketing strategies to convert casual riders into annual members (Cyclistic bike-share).

## Language
- Code comments and commit messages: English
- Documentation / README: Spanish (bilingual is fine)

## Tech Stack
- R with tidyverse, lubridate
- Data: divvy-tripdata CSVs (June 2022 – June 2023, ~6.5M rows, 13 columns)
- Output: hosted dashboard (TBD)

## Project Structure (planned)
```
data/       # raw CSV files (not committed)
scripts/    # R scripts
output/     # cleaned data, plots, exports
```

## Key Analysis Questions
1. Which sectors/provinces have highest maintenance program incidence?
2. Infrastructure development in high-incidence areas?
3. Areas with lowest incidence?
4. Seasonal patterns in maintenance?
5. Day of week / time of day with highest scheduled maintenance?
6. Areas with highest accumulated maintenance time?
7. Correlation with commercial activity, average power per zone, fuel consumption, schools, malls, hospitals?
8. Punctuality of scheduled maintenance.

## Data Notes
- Source: [divvy-tripdata](https://divvy-tripdata.s3.amazonaws.com/index.html) — Motivate International Inc.
- No PII in dataset
- Negative trip durations = maintenance rides → filter out into `clean_yearlytrips`
- Recoding: `member` → `Subscriber`, `classic_bike` → `Classic Bike`, etc.
