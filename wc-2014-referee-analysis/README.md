2014 FIFA World Cup Referee Analysis
====================================

This folder contains mean time between fouls and stoppages for all 2014 FIFA World Cup matches.  The concept of both 
metrics is presented in [this Soccermetrics blog post](http://www.soccermetrics.net/team-performance/introducing-mean-time-between-fouls-and-stoppages).

The data has been used in the following articles:

* [A first look at MTBF for the 2014 World Cup](http://www.soccermetrics.net/team-performance/a-first-look-at-mtbf-for-the-2014-world-cup)
* [Looking at MTBS for the 2014 World Cup](http://www.soccermetrics.net/team-performance/looking-at-mtbs-for-the-2014-world-cup)

Header | Definition
-------|-----------
home_team | Name of designated home team
away_team | Name of designated away team
referee | Name of match referee
period | Match period number (1=1st half, 2=2nd half, 3=1st extra time, 4=2nd extra time)
fouls | Number of fouls (Only in MTBF file)
stops | Number of stoppages (Only in MTBS file)
MTBF | Mean time between fouls, in seconds (Only in MTBF file)
MTBS | Mean time between stoppages, in seconds (Only in MTBS file)

Sources: 

* Press Association Football MatchStory
* Soccermetrics Connect API