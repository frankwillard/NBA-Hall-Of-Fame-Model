# NBA Hall Of Fame Model

*Project in progress

## Overview

In the eyes of voters, what makes an NBA player worthy of induction into the [Basketball Hall of Fame](https://www.hoophall.com/)?

We are using player stats and allocades scraped from [Basketball Reference](https://www.basketball-reference.com/) to predict whether an NBA player will be inducted into the Hall of Fame once they are eligible. Specifically, we hope to train a model to accurately identify Hall of Fame players across NBA history. Then, using this model, we will predict the current Hall of Fame likelihood of active NBA players based on their in-game statistics and awards.

## Player Web Scraper

Using Beautiful Soup, we parsed through each player pages on [Basketball Reference](https://www.basketball-reference.com/) to scrape relevant metadata and player statistics. An example of a player statistcs page can be found [here](https://www.basketball-reference.com/players/j/jamesle01.html). In total, we scraped data from four sections of each page, including:
  1. Player metadata (their name, their most common position, whether they are eligible for the Hall of Fame)
  2. Accolades (number of league-wide awards including All-Star selections, All-NBA selections, NBA championships, and more)
  3. Traditional statistics (per-game and career totals for categories like points, rebounds, assists, FG%, TS%, etc.)
  4. Advanced metrics (VORP, box plus-minus, win shares, etc.)
  
After being scraped, this data is compiled in a dataframe with each player representing a row. The scraper can be found in the `Player_Web_Scraper` notebook, with the resulting dataframe saved as `Scraped Player Data.csv`

