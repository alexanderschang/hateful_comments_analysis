# Analysis of Online User Comments
This analysis was based on web scraping comments from Disqus, an online public comment sharing platform where users create profiles to participate in interactive conversations. 

![hate_overview](images/hate_overview.png)
# Topic Modeling
Topic Modeling is an unsupervised NLP method which aims to discover the abstract "topics" (themes) that are present in a collection of documents (in this case, a bunch of comments). Specifically, I used Nonnegative Matrix Factorization (NMF), which is widely used for dimensionality reduction as it automatically extracts sparse and meaningful features from a set of nonnegative vectors. 

It's evident that in terms of hate speech, comments are either extremely racist (topic 1) or indicate violent intentions/behaviors (topic 4). Diving even deeper, we can analyze more details for a given topic: 

![example_topic](images/example_topic.png)
