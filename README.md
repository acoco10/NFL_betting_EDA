# You Should Absolutely Bet on The Better QB When They Are an Underdog
I listen to alot of football podcasts. Some about the draft, some that go nitty gritty on the film and, some of my favorites, about betting lines. I rarely gamble myself, but analyzing football as a market and the true ways teams are perceived is endlessly fascinating. One of the things I hear over and over again is that “the better QB is getting points!” If a “better” QB is an underdog in a game it's thrown out as ironclad reasoning for betting on their team. The QB is responsible for so much of a teams performance that intuitively it makes sense that when a “better” QB is being spotted points, the market may have overweighted other factors or simply misevaluated the QBs based on recency bias. 

On the other hand there are various studies on human decision making, especially when we decide what to believe, that make me dubious when such phrases are thrown around as facts. Just hearing something from someone we respect, or that makes sense to us, can stick in our brain, then we naturally find evidence to back up our belief whether or not it is true. I always try to investigate when I hear a phrase that is said in such a way as if it provides its own evidence. In this case however, after a look at the data, we can say “the better QB is getting points” with even more conviction. Over the past three years, when the better QB was an underdog, they covered over 60% of the time, in games where the spread was 2.5 points or more, they covered over 80% of the time. 

## Methodology: What is better?

I decided to stick with a (relatively) simple measure of quarterback performance: completion percentage over expectation combined with expected points added. 

Expected points added or EPA is a way of measuring how many points each play is worth. In football every play is not a scoring play, in fact very few are. EPA aims to quantify how many points each play was regardless of whether it was a scoring play. Based on field position and down and distance you can calculate how much a play increased or decreased your probability of scoring points. This article from inside the pylon provides a great history of EPA, dating all the way back to 1971 and Bill Walsh QB and statistician, Virgil Carter. It's also important to note that there is no standardized way of calculating EPA, I used Ben Baldwin and Sebastian Carl’s measure from rbsdm.com. By looking at dropback EPA, the aim is to quantify how much each passing play is worth in order to show the value generated each time a quarterback throws a pass. 

Completion percentage over expectation is a measurement with similar intuition invented by Ben Baldwin. Based on factors like the down and distance, area of the field(middle or not middle), the distance the pass traveled in the air and whether or not the QB was getting hit as he threw, he created a  calculation for how often passes were expected to be completed in that situation and subtract that from the result. It's a way of quantifying those special plays we see every week where Josh Allen flings it 30 yards with a defender draped all over them. While also penalizing him if he throws a five yard slant in the dirt from a clean pocket.

## Data sources
My data came from three sources: This dataset from Kaggle by user Spreadspoke for the betting lines, this github repo for weekly player data, developed by Sebastian Carl, Ben Baldwin, Lee Sharpe and Tan Ho, and CPOE+EPA data from RBSDM.com, also authored by Sebastian Carl and Ben Baldwin. 



## Results 
In games with an underdog better QB (UDBQB) the UDBQB covered 65% of the time. I examined the past three years, 2019, 2020 and 2021. There were only around 30 such games a year. This is partly because I only used games where I had previous career data for both quarterbacks, which removed a ton of games each year, and partly because the market avoids UDBQBs. 

![Distribtuion_spread_underdog](https://github.com/acoco10/NFL_betting_EDA/blob/main/graphs/Dist_allQB.png)
Figure 1 shows the distribution of spreads for UDBQBs. When the spread is less than 2.5, betting on the underdog QB is kind of a crapshoot This is to be expected to some extent as games less than 3 are essentially a tossup because of the nfl scoring system and where games historically land. You would think 2.5 would be no different, and it's only about 10 games, but in those games the underdog better QB did cover 8 times out of 10. With a spread of 2.5 or greater, the UDBQB covered  a staggering 83% of the time. 

I removed a week 7 game between the dolphins and the bills where the dolphins were a whopping 17 point underdog for legibility. At the time (according to the metrics I used, please don’t kill me Bills Mafia) Ryan Fitzpatrick was the “better” QB than Josh Allen. They lost the game, but I think we all know Fitzmagic covered, “only” losing by 10 (31-21). It's crazy to think that Just three years later, Fitzpatrick would be sitting in the buffalo stands in 9 degree weather, shirtless, watching Allen put on the greatest QB performance ever against the Patriots in week 1 of the playoffs. 

![Distribution_spread](https://github.com/acoco10/NFL_betting_EDA/blob/main/graphs/Dist_allQB.png)
Figure 2 shows the distribution of spreads and whether the better QB covered in all the games in my sample. The better QB covered 52% of the time in all games, more than a coin flip but significantly less than the 65% of the time they covered as an underdog. When the spread lands on 3, the better QB covers 60% of the time. There were about 20 of these games in the previous graph and 70 here, so 50 of those 70 are the favored, better QB covering when the spread is 3. 


## Limitations 

My findings are limited by the relatively small sample size of games each year where I had CPOE+EPA data from at least 300 snaps from previous seasons. Of the 784 games played from 2019-2021 I only looked at 450, of those 450 only 110 had a UDBQB. I see no reason why this reduction would not be repeatable, but looking at such a small portion of the overall sample may have introduced bias I have not considered. In the future I hope to use a more robust dataset of previous seasons and develop a way to measure in season QB performance, so that rookies or backups who have played enough games that season can be added to the dataset and QBs with prior data can have their performance more accurately measured. 

