2014 FIFA World Cup Effective Playing Time
==========================================

This folder contains effective playing time data from the 2014 FIFA World Cup which was made available from the 
Soccermetrics Connect API during the competition.  Calculating the correct playing time was a challenge because the 
data supplier did not record ball-out events, so the effective time has to be estimated instead of calculated.  A 
regression model was created to estimate time lost due to the ball leaving the field and adjust the nominal effective
time; it is described in [this blog post](http://www.soccermetrics.net/soccermetrics-api/estimating-time-lost-due-to-ball-out-of-play).

This data has been used in the following articles:

* [Effective playing time at the 2014 FIFA World Cup](http://www.soccermetrics.net/soccermetrics-api/effective-playing-time-2014-fifa-world-cup)
* [Want 90 minutes of action? Play 120](http://www.soccermetrics.net/team-performance/effective-time-2014-fifa-world-cup-matches-extra-time)

Header | Definition
-------|-----------
home_team_name | Name of designated home team
away_team_name | Name of designated away team
calc_eff_time | Nominal amount of effective time, in seconds, calculated from Soccermetrics' state transition model
ball_out_events | Number of times ball has gone out of play (throw-ins, corners, goal kicks)
calc_time_lost | Nominal amount of time lost, in seconds, from ball-out events, fouls, subs, goals, other stoppages
pred_time_lost_mean | Mean predicted time lost due to ball-out events, in seconds
pred_time_lost_upper | Upper predicted time lost due to ball-out events, in seconds
pred_time_lost_lower | Lower predicted time lost due to ball-out events, in seconds

Eight rows have repeated home and away team pairs; these correspond to the eight World Cup matches that went to extra
 time.  The smaller of the calculated effective time corresponds to the extra time period.

Sources: 

* Press Association Football MatchStory
* Soccermetrics Connect API