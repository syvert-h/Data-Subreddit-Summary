# Data-Subbredit Summariser

Interactive jupyter notebook which extracts and summarises key information from top and hot posts in r/dataanalysis and r/datascience. 

We can filter by Subbredit, Flair, Origin (Top or Hot), Keyword Search Titles, Descriptions, or Comments to get the following...
- Interactive Data Table: summarise text (there is no graphical implementation for sentences of text).
- Interactive Word Cloud: highlight the most important keywords in a title, description or comment.

### Motivation:
I am a follower in the r/dataanalysis and r/datascience subbredits. I found the adundance of advice and ideas to be very useful. However, I came across a problem where I did not have the time and patience to thoroughly read through hundreds of posts. Hence, I have created this interactive notebook to do this work for me, gathering the information into a more digestable manner.

### More Background:
I created a python script which extracts posts from r/dataanalysis and r/datascience using the reddit API PRAW. I extracted ~300 posts from each subbredit, along with the 10 best comments from each post. The scraped data is cleaned, before using Natural Langauge Processing (NLP) to extract the keywords and summaries from the text. Then using the ipywidget+IPython packages, I create interactive data tables and word cloud within the jupyter notebook.

Note:
- Since one post can have many comments, we combine concatenate all comments before summarising. In addition, we average the score of all comments to represent this summary.
- Extractive text summarisation is used (not abstractive)

### Technology Used:
- Python: PRAW, Pandas, NLTK, Yake, matplotlib, IPython, ipywidgets, jupyter notebook

### Future Improvements:
1. Highlight keyword in summarised text:
As stated before, making the information more digestable was important for me. Data tables can be overloading at times, so highlighting the key information will help the reader.

2. Implement a word graph:
Word graphs are similar to word clouds, except they show how often words are related. I'd like to implement this to better understand how keywords of posts interact with one another.