# Winnipeg Sports API
*Created by Group 14*

## Description
- **Manitoba sports event API**

- This is a basic restful API which is used to give information about Winnipeg sports teams including the Jets, Bombers, and Goldeyes. It gives information about the team that you are looking for roster and also line up of the match.

## Parameters
**teamName** (String) The name of the team

**year** (integer) The year of game play 


## Endpoints
**nextGameInfo(teamName)**: returns when & where the team is playing and who its against.

**roster(teamname, year)** : returns a list of the team members in the selected year.

**playsTonight(teamName)**: returns a true or false if a team is playing tonight.

## Resources
> "game":
>   {
>
>     "teamName": "Winnipeg Jets",
>
>     "when": "2020-11-20-19:00UTC",
>
>     "opponent": "Calgary Flames",
>
>     "where": "Winnipeg"
>
>   }

> "roster":
>   {
> 
>       "teamName": "Winnipeg Jets",
>
>       "players": [ 
>       "Tobias Enstrom", 
>       "Dustin Byfulgien",
>       "Andrew Ladd"
>       ],
>
>     "year": "2018"
>
>   }
>       

## Sample requests

This is the sample request to get a team's next fixture information:

>       https://winnipeg_sports_api/json?teamName="Winnipeg Jets"


This is the sample request to get a team's roster information:

>       https://winnipeg_sports_api/json?teamName="Winnipeg Jets"&year=2020


This is the sample request to get information that a team plays tonight:

>       https://winnipeg_sports_api/json?teamName="Winnipeg Jets"

