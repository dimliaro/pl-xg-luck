# Premier League: Luck or skill?

**Question:** 
Which PL teams are genuinely good and which are lucky? how early in the season can we tell?

In this project we explore whether a team's results reflect real quality or luck — and whether we can spot overperformers early enough to predict a drop.

Which teams are overperforming this season, and should we expect them to drop? 

**Data:** Understat (team match-level xG and expected points), via `jeke-understat-scrapper`.
## Progress
- **Session 1:** Pulled 2025/26 season data, compared actual points vs expected points (xPts).

![Luck chart](luck_25_26.png)

**First finding:** Aston Villa earned ~14 points more than their chances justified and
finished 4th; based on xPts alone they'd have been 12th. Wolves were ~15 points below
expectation — but at 35 xPts they would still have been relegated.

Open question: is this luck or skill? Next step is to check whether over/underperformance
persists across seasons. Can we predict this season's lucky teams?


- **Session 2:**  Extended the data to 12 seasons (2014/15–2025/26, 240 team-seasons) and ranked every team-season by how far they over- or under-performed their expected points.

**Sanity Check**
Luck should roughly cancel out accross each season. In 2025/26 it summed to -20.
The reason: every draw removes 1 point from the league total (2 points for each team, leaving 1 out) 25-26 season had 104 draws versus 84 expected draws predicted by the model. To compare teams fairly, accross seasons, luck is adjusted by substracting each season's average ('luck_adj').

**5 Largest**
![Actual vs expected points](pts_vs_xpts_all(Nlargest).png)
**5 Smallest**
![Actual vs expected points](pts_vs_xpts_all(Nsmallest).png)

**Findings** 
- **Liverpool 2019-2020**  is the biggest overperofmer of the decade. 99 points from 74 expected points (+25).
But 74 points would still have made them a great team. So they were good AND lucky.
Luck sits on top of quality; it doesn't replace it.
- **Aston Villa 2025/26** (+14) ranks 7th of the decade, and 2025/26 is the only season with two teams in the top 10 (Villa and Sunderland).
- **Manchester United** appears twice in the top 10 (2017/18 and 2023/24), but six years apart with different managers and squads. Even though I'm a United fan, that's not evidence that overperformance persists.

**Model limitation:** xG measures the quality of chances, not the quality of the goalkeeper (David De Gea saving the Titanic!)
facing them. An elite goalkeeper season shows up here as "luck", even though it's skill.

**Next (Session 3):** Does luck in one season predict luck in the next? If it's mostly luck, the relationship should be close to zero.