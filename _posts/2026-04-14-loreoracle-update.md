# LoreOracle - Update 4/14

## Objectives
For this update, I immediately went to tackle two nagging issues. For one, the streamlit interface was simply too slow. For two, the time from query to query loading to answer from the LLM was simply too long. These combined factors created a lagging, slow user experience.

## Techniques
- To solve the issue with the streamlit interface being too slow, I performed several interventions. First, I updated the index database to only recompile when a flag is passed. This prevents some of the overhead of having to redo it on every start. Secondly, I used several of the
built in streamlit caching functions to prevent certain bits of code being constantly ran by the streamlit instance.
- To solve the issue with the LLM being slow to respond and often timing out, I changed several aspects of the code. First, I decreased the chunk size for the RAG DB. This alone heavily sped up retrieval, but it did come at a cost of accuracy of summarized responses. I also switched from a tree-summarization return model to a compact one, which again sped up return time.

## Lessons Learned
The biggest lesson here was more information on how different parameters of chunking and summarization affect the complexity of model usage. By increasing the similarity_top_k, we increase the amount of sources the engine can pull from. By implementing MMR query mode, 
we can increase the diversity of those sources. By decreasing the chunking sizes, we speed up the summarization of the sources and get our answers faster. Each of these has a trade-off that has become more apparent to me as I've worked through these issues.

## Forward
Next up is adding this functionality directly into the Chronicler app! I'm looking for permission from the dev to ensure I'm not violating any licenses, but getting this tuned and in there is an exciting prospect for me!
