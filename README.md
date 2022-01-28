# Exploratory Data Analysis: You Should Absolutely Bet on the Better QB Getting Points
![Fitzmagic](https://sportshub.cbsistatic.com/i/r/2020/12/27/0132b98e-b98b-481b-9438-13464d7d6b96/thumbnail/770x433/0c1af51e24fd164bef87c796f1c8d548/dolphins-fitzpatrick-mahomes.jpg)
<sub><sup>cbssports.com</sup></sub>

# Introduction

I listen to alot of football podcasts. Some about the draft, some that go nitty gritty on the film and, some of my favorites, about betting lines. I do not actually gamble very often myself, but analyzing football as a market and the true ways teams are perceived is endlessly fascinating. One of the things I hear over and over again is that “the better QB is getting points!” If a “better” QB is an underdog in a game it's thrown out as ironclad reasoning for betting on their team. The QB is responsible for so much of a teams performance that intuitively it makes sense that when a “better” QB is being spotted points, the market may have overweighted other factors or simply misevaluated the QBs based on recency bias. On the other hand there are various studies on human decision making, especially when we decide what to believe, that make me dubious when such phrases are thrown around as facts. Just hearing something from someone we respect can stick in our brain, then we naturally find evidence to back up our belief whether or not it is true. I always try to investigate when I hear a phrase that is said in such a way as if it provides its own evidence. In this case however, after a look at the data, we can say “the better QB is getting points” with even more conviction. Over the past three years, when the better QB was an underdog, they covered over 60% of the

# Methodology: What is Better?

I decided to stick with a (relatively) simple measure of quarterback performance: completion percentage over expectation combined with expected points added. 
Expected points added or EPA is a way of measuring how many points each play is worth. Obviously in football every play is not a scoring play, but based on field position and down and distance you can calculate how much a play increased or decreased your probability of scoring points. This article from inside the pylon provides a great history of EPA, dating all the way back to 1971 and Bill Walsh QB and statistician, Virgil Carter. It's also important to note that there is no standardized way of calculating EPA, I used Ben Baldwin and Sebastian Carl’s measure from rbsdm.com.

Completion percentage over expectation is a measurement with similar intuition invented by Ben Baldwin. Based on factors like the down and distance, area of the field(middle or not middle), the distance the pass traveled in the air and whether or not the QB was getting hit as he threw, he created a  calculation for how often passes were expected to be completed in that situation and subtract that from the result. It's a way of quantifying those special plays we see every week where Josh Allen flings it 30 yards with a defender draped all over them. While also penalizing him if he throws a five yard slant in the dirt from a clean pocket.

Importantly both these metrics rely only on the results of a play. I do believe there are situations where a pass “should” have been caught or “should” have been intercepted but trying to introduce human judgment to measure these things inherently introduces noise and over a large enough sample size, luck usually evens out. Furthermore, even if they are not perfectly “fair” measures, who cares? If they are predictive of whether or not a team covers the spread it doesn’t matter if they are perfectly accurate representations of everything that happens on the football field. It doesn't matter if you like watching a quarterback play if they consistently win games and cover spreads. 

#Data Sources

My data came from three sources: This dataset from Kaggle by user Spreadspoke for the betting lines, this github repo for weekly player data, developed by Sebastian Carl, Ben Baldwin, Lee Sharpe and Tan Ho, and CPOE+EPA data from RBSDM.com, also authored by Sebastian Carl and Ben Baldwin. The betting line data came from pro football reference, who do not specify the book the obtained it from. 

#Results

I examined the past three years, 2019, 2020 and 2021 and in all three years, when the quarterback with the higher career composite CPOE+EPA prior to the year studied, was an underdog, they covered over 60% of the time and some years close to 70%. There were only around 30 such games a year. This is partly because I only used games where I had previous career data for both quarterbacks, which removed a ton of games each year, and partly because the market can be relied on to not make the better QB an underdog very often. 

I also looked at whether this was just a better QB thing, and the better QB did cover about 52% of the time, 10% lower than when they were underdogs. 

Two things jump out at me for this graph, when the spread is less than 2.5, betting on the dog QB is kind of a crapshoot. This is to be expected to some extent as games less than 3 are essentially a tossup because of the nfl scoring system and where games historically land. You would think 2.5 would be no different, and it's only about 10 games, but in those games the underdog better QB did cover 8 times out of 10. With a spread of 3 or greater, the underdog QB covered 70% of the time. 

The mean spread when a better QB is an underdog is 3.71, here's the distribution. As spreads do, they are clustered around 3. All the way on the left there is a week 7 game between the dolphins and the bills, where the dolphins were a whopping 17 point underdog. At the time (according to the metrics I used, please don’t kill me Bills Mafia) Ryan Fitzpatrick was the “better” QB than Josh Allen. They lost the game 31-21 but hell yeah Fitzmagic covered. It's crazy to think that Just three years later, Fitzpatrick would be sitting in the buffalo stands in 9 degree weather, shirtless, watching Allen put on the greatest QB performance ever. 

