# LoreOracle - A RAG-Powered Custom DND Assistant

## Objective
As a frequent Game Master for mine and my friends Dungeons and Dragons games, I have amassed a large collection of lore pages within the DND Wiki-creating app Chronicler. As such, I aimed to create an assistant that could use the context of my hundreds of Wiki pages to answer questions about my created world, both for me and my players.

## Tech Stack
- Ollama
- streamlit
- Chronicler

## Techniques
This project imported my wiki pages, tokenized and generated embeddings which were then stored for further use, and used a llama3 model with those embeddings as context to take in a question and output an answer, with citations. This process was then wrapped in a streamlit GUI to give the app a professional appearance.

## Challenges
The main challenge we ran into during this project was speed. Booting up the model and tokenizing and embedding the pages was slow, and several optimization techniques were needed, like storing the embeddings and changing the API-based model used. We also simplified the streamlit interface to speed up the startup process.

## Lessons Learned
This project was a good experience in using API-based models for LLM tasks. I learned optimization techniques to get the most out of my hardware, and I learned valuable lessons in presenting models through the interface.

## Further
Going further, I believe there is still work to be done in speeding up the process. I am limited by hardware, but getting this hosted in the cloud would likely trivialize many of the issues I've had. I would also like to get this integrated into the Chronicler app, and discussions have been ongoing with the creator.
