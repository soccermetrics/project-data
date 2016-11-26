Headed Shots / Tiros de Cabeza in/en Primera División Argentina 2016-17
=======================================================================

In late summer of 2016 Soccermetrics started to write more analytical content on South American football using detailed match data from [DataFactory](http://www.datafactory.la). This folder contains a data file that records all shots made with the head in Primera División Argentina matches for the 2016-17 season.  The data file is the result of a project whose goal is to fill in the gap in DataFactory's data coverage, which records all headed goals but not all headed shots that did not result in a goal.  Such data would enable better-quality analytical models to be trained, such as expected goal models.

Contributions from analysts and football fans is strongly encouraged.  All you have to do is record the match time at which a headed shot occurred.  You don't have to worry about who made the shot; I have that information already through DataFactory.  

-----------------

En la segunda mitad de 2016 Soccermetrics entró en un acuerdo con DataFactory para crear contenido analítico acerca del fútbol sudamericano con sus datos más detallistas.  Cubren la mayoría de las incidencias en el partido, salvo por los tiros de cabeza que no resultan en goles (tiros desviados, atajados, bloqueados, estrellados con el poste, etc).  En tanto presento este proyecto para anotar el tiempo de todos los tiros de cabeza.

Buscamos contribuciones de la comunidad de aficionados y analistas de fútbol.  Contribuir es muy fácil, sólo hay que anotar el tiempo de juego dónde hay un tiro de cabeza (que resulte en gol o no).  Nada más -- podremos localizar el evento con el tiempo de juego.

-----------------

The headed shot data is in a CSV file called `headed_shot_times.csv` and has the following fields:

Header | Definition
-------|------------
Matchday | Matchday number of competition / Fecha del torneo
Home Team | Name of home team / Nombre del equipo local
Visiting Team | Name of away team / Nombre del equipo visitante
Head Shot Time | Time of headed shot (MM : SS) / Tiempo de tiro de cabeza (MM : SS)
