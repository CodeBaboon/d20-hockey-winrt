d20 hockey winrt
===============

This project is designed to bring the 1980's pen-and-paper hockey dice game invented by Jim Harris to life as a Windows 8 JavaScript application. Furthermore, it aims to add some (optional) enhanced gameplay elements to the classic formula.

##original gameplay

The premise of the game is simple: write the names of 20 hockey players in a list, then simulate their annual point totals by rolling a 20-sided die. 

The season is split into 4 quarters of 20 games each. Beginning with the first player in the list, the die is rolled twice: once to represent the number of goals scored in the quarter, and once to represent the number of assists. This gave a total number of points for the quarter and was logged on the paper in the format 6-17-23.

After determining the quarterly totals for one player, the process is repeated for each player down the list. This quarterly process is repeated 3 more times to get the totals for all four quarters, which are then summed up for the final season total of each player.

At the end of each season it's fun to analyze the results, noting who the goal, assist, and points leaders were. But the real fun begins once multiple seasons have been played, when certain players inevitably displayed (completely random) patterns of success or failure. Generally low-performers would be culled from the 'league' every few seasons and replaced with new ones. Reviewing the careers of past players and cheering for the surviving 'old-timers' brought great joy our hearts.

##enhanced gameplay

The Win8 implementation of d20 hockey will provide the ability to define player attributes that will add flavor to the game play. Attributes such as sniper, playmaker, clutch, or consistent will add modifiers to dice rolls.

To enhance the career element players can be given hidden generated 'career arcs' that will modify their results. Players can also retire for age reasons rather than only through poor performance. Injuries will be a possibility, and injuries sustained in one season may negatively impact results in future seasons, increase the possiblity of future injuries, or perhaps force the player into retirement.

Finally, players will earn 'experience points' during the season that can then be used in the off-season to purchase new attributes, remove negative attributes, or stave off age-related decline.

##features

- create 0-to-many leagues
  properties: league name, player count, mode (freeplay|original|career)

  - each league has 0-to-many seasons
    properties: year

    - each season has 0-to-many players
      properties: name, team, age, g/a/pts per quarter

- store data in HTML5 IndexedDb
- ** future ** export/import data to/from file or cloud


##stories

* list leagues
* create league
* delete league
* open league

* list seasons
* create season
* delete season? (don't think so)
* open season

* add new player to season
* add existing player to season
* start season
* advance season (roll dice)
* complete season (awards)

* review player details
* review season details (leaders, awards)
* review league leaders (goals, assists, points, awards)
