# 💡 Business Insight Questions for the 2025 MLB Season Dataset
---

## ⚾ 1. Game-Level Dataset (`games_2024.csv`)

These questions focus on game performance, attendance, and environmental impact.

1. **Home Advantage:**  
   - Do home teams win significantly more games than away teams?  
   - Which teams have the strongest home-field advantage based on win rate?

2. **Scoring Patterns:**  
   - What is the average total score per game, and how does it vary by month or weather condition?  
   - Are higher-scoring games more common in certain ballparks?

3. **Game Duration Analysis:**  
   - What factors (total runs, number of hits, or innings played) correlate most strongly with game length?  
   - Are games involving specific teams consistently longer or shorter than average?

4. **Attendance Insights:**  
   - Which teams attract the highest attendance, and how does attendance correlate with performance or opponent strength?  
   - Does attendance decrease during extreme weather or weekday games?

5. **Performance Under Pressure:**  
   - Are there trends in performance (runs, errors, hits) between closely contested games (decided by ≤2 runs) versus blowouts (≥5 runs)?

---

## 🧢 2. Team-Level Dataset (`teams_2024_combined.csv`)

These questions highlight relationships between offensive, defensive, and overall team success.

1. **Offense vs. Success:**  
   - How strongly do hitting metrics (`hit_avg`, `hit_homeRuns`, `hit_ops`) correlate with total wins or runs scored?  
   - Which offensive statistic best predicts a team’s winning percentage?

2. **Pitching Efficiency:**  
   - Do teams with lower `pitch_era` or `pitch_whip` consistently finish higher in their divisions?  
   - Is strikeout-to-walk ratio (`pitch_strikeoutWalkRatio`) a better indicator of team success than ERA?

3. **Fielding Impact:**  
   - Does fielding performance (`field_errors`, `field_fielding`) significantly influence overall team wins?  
   - Which teams minimize errors yet still allow high runs — and what might that suggest?

4. **Balanced Teams:**  
   - Which teams show the most balance between hitting and pitching performance (e.g., top quartile in both OPS and ERA)?  
   - Are elite offensive teams also strong defensively, or do teams tend to specialize?

5. **Run Production vs. Run Prevention:**  
   - Compare teams’ `hit_runs` (runs scored) and `pitch_runs` (runs allowed).  
   - Which teams are most efficient at turning offensive production into wins?

6. **Resource Allocation Insight (Business Angle):**  
   - If you were an MLB general manager, which areas (hitting, pitching, fielding) would you prioritize investment in based on these metrics?

---

## 🧍‍♂️ 3. Player-Level Dataset (`players_2024.csv`)

These questions encourage deeper exploration of individual performance and player value.

1. **Player Efficiency:**  
   - Which hitters produce the most RBIs per hit or per at-bat?  
   - Among pitchers, who has the best ratio of strikeouts to walks?

2. **Consistency vs. Power:**  
   - Is batting average (`avg_hit`) or slugging percentage (`slg_hit`) a stronger indicator of a player’s contribution to team wins?  
   - Are high home run hitters also consistent contact hitters?

3. **Pitcher Workload & Performance:**  
   - Do pitchers with more innings pitched (`inningsPitched`) maintain their effectiveness (ERA, WHIP) better or worse than those with fewer innings?  
   - How does performance change between starters and relievers (based on `gamesStarted`)?

4. **Stealing & Aggression:**  
   - Which players or teams demonstrate the highest base-stealing success rates (`stolenBasePercentage_hit`)?  
   - Does base-stealing success correlate with team-level run production?

5. **Value Comparison:**  
   - Identify the most well-rounded players by combining multiple metrics (e.g., OPS + defensive stats).  
   - Which players provide high impact relative to playing time (per game or per plate appearance)?

6. **Performance Trends (Predictive Thinking):**  
   - Using player-level data, can you predict which players are likely to improve or regress next season based on their current performance balance?

---

## 🧩 Cross-Dataset Analytical Questions

Encourage combining datasets to find deeper, relational insights.

1. **Game Outcomes & Team Stats:**  
   - How do team-level stats (OPS, ERA) relate to game-level outcomes (wins, run differentials)?  
   - Can team pitching and hitting performance explain their total wins across the season?

2. **Player-to-Team Impact:**  
   - Are teams with higher aggregate OPS or lower team ERA simply a reflection of having multiple high-performing players?  
   - How much variance in team performance is explained by the top 3 players on each roster?

3. **Fan Engagement vs. Performance:**  
   - Does fan attendance (from game-level data) track more closely with offensive excitement (runs, home runs) or team success (wins)?  

4. **Environmental Influence:**  
   - Do certain stadiums or weather conditions consistently produce more home runs or longer games?  
   - Can you model expected runs per game based on temperature, venue, and team offensive stats?

---

## 🎓 Suggested Analysis Deliverables
To help structure student projects, consider asking for:
- **Descriptive Analysis:** Key patterns or relationships in one dataset.  
- **Correlational Study:** Relationship between two performance variables.  
- **Predictive Modeling:** Using player or team stats to predict wins or ERA.  
- **Visualization Project:** Trend dashboards (runs vs. wins, OPS vs. attendance).  

---

## 💬 Tip for Students
> Aim to connect **performance metrics** to **business outcomes** (fan attendance, win rates, player valuation).  
> Think like an analyst on a team’s front office: how could this data inform future roster or strategy decisions?
