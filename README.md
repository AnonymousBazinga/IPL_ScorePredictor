## Indian Premier League Score Predictor

The existing score predictor used in the IPL is based only on run rate (ex. if they go at 12 runs per over for the rest of the game, the team will score x runs in total). However, this is not very effective at real score prediction since it does not account for wickets lost, home-team advantage, stadium size/ average, innings etc. Hence, I built the score predictor with a simple gradio (and streamlit) interface to input the numbers and generate an AI predicted score considering the features.

## Data

Most of the data comes from a Kaggle dataset. You can read more about it here - https://www.kaggle.com/datasets/rajsengo/indian-premier-league-ipl-all-seasons.
I also used webscraping from https://t20-head-to-head.com/statistics-by-ipl-venue/# this website to get the average stadium score for the various venues of the 2023 IPL.

Only the required columns (runs, wickets, overs, home team, etc.) were extracted and formatted on excel for feeding into the model. Only data from 2022 was used to make the model learn based on present data rather than past playing styles (ex. more aggressive scoring, higher average scores)

## Issues

The model does not account for the form of the players. It seemed too tedious for the user to have to enter a list of all players playing in order for the model to consider their form.
