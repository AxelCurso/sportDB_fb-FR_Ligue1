# :soccer::fr: Database for Ligue 1 :fr::soccer:
*My small contribution to have all the statistics in a handy way*

[Why](#why)<br/>
[How the files works](#how-the-files-works)

## Why
For my personal work, I needed all the statistics of the french first division of football. But there was no database listing every  statistics of that league. Surely there was some but no one were free or easy to use. (Maybe I didn't search well too)<br/>
So I tried to do it myself.<br/>
Then I made some scripts to scrapes the official website of the Ligue 1 (https://www.ligue1.fr).<br/>
And here are all the statistics given by the website. We have the standings bit and the individual match statistics as well.<br/>
*Nb: We have the statistics of the individual match only since the season 2020-2021!*<br/>
<br/>
***If there is any errors, please tell me.***<br/>
***I try my best to keep the database up to date.***

## How the files works
- **Teams.csv**: The id to name file
	- *id*: The id of the team for this database
	- *abbr*: The abbreviation of the team name
	- *fullName*: The full name of the club

*Every season is on there folder*
- **matchs.csv**: Has the statistics for every match of the season
	- *id*: The id of the match according to the Ligue 1 website
	- *date*: An int with the format `YYYYMMDD`
	- *hour*: An int with the format `hhmm`
	- *leagueMatchNb*: The week match
	- *id[Home/Away]*: The id of the team in the `Teams.csv` file
	- *\[home/away]Team*: The abbreviation of the team name
	- *\[h/a]_score* : The number of goals scored by the team
	- *\[h/a]_possession*: The percentage of possession
	- *\[h/a]_duelsWon*: The percentage of duel won
	- *\[h/a]_aerialDuelsWon*: The percentage of duel won in the air
	- *\[h/a]_interceptions*: The number of interceptions realized
	- *\[h/a]_offPlays*: The number of offside committed
	- *\[h/a]_corners*: The number of corner obtained
	- *\[h/a]_passes*: The number of passe tried
	- *\[h/a]_longPasses*: The number of long passe tried
	- *\[h/a]_succeededPasses*: The percentage of passe succeeded
	- *\[h/a]_succeededPassesOppositeSide*: The percentage of succeeded passes in the opposite side
	- *\[h/a]_centers*: The number of crosses tried
	- *\[h/a]_succeededCenters*: The percentage of crosses succeeded
	- *\[h/a]_shots*: The number of shot attempted
	- *\[h/a]_targetedShots*: The number of shot on target
	- *\[h/a]_counteredShots*: The number of shot blocked
	- *\[h/a]_extSurfaceShots*: The number of shot tried outside the box
	- *\[h/a]_intSurfaceShots*: The number of shot tried instide the box
	- *\[h/a]_precisionShots*: The percentage of shots on target
	- *\[h/a]_tackles*: The number of tackle tried
	- *\[h/a]_succeededTackles*: The percentage of tackle succeeded
	- *\[h/a]_clears*: The number of clearance
	- *\[h/a]_concededFaults*: The number of foul conceded
	- *\[h/a]_yellowCards*: The number of yellow card obtained
	- *\[h/a]_redCards*: The number of red card obtained
<br/>

- **standing.csv**: The standing of the league for every match week
	- *leagueMatchNb*: The match week number
	- *1st[..]20th*: The abbreviation of the team name at the specific place
<br/>

- **[1st..20th]PlaceOverTime.csv**: The evolution of a specific place in the league for every match week
	- *leagueMatchNb*: The match week number
	- *teamName*: The abbreviation of the team name
	- *points*: The number of points after `leagueMatchNb` match
	- *wins*: The number of wins after `leagueMatchNb` match
	- *draws*: The number of draws after `leagueMatchNb` match
	- *loses*: The number of loses after `leagueMatchNb` match
	- *goalsFor*: The number of goals scored after `leagueMatchNb` match
	- *goalsAgainst*: The number of goals taken after `leagueMatchNb` match
	- *goalsDiff* : The difference of goals scored and goals taken after `leagueMatchNb` match
