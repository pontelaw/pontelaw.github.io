# JohnFantasy - NER for Free-Text Fantasy Football Queries

## Objective
The objective for this project was to enable a user of the JohnFantasy discord bot to freely query for a player's stats and status. This was accomplished through the Named Entity Recognition of players names.

## Tech Stack
- spaCy
- Discord

## Technique
To make this work, the user first queries the bot using a discord endpoint, like !predict. They then type a sentence, etc., where they ask about a player. In some cases, this looks like "Tell me about <player>", or "Who's better: <player 1> or <player 2>?". A pre-trained NER model using spacy then classifies the input.
Any found PERSON tags are then used to retrieve a player's stats and status, and is output to the discord server in a response.

## Challenges
The efficency of this model is the biggest challenge. We don't want the user waiting for multiple minutes in order to receive the results of their query, so the model must be lightweight, and the calls to the ESPN API need to be infrequent to reduce load.

## Lessons Learned
This was another big exercise in integrating a finished model into a production environment, where efficiency and uptime are key. We also had to be accurate, as poor recognition led to garbage output or missed tags.

## Futher
We are aiming to take this further in two ways. For one, we plan on obtaining or creating a corpus of NFL specific names / phrases, to ensure that we capture correctly as many of the tags as possible. We also aim to augment the free-text querying system to include intent classification, so that we can predict and subsequently output any number of player functions. As of right now, only player stat reporting is supported.
