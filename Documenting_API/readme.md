<div align="center">

# Chapter 5-  Documenting Your API

![Language](https://img.shields.io/badge/Language-Python-blue)
![SQLAlchemy](https://img.shields.io/badge/ORM-SQLAlchemy-green)
![Pytest](https://img.shields.io/badge/Testing-Pytest-blue)
![FastAPI](https://img.shields.io/badge/API-FastAPI-teal?logo=fastapi&logoColor=white)
![Pydantic](https://img.shields.io/badge/Data%20Validation-Pydantic-orange?logo=pydantic&logoColor=white)
![Uvicorn](https://img.shields.io/badge/Web%20Server-Uvicorn-purple?logo=uvicorn&logoColor=white)

</div>


# SportsWorldCentral (SWC) Fantasy Football API Documentation

Thanks for using the SportsWorldCentral API. This is your one-stop shop for
accessing data from our fantasy football website, www.sportsworldcentral.com.


## Table of Contents

- [Public API](#public-api)
- [Getting Started](#getting-started)
  - [Analytics](#analytics)
  - [Player](#player)
  - [Scoring](#scoring)
  - [Membership](#membership)
- [Terms of Service](#terms-of-service)
- [Example Code](#example-code)
- [Software Development Kit (SDK)](#software-development-kit-sdk)

## Public API
*Coming Soon*

We'll be deploying our application soon. Check back for the public API address.

## Getting Started

Since all of the data is public, the SWC API doesn't require any authentication. 
All of the the following data is available using GET endpoints that return 
JSON data.

### Analytics

Get information about the health of the API and counts of leagues, teams, 
and players.

### Player
You can get a list of all NFL players, or search for an individual player 
by player_id.

### Scoring

You can get a list of NFL player performances, including the fantasy points they 
scored using SWC league scoring.

### Membership
Get information about all the SWC fantasy football leagues and the teams in them.

## Terms of Service

By using the API, you agree to the following terms of service:

- **Usage Limits**: You are allowed up to 2000 requests per day. Exceeding this 
                    limit may result in your API key being suspended.
- **No Warranty**: We don't provide any warranty of the API or its operation.

## Example Code

Here is some Python example code for accessing the health check endpoint:

```
import httpx

HEALTH_CHECK_ENDPOINT = "/"
    
with httpx.Client(base_url=self.swc_base_url) as client:
    response = client.get(self.HEALTH_CHECK_ENDPOINT)
    print(response.json())
```

## Software Development Kit (SDK)
*Coming Soon*

Check back for the Python SDK for our API.
