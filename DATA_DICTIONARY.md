# 📖 Gaming Addiction Dataset: Data Dictionary

## Overview
* **Total Instances (Rows):** 250
* **Total Features (Columns):** 47
* **Primary Key:** `user_id`
* **Target Variable:** `addiction_binary`

---

## 1. Identifier & Demographics

| Column Name | Data Type | Null Count | Allowed Values / Summary | Description |
| :--- | :--- | :--- | :--- | :--- |
| `user_id` | Categorical (`object`) | 0 | `USR000001` to `USR000250` | Unique alphanumeric identifier for each gamer/participant. |
| `age` | Integer (`int64`) | 0 | Min: 13, Max: 40 (Mean: ~22.2) | Age of the individual in years. |
| `gender` | Categorical (`object`) | 0 | Male, Female, Non-binary, Prefer not to say | Self-reported gender identity. |
| `country` | Categorical (`object`) | 0 | 15 unique countries (Top: USA, India, Brazil, South Korea) | Country of residence. |
| `occupation` | Categorical (`object`) | 0 | Employed, Student, Unemployed, Freelancer, Other | Primary daily occupation/status. |
| `income_level` | Categorical (`object`) | 0 | Lower, Lower-Middle, Middle, Upper-Middle, Upper | Household or personal income classification. |
| `relationship_status` | Categorical (`object`) | 0 | Single, In a relationship, Married, Divorced, Prefer not to say | Current marital/relationship status. |

---

## 2. Gaming Profile & Platform Logistics

| Column Name | Data Type | Null Count | Allowed Values / Summary | Description |
| :--- | :--- | :--- | :--- | :--- |
| `years_gaming` | Integer (`int64`) | 0 | Min: 1, Max: 25 | Total years the individual has been playing video games. |
| `preferred_genre` | Categorical (`object`) | 0 | RPG, MMORPG, Strategy, Sandbox, FPS, MOBA, etc. | Most played or preferred game genre. |
| `platform` | Categorical (`object`) | 0 | PC, Mobile, Console, PC+Mobile, Cross-Platform | Primary gaming platform used. |
| `device_type` | Categorical (`object`) | 0 | Laptop, High-end PC, Mobile, Console, Mixed, etc. | Specific hardware tier or primary gaming device used. |
| `rank_tier` | Categorical (`object`) | 0 | Bronze, Silver, Gold, Platinum, Diamond, Master, etc. | In-game competitive rank or skill tier placement. |
| `subscription_status` | Categorical (`object`) | **82 (32.8%)** | Free, Premium, Ultimate, *NaN* | Tier of active paid gaming subscriptions (contains missing values). |
| `internet_speed_mbps` | Continuous (`float64`) | 0 | Min: 5.0, Max: 255.5 Mbps | Home internet connection speed measured in Megabits per second. |

---

## 3. Gameplay Behaviors & Patterns

| Column Name | Data Type | Null Count | Allowed Values / Summary | Description |
| :--- | :--- | :--- | :--- | :--- |
| `daily_playtime_hours` | Continuous (`float64`) | 0 | Min: 0.5, Max: 11.9 | Average daily time spent playing games (in hours). |
| `weekly_play_sessions` | Integer (`int64`) | 0 | Min: 1, Max: 15 | Number of individual gaming sessions logged per week. |
| `late_night_sessions_hours` | Continuous (`float64`) | 0 | Min: 0.0, Max: 5.2 | Time spent gaming during late-night hours (e.g., 12 AM – 6 AM). |
| `weekend_playtime_hours` | Continuous (`float64`) | 0 | Min: 0.5, Max: 20.0 | Average gaming duration on weekend days (in hours). |
| `consecutive_hours_max` | Continuous (`float64`) | 0 | Min: 1.0, Max: 20.6 | Maximum continuous duration spent in a single gaming session. |
| `screen_time_total_hours` | Continuous (`float64`) | 0 | Min: 1.2, Max: 15.1 | Total daily screen time including non-gaming screen usage. |
| `multiplayer_ratio` | Continuous (`float64`) | 0 | Min: 0.0, Max: 1.0 | Proportion of total play time spent in multiplayer vs. single-player modes. |
| `toxic_chat_reports` | Integer (`int64`) | 0 | Min: 0, Max: 32 | Total times the user was reported for toxic behavior/chat. |
| `rage_quit_frequency` | Integer (`int64`) | 0 | Min: 0, Max: 10 | Estimated count or rate of rage-quitting matches mid-game per period. |

---

## 4. Financial & Monetization Variables

| Column Name | Data Type | Null Count | Allowed Values / Summary | Description |
| :--- | :--- | :--- | :--- | :--- |
| `in_game_purchases` | Integer (`int64`) | 0 | Min: 0, Max: 21 | Total count of microtransactions/in-game purchases made. |
| `monthly_spending_usd` | Continuous (`float64`) | 0 | Min: $0.00, Max: $182.60 | Average monthly expenditure on games/microtransactions (in USD). |
| `lootbox_openings` | Integer (`int64`) | 0 | Min: 0, Max: 41 | Count of randomized lootboxes or gacha items opened. |

---

## 5. Psychological & Mental Health Metrics

| Column Name | Data Type | Null Count | Allowed Values / Summary | Description |
| :--- | :--- | :--- | :--- | :--- |
| `stress_score` | Continuous (`float64`) | 0 | Min: 1.0, Max: 10.0 | Standardized score measuring reported stress levels. |
| `loneliness_score` | Continuous (`float64`) | 0 | Min: 1.0, Max: 10.0 | Self-reported measure of social isolation/loneliness. |
| `dopamine_dependency_index` | Continuous (`float64`) | 0 | Min: 1.0, Max: 8.6 | Index measuring psychological reliance on instant gratification/gaming rewards. |
| `self_control_score` | Continuous (`float64`) | 0 | Min: 1.0, Max: 10.0 | Standardized assessment of personal discipline and impulse control. |
| `impulsiveness_score` | Continuous (`float64`) | 0 | Min: 1.0, Max: 10.0 | Measure of inclination toward impulsive behaviors. |
| `anxiety_level` | Continuous (`float64`) | 0 | Min: 1.0, Max: 10.0 | Standardized score reflecting general or situational anxiety levels. |
| `depression_indicator` | Continuous (`float64`) | **11 (4.4%)** | Min: 1.0, Max: 8.6 | Clinical or self-assessed indicator of depressive symptoms. |
| `emotional_stability` | Continuous (`float64`) | 0 | Min: 2.3, Max: 10.0 | Psychological score evaluating emotional regulation and resilience. |

---

## 6. Physical Well-being & Lifestyle Factors

| Column Name | Data Type | Null Count | Allowed Values / Summary | Description |
| :--- | :--- | :--- | :--- | :--- |
| `sleep_hours` | Continuous (`float64`) | 0 | Min: 3.4, Max: 9.5 | Average nightly sleep duration (in hours). |
| `exercise_frequency_per_week` | Integer (`int64`) | 0 | Min: 0, Max: 5 | Number of physical workout/exercise sessions completed per week. |
| `caffeine_intake_cups_day` | Integer (`int64`) | 0 | Min: 0, Max: 7 | Daily consumption of caffeinated drinks (measured in cups). |
| `social_interaction_hours` | Continuous (`float64`) | 0 | Min: 0.0, Max: 6.6 | Hours per day spent engaging in real-life/in-person social activities. |

---

## 7. Academic, Work & Productivity Impact

| Column Name | Data Type | Null Count | Allowed Values / Summary | Description |
| :--- | :--- | :--- | :--- | :--- |
| `gpa_or_performance_score` | Continuous (`float64`) | **10 (4.0%)** | Min: 2.17, Max: 4.00 | Academic Grade Point Average (GPA) or workplace performance rating score. |
| `missed_deadlines` | Integer (`int64`) | 0 | Min: 0, Max: 8 | Number of missed work or academic project deadlines. |
| `productivity_drop_percent` | Continuous (`float64`) | 0 | Min: 0.0%, Max: 44.2% | Estimated percentage reduction in personal productivity attributed to gaming. |
| `absenteeism_days` | Integer (`int64`) | 0 | Min: 0, Max: 14 | Days missed from work or school per evaluation period. |

---

## 8. Modeled & Target Indicators

| Column Name | Data Type | Null Count | Allowed Values / Summary | Description |
| :--- | :--- | :--- | :--- | :--- |
| `behavioral_cluster` | Categorical (`object`) | 0 | Casual Enjoyer, Competitive Grinder, Streamer/Creator, Toxic Competitor, etc. | Machine-learned cluster segment describing gamer profile/type. |
| `addiction_binary` *(Target)* | Binary Integer (`int64`) | 0 | `0` = No, `1` = Yes (~16.8% prevalence) | **Target Variable:** Binary flag indicating presence of gaming addiction disorder. |
| `burnout_probability` | Continuous (`float64`) | 0 | Min: 0.32, Max: 1.00 | Estimated risk/probability score for emotional and mental burnout. |
| `mental_health_risk_score` | Continuous (`float64`) | 0 | Min: 0.12, Max: 0.92 | Composite calculated risk score combining anxiety, stress, and depression metrics. |
| `churn_probability` | Continuous (`float64`) | 0 | Min: 0.15, Max: 1.00 | Predicted likelihood of quitting the game/platform. |
