##Premier League: Luck or skill?

**Question:** 
Which PL Teams are genuinely good and which are lucky? how early in the season can we tell

In this project we are exploring this exact question. Can we determine from early on, if a team will be lucky, based on their previous seasons performances? 

**Data:** Understat (team match-level xG and expected points), via `jeke-understat-scrapper`.
## Progress
- **Session 1:** Pulled 2025/26 season data, compared actual points vs expected points (xPts).

![Luck chart](luck_25_26.png)

**First finding:** Aston Villa earned ~14 points more than their chances justified and
finished 4th; based on xPts alone they'd have been 12th. Wolves were ~15 points below
expectation — but at 35 xPts they would still have been relegated.

Open question: is this luck or skill? Next step is to check whether over/underperformance
persists across seasons. Can we predict this season's lucky teams?