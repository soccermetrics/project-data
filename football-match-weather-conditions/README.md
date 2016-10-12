Football Match Weather Data
===========================

This folder will contain data of weather conditions at football matches.  The objective is to create a database to support studies on the effect of environmental conditions on football.

The initial collection of competitions are listed below:

| Competition                | Season  | Filename                        |
|:---------------------------|:--------|:--------------------------------|
| Argentina Primera División | 2016-17 | `argentine-primera-2016-17.csv` |
| English Premier League     | 2016-17 | `english-premier-league-2016-17.csv` |
| French Ligue 1             | 2016-17 | `french-ligue-1-2016-17.csv` |
| German 1.Bundesliga        | 2016-17 | `german-bundesliga-2016-17.csv` |
| Italian Serie A            | 2016-17 | `italian-serie-a-2016-17.csv` |
| Spanish Primera División   | 2016-17 | `spanish-primera-2016-17.csv` |
| Major League Soccer        | 2016    | `major-league-soccer-2016.csv` |

These datasets contain the following fields:

| Field            | Description                    | Type   |
|:-----------------|:-------------------------------|:-------|
| Matchday         | Matchday of league competition | Number |
| Home Team        | Name of home team              | String |
| Away Team        | Name of away team              | String |
| Kickoff Temp     | Temperature at kickoff (deg Celsius) | Float (XX.X) |
| Kickoff Humidity | Relative humidity at kickoff (percent) | Integer |


Sources: Wikipedia, official league websites
