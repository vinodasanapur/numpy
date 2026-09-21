```markdown
# IPL Matches Data Analysis (2008 – 2024)[cite: 2]

An exploratory data analysis (EDA) pipeline for processing and analyzing historical Indian Premier League (IPL) match records from 2008 through 2024[cite: 2].

## 📌 Dataset Overview

* **Source File:** `matches.csv`[cite: 2]
* **Total Records:** 1,095 matches[cite: 2]
* **Features:** 20 columns detailing match outcomes, teams, venues, toss decisions, and officials[cite: 2]

### Schema Specification

| # | Column Name | Non-Null Count | Data Type | Description |
|---|---|---|---|---|
| 0 | `id` | 1,095 | int64 | Unique match identifier[cite: 2] |
| 1 | `season` | 1,095 | object | IPL season/year[cite: 2] |
| 2 | `city` | 1,044 | object | City where the match took place[cite: 2] |
| 3 | `date` | 1,095 | object | Match date (`YYYY-MM-DD`)[cite: 2] |
| 4 | `match_type` | 1,095 | object | Stage of tournament (e.g., League, Qualifier, Final)[cite: 2] |
| 5 | `player_of_match` | 1,090 | object | Awarded Player of the Match[cite: 2] |
| 6 | `venue` | 1,095 | object | Stadium name[cite: 2] |
| 7 | `team1` | 1,095 | object | First competing team[cite: 2] |
| 8 | `team2` | 1,095 | object | Second competing team[cite: 2] |
| 9 | `toss_winner` | 1,095 | object | Team that won the toss[cite: 2] |
| 10 | `toss_decision` | 1,095 | object | Decision after toss (`bat` or `field`)[cite: 2] |
| 11 | `winner` | 1,090 | object | Winning team[cite: 2] |
| 12 | `result` | 1,095 | object | Result type (`runs`, `wickets`, `no result`)[cite: 2] |
| 13 | `result_margin` | 1,076 | float64 | Margin of victory (runs or wickets)[cite: 2] |
| 14 | `target_runs` | 1,092 | float64 | Target score for the chasing team[cite: 2] |
| 15 | `target_overs` | 1,092 | float64 | Total overs allocated for the target[cite: 2] |
| 16 | `super_over` | 1,095 | object | Indicates if a Super Over was played (`Y`/`N`)[cite: 2] |
| 17 | `method` | 21 | object | Special match evaluation method (e.g., `D/L`)[cite: 2] |
| 18 | `umpire1` | 1,095 | object | Primary on-field umpire[cite: 2] |
| 19 | `umpire2` | 1,095 | object | Secondary on-field umpire[cite: 2] |

---

## 🛠 Project Setup & Dependencies

```bash
pip install pandas

```

---

## 🚀 Quickstart & Pipeline Usage

```python
import pandas as pd

# Load dataset
df = pd.read_csv("matches.csv")

# Verify data shape
print(f"Dataset Dimensions: {df.shape}")  # (1095, 20)

# Inspect head and tail
print(df.head())
print(df.tail())

# Schema summary
df.info()

```

---

## 📊 Summary Statistics & Data Health

* **Missing Values Overview:**
* `method`: ~98% missing values (only populated during Duckworth-Lewis scenarios).


* `city`: 51 missing entries.


* `result_margin`: 19 missing entries (corresponds to no-result or abandoned matches).


* `player_of_match` & `winner`: 5 missing entries each.




* **Memory Usage:** ~171.2 KB.



```

```
