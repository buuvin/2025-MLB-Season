# 📘 METADATA – 2025 MLB Season Dataset

This document describes the structure and variables of each dataset included in the **2025 MLB Season Repository**.  
All data was collected using the **MLB Stats API** and cleaned for educational and analytical use.

---

## ⚾ 1. Game-Level Data (`games_2025.csv`)

**Rows:** One per game  

| Variable | Type | Description |
|-----------|------|-------------|
| `gamePk` | int | Unique game identifier. |
| `date` | string | Official date of the game. |
| `venue` | string | Name of the ballpark where the game was played. |
| `home_team`, `away_team` | string | Names of the home and away teams. |
| `home_team_id`, `away_team_id` | int | MLB team identifiers for each team. |
| `home_score`, `away_score` | int | Final score for the home and away teams. |
| `home_hits`, `away_hits` | int | Number of hits for each team. |
| `home_errors`, `away_errors` | int | Number of fielding errors for each team. |
| `weather` | string | Weather condition at game time (e.g., Clear, Cloudy). |
| `temperature` | int | Temperature in Fahrenheit at the start of the game. |
| `attendance` | int | Official attendance at the game. |
| `duration_minutes` | int | Total duration of the game in minutes. |

---

## 🧢 2. Team-Level Data (`teams_2025_combined.csv`)

**Rows:** One per MLB team (30 total)  

| Variable Prefix | Description |
|-----------------|--------------|
| `hit_` | Hitting statistics (offensive performance) |
| `pitch_` | Pitching statistics (defensive performance) |
| `field_` | Fielding statistics (defensive and positional play) |

**Key Variables:**
| Variable | Type | Description |
|-----------|------|-------------|
| `team_id` | int | Unique MLB team identifier. |
| `team_name` | string | Full name of the team. |
| `league` | string | League affiliation (American League or National League). |
| `division` | string | Division within the league. |
| `hit_*` | numeric | Aggregated team batting metrics, including total hits, home runs, RBIs, slugging %, and on-base %. |
| `pitch_*` | numeric | Aggregated team pitching metrics, including ERA, WHIP, strikeouts, walks, and innings pitched. |
| `field_*` | numeric | Aggregated team fielding metrics, including errors, fielding percentage, assists, and double plays. |

**Example Columns:**
- `hit_avg`: Team batting average  
- `hit_homeRuns`: Total home runs hit  
- `pitch_era`: Team earned run average (ERA)  
- `pitch_strikeOuts`: Total strikeouts recorded by pitchers  
- `field_errors`: Total errors committed  
- `field_fielding`: Overall fielding percentage

---

## 🧍‍♂️ 3. Player-Level Data (`players_2025.csv`)

**Rows:** One per MLB player with at least one recorded appearance in the 2025 season  

| Variable Prefix | Description |
|-----------------|--------------|
| `_hit` | Hitting (offensive) statistics |
| `_pitch` | Pitching (defensive) statistics |

**Key Variables:**
| Variable | Type | Description |
|-----------|------|-------------|
| `player_id` | int | Unique MLB player identifier. |
| `player_name` | string | Full name of the player. |
| `team_id` | int | Team identifier the player was active with. |
| `team_name` | string | Full team name. |
| `age_hit`, `age_pitch` | int | Player’s age for hitting or pitching statistics. |
| `gamesPlayed_hit`, `gamesPlayed_pitch` | int | Number of games the player appeared in as a hitter or pitcher. |
| `avg_hit`, `homeRuns_hit`, `rbi_hit`, `obp_hit`, `slg_hit`, `ops_hit` | float | Common batting metrics: batting average, home runs, runs batted in, on-base %, slugging %, and OPS. |
| `era`, `whip`, `strikeOuts_pitch`, `inningsPitched`, `wins`, `losses`, `saves` | float/int | Key pitching metrics: ERA, WHIP, strikeouts, innings pitched, wins, losses, and saves. |
| `strikeoutWalkRatio`, `strikeoutsPer9Inn`, `walksPer9Inn`, `hitsPer9Inn` | float | Derived pitching efficiency metrics. |
| `inheritedRunners`, `inheritedRunnersScored` | int | Relief pitching metrics. |
| `fielding-related columns` | Various | Include interference, passed balls, and sacrifice events. |

---

## 🔗 Relationships Across Datasets

| Relationship | Join Key |
|---------------|-----------|
| **Games ↔ Teams** | `home_team_id` / `away_team_id` ↔ `team_id` |
| **Teams ↔ Players** | `team_id` |
| **Games ↔ Players** | Indirect via `team_id` |

---

## 🧮 Data Overview

| Dataset | Rows | Description |
|----------|------|-------------|
| `games_2024.csv` | ~2,430 | One row per MLB regular-season game |
| `teams_2024_combined.csv` | 30 | One row per MLB team |
| `players_2024.csv` | ~800–850 | One row per MLB player with recorded stats |

---

## 📅 Season Details

- **Season Covered:** 2025 MLB Regular Season  
- **Scope:** Major League Baseball (`sportId=1`) only  
- **Game Type:** Regular season games (`game_type=R`)  
- **Player Pool:** All MLB players with recorded stats (`playerPool=ALL`)

---

## ⚙️ Data Source
All data originates from the [MLB Stats API](https://statsapi.mlb.com/).  
Collection and preprocessing scripts written in **Python** using:
- `requests`
- `pandas`
- `tqdm`

---

## ⚖️ License & Use
This dataset is for educational and research use only.  
Data © Major League Baseball Advanced Media (MLBAM).

---

## 👤 Author
**Bhuvan Balagar**  
📧 Contact: [your.email@example.com]  
💼 Project: *2025 MLB Analytics Datathon*
