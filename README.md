# paper-replication-scalable-oversight

This is code for a replication for the algoverse ai safety fellowship trial week. 

generate_summaries_and_poems.ipynb is where you can generate the summaries and poems used for the pairwise and individual tests. for poems test I only tested on gpt-4.1 nano and claude 3 haiku

generate_answers_summary.ipynb: this is the notebook where you can run the individual and pairwise recognition and preference experiments. The only model I tested its capabillity for pref and recog was gpt-4.1-nano as claude 3 haiku doesnt allow you to get log probabillities.

generate_answers_poem.ipynb: this notebook will allow you to do everything the summary notebook does except for poems.

generate_graphs.ipynb: This allows you to generate graphs for the different experiments.

Analysis: We can see from the graphs self-preference individual preference is consistent with results from the paper: it shows 50/50 preference towards other models summaries. Individual Self-recognition however shows a stark decline down to 30-40 percent, which could be caused by the capabillities of gpt-4.1-nano as it is meant to be fast but not super capable like gpt-4 or 3.5. This is further justified by LLama being the highest one because they are similar sized models meant for fast inference. In the pairwise experiments we got a slightly unexpected result. Referencing from the paper, we should expect the human response to be the highest but we do not see this, however we do see consistent 50/50 for both self-preference and self-recognition in the pairwise setting similar to the paper. You can see all the graphs in the generate_graphs notebook.

For poetry, we see a similar behavior in the pairwise setting. Summarization is not a similar task to writing a poem however writing style can be translated to both, which is one hypothosis to why they are similar.
