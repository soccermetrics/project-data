J-League Effective Playing Time
===============================

Since 2013, the J-League has implemented a league initiative called "Plus Quality", which seeks to understand and 
improve the quality of play and reduce the amount of dead time or negative play.  With the help of their data supplier 
[Datastadium](https://www.datastadium.co.jp/en/index), the league calculates the amount of effective playing time in 
all league and cup matches and across all three divisions.

The objective of this analysis is to determine the impact of clubs on the amount of effective playing time relative 
to the average match.  In previous seasons, this analysis has been conducted with a classic regression model, but 
this season a Bayesian regression model is used.  Bayesian inference models will allow us to infer not just a point 
estimate of club impact, but its uncertainty and thus likely interval of values as well.

The effective time data is in CSV format with the following fields:

Header | Definition
-------|-----------
`home_team` | Name of home team
`away_team` | Name of away team
`apt` | Actual (or effective) playing time, in seconds

These data were used in the following articles:

* [Effective time in the J-League](http://www.soccermetrics.net/match-quality-metrics/effective-time-in-the-j-league)
* [Effective time in the J-League, part 2](http://www.soccermetrics.net/match-quality-metrics/effective-time-in-the-j-league-part-2)
* [Effective time in the J-League 2013: Who's to blame?](http://www.soccermetrics.net/match-quality-metrics/effective-time-in-j-league-2013-whos-to-blame)
* [Updating effective time analysis in J-League matches](http://www.soccermetrics.net/match-quality-metrics/updating-effective-time-analysis-in-j-league-matches)
* [Effective time in J-League 2014: Club impact in J1](http://www.soccermetrics.net/match-quality-metrics/j-league-2014-effective-time-club-impact)
* [Effective time in J-League 2014: Club impact in J2](http://www.soccermetrics.net/match-quality-metrics/j-league-div-2-2014-effective-time-club-impact)
* [Effective time in J-League 2015: Club impact in J1](http://www.soccermetrics.net/match-quality-metrics/j-league-div-1-2015-effective-time-club-impact)
* [Effective time in J-League 2015: Club impact in J2](http://www.soccermetrics.net/match-quality-metrics/j-league-div-2-2015-effective-time-club-impact)

There is also an iPython notebook that describes and carries out the Bayesian analysis. The notebook requires `pymc`,
`numpy`, and `pandas`.  To run the analysis on different files, just change the name of the `data_file` variable in
the notebook and rerun the cells.

Sources:

* J-League Plus Quality
* Datastadium Inc.
