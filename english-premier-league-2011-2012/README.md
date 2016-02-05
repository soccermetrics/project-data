2011-12 English Premier League Data
===================================

This folder contains summary statistical data and contextual data from every match of the 2011-12 English Premier 
League season.  The summary statistical data is the public dataset of the MCFC Analytics project, and the 
contextual data is the result of the Enriched Data Project that Soccermetrics started in support of MCFC Analytics. 
The full data set populated an early version of the Soccermetrics API, which is a sports modeling and 
analytics layer on top of match data sources.

The data set has been revised in order to be loaded in match databases created with the latest generation of 
Soccermetrics' [Marcotti data schema](https://github.com/soccermetrics/marcotti).  In addition to making data 
available, the goal of the data set is to describe the required files and the expected fields within.  In some of the 
data files, there are `ID` fields that associated with the supplier's internal databases, but those fields are optional.

There are some fields that are not populated yet.  Relative humidity has not yet been filled for all matches, and 
some goal events are marked as "Unknown".  Some booking events are described as "reckless challenge", which may not 
necessarily be an accurate description of the foul.  

The data has been described in the following articles:

* [Introducing the Soccermetrics API](http://www.soccermetrics.net/soccer-database-development/introducing-the-soccermetrics-api)
* [Further comments on the MCFC Analytics Dataset](http://www.soccermetrics.net/match-data-collection/further-comments-on-the-mcfc-analytics-dataset)
* [Introducing the Football Match Result and Summary Database](http://www.soccermetrics.net/soccer-database-development/fmrd-summary-schema-introduction)

The dataset includes the following files:

File Name | Description
----------|-------------
Competitions.csv | Football Competitions
Clubs.csv | Football Club Names
Venues.csv | Match Venues
Players.csv | Biographical Player Data with Default Position
Managers.csv | Biographical Manager Data
Referees.csv | Biographical Referee Data
Matches.csv | High-Level Match Data
MatchLineups.csv | Starting/Bench Players in Matches
Goals.csv | Goal Events in Matches (not including Penalties)
Penalties.csv | Penalty Events
Bookables.csv | Disciplinary Events
Substitutions.csv | Substitution Events
PlayerStats.csv | Summary Statistical Data of all Players

Competitions
------------

Field | Description | Type
------|-------------|------
ID | Supplier ID of competition record | Integer
Name | Name of football competition | String
Level | Level of competition in league pyramid | Integer
Country | Country to which competition belongs | String

Clubs
-----

Field | Description | Type
------|-------------|-----
ID | Supplier ID of club record | Integer
Name | Name of football club | String
Country | Country in which club resides | String

Venues
------

Field | Description | Type
------|-------------|-----
Venue Name | Name of match venue | String
City | City/locality where venue resides | String
Region | Administrative region (state/province equivalent) | String
Country | Country of venue | String
Timezone | Timezone region of venue | String
Altitude | Venue altitude (-200 to 4500 meters) | Decimal
Latitude | Venue latitude (-90.000000 to 90.000000 degrees) | Decimal
Longitude | Venue longitude (-180.000000 to 180.000000 degrees) | Decimal
Config Date | Effective date (YYYY-MM-DD) of venue configuration | String
Surface | Type of playing surface | String
Length | Length of playing surface (90 to 120 meters) | Decimal
Width | Width of playing surface (45 to 90 meters) | Decimal
Capacity | Total venue capacity | Integer
Seats | Total seats at venue | Integer

Players
-------

Field | Description | Type
------|-------------|-----
ID | Supplier ID of player record | Integer
Country | Country of player | String
First Name | Self-explanatory | String
Middle Name | Middle name(s), if applicable | String
Last Name | Primary surname | String
Second Last Name | Second surname, usually the mother's surname | String
Nickname | Popularly known name of player | String
Name Order | Naming Order (NameOrderType) | String
DOB | Birthdate (YYYY-MM-DD) of player | String
Position | Default position of player | String

Managers
--------

Field | Description | Type
------|-------------|-----
Country | Country of manager | String
First Name | Self-explanatory | String
Middle Name | Middle name(s), if applicable | String
Last Name | Primary surname | String
Second Last Name | Second surname, usually the mother's surname | String
Nickname | Popularly known name of manager | String
Name Order | Naming Order (NameOrderType) | String
DOB | Birthdate (YYYY-MM-DD) of manager | String

Referees
--------

Field | Description | Type
------|-------------|-----
Country | Country of referee | String
First Name | Self-explanatory | String
Middle Name | Middle name(s), if applicable | String
Last Name | Primary surname | String
Second Last Name | Second surname, usually the mother's surname | String
Nickname | Popularly known name of referee | String
Name Order | Naming Order (NameOrderType) | String
DOB | Birthdate (YYYY-MM-DD) of referee | String

Matches
-------

Field | Description | Type
------|-------------|-----
Date | Match date | String
Matchday | League matchday | String
Venue | Match venue | String
Home Team | Self-explanatory | String
Away Team | Self-explanatory | String
Home Mgr | Name of home team manager | String
Away Mgr | Name of away team manager | String
Referee | Name of match referee | String 
Attendance | Match attendance |  Integer
1st Half | Length of first period | Integer
2nd Half | Length of second period | Integer
KO Time | Local time (HH:MM) at kickoff | String 
KO Temp | Temperature at kickoff (-15.0 to 50.0 C) | Decimal 
KO Humidity | Relative humidity at kickoff (0.0 to 100.0%) | Decimal 
KO Wx | Predominate weather condition at kickoff (WeatherConditionType) | String
HT Wx | Predominate weather condition at halftime (WeatherConditionType) | String
FT Wx | Predominate weather condition at end of match (WeatherConditionType) | String

MatchLineups
------------

Field | Description | Type
------|-------------|-----
Matchday | League matchday | Integer
Home Team | Self-explanatory | String
Away Team | Self-explanatory | String
Player's Team | Self-explanatory | String 
Player | Full name or nickname of player | String 
Starting | Starting player flag (1=yes, 0=no) | Integer 
Captain | Captain flag (1=yes, 0=no) | Integer

Goals
-----

Field | Description | Type
------|-------------|-----
Matchday | League matchday | Integer
Home Team | Self-explanatory | String
Away Team | Self-explanatory | String
Team | Name of scoring team | String 
Player | Full name or nickname of player | String 
Event | Shot event that resulted in goal (ShotEventType) | String
Bodypart | Body part used to score goal (BodypartType) | String
Time | Match time in minutes (1 to 90 minutes) | Integer
Stoppage | Stoppage time in minutes, if applicable | Integer

Penalties
---------

Field | Description | Type
------|-------------|-----
Matchday | League matchday | Integer
Home Team | Self-explanatory | String
Away Team | Self-explanatory | String
Penalty Taker | Full name or nickname of player taking penalty | String 
Foul | Foul event that resulted in penalty (FoulEventType) | String
Outcome | Outcome of penalty kick (ShotOutcomeType) | String
Time | Match time in minutes (1 to 90 minutes) | Integer
Stoppage | Stoppage time in minutes, if applicable | Integer

Bookables
---------

Field | Description | Type
------|-------------|-----
Matchday | League matchday | Integer
Home Team | Self-explanatory | String
Away Team | Self-explanatory | String
Player | Full name or nickname of player being booked | String 
Foul | Foul event that resulted in penalty (FoulEventType) | String
Card | Disciplinary card shown (CardType) | String
Time | Match time in minutes (1 to 90 minutes) | Integer
Stoppage | Stoppage time in minutes, if applicable | Integer

Substitutions
-------------

Field | Description | Type
------|-------------|-----
Matchday | League matchday | Integer
Home Team | Self-explanatory | String
Away Team | Self-explanatory | String
Player In | Full name or nickname of player substituted into match | String 
Player Out | Full name or nickname of player substituted out of match | String 
Time | Match time in minutes (1 to 90 minutes) | Integer
Stoppage | Stoppage time in minutes, if applicable | Integer

PlayerStats
-----------

_(With over 200 fields, it will take a while to describe all of the fields in the PlayerStats file.)_

Field | Description | Type
------|-------------|-----
Date | Match date (YYYY-MM-DD) | Integer 
Matchday | League matchday | Integer 
Player ID | Supplier ID of player record | Integer
Last Name | Last name of player | String
First Name | First name of player | String
Team | Name of player's team | String
Team Id | Supplier ID of player's team | Integer 
Opposition | Name of opposing team | String 
Opposition Id | Supplier ID of opposing team | Integer
Venue | Locale of match from player's perspective (Home/Away) | String 
Position Id | Supplier ID of player's position | Integer


Sources:

* FA Premier League
* Press reports
* Weather Underground
* Opta Sports