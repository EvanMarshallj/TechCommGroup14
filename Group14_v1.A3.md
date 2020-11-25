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

**roster(teamName, year)** : returns a list of the team members in the selected year.

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

## Sample Requests

This is the sample request to get a team's next fixture information:

>       https://winnipeg_sports_api/json?teamName="Winnipeg Jets"

This is the sample request to get a team's roster information:

>       https://winnipeg_sports_api/json?teamName="Valour FC"&year=2020

This is the sample request to check if a team plays tonight:

>       https://winnipeg_sports_api/json?teamName="Winnipeg Jets"

## Sample Response 

Sample response for the above request to get next fixture for Winnipeg Jets:

>        {
>           "game":
>            {
>
>               "teamName": "Winnipeg Jets",
>               "when": "2020-11-20-19:00UTC",
>               "opponent": "Calgary Flames",
>               "where": "Winnipeg"
>           }
>       }

Sample response for the above request to get roster for Valour FC for 2020 season:

>       {
>           "roster":
>           {
> 
>               "teamName": "Winnipeg Jets",
>                "players": [ 
>                            "Matt Silva", 
>                            "Julian Dunn",
>                            "Amir Soto",
>                            "Brett Levis",
>                            "Dante Campbell", 
>                            "Raphael Garcia",
>                            "Fraser Aird",
>                            "Solomon Kojo Antwi",
>                            "Carreiro Dylan",
>                            "Cebara Stefan", 
>                            "Dyer Moses",
>                            "Gutiérrez Diego",
>                            "Hocine Chakib",
>                           ],
>
>               "year": "2020"
>           }
>       }
Sample response for the above request to check if Winnipeg Jets plays tonight:

>        {
>           "results":
>            {
>                "TeamName":"Winnipeg Jets",
>                "Date":"2020-11-23",
>                "PlaysTonight":"False"
>            }
>       }
