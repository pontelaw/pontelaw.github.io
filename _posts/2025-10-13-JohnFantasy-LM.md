# JohnFantasy - A Linear Model for Projection Prediction

## Objective
The objective of this project was to create a better prediciton system for the scores of fantasy football players. Named for my son and integrated into a discord bot with the same name, its meant to represent an average 'John' in a fantasy football league.

## Tech Stack
- NFLfastR
- R
- Discord

## Technique
This project used the NFLfastR API system to obtain the latest player statistical data, which was then ran through a linear regression model to predict a players point output for an upcoming week. The goal was to find a combination of features that would provide more accurate
prediction then what was available on ESPN.

## Challenges
The biggest challenge of this project was finding the most important features to use in our model. Ultimately, the matchup ended up mattering most, that being a players past performance, and how good their next opponent was at limiting points allowed to that position group.

## Lessons Learned
Most importantly with this project, I got valuable experience in deploying a trained model, with that model being readily available for use with the JohnFantasy discord bot. Players in the discord server are able to query the bot to find better predictions dynamically, with the model being retrained weekly on up-to-date data.

## Further
In the future, the model may be moved from a linear regression model to a neural net.
