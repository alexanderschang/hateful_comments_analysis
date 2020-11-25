# Analysis of Hateful Online Comments
This analysis was based on web scraping comments from Disqus, an online public comment sharing platform where users create profiles to participate in interactive conversations. 

![hate_overview](images/hate_overview.png)
# Overview - Topic Modeling
Topic Modeling is an unsupervised NLP method which aims to discover the abstract "topics" (themes) that are present in a collection of documents (in this case, a bunch of comments). Specifically, I used Nonnegative Matrix Factorization (NMF), which is widely used for dimensionality reduction as it automatically extracts sparse and meaningful features from a set of nonnegative vectors. 

It's evident that in terms of hate speech, comments are either extremely racist (topic 1) or indicate violent intentions/behaviors (topic 4). 

![proportion_bargraph](images/proportion_bargraph.png)
![proportions_overtime](images/proportions_overtime.png)
Data visualizations are also included to strengthen the analysis. For example, we can see that almost 20% of tokenized comments fall under topic 9, a highly racist topic with racial slurs and demeaning words. In addition, the proportion of comments under this topic (pink line) also began spiking from August to September, which corresponds to the heightened racial tensions in the United States following the Black Lives Matter movement and months of protests during the summer. Note that the topic proportions over time graph is supposed to be interactive, which utilizes the plotly library. 

# Detailed Analysis 
Diving even deeper, we can analyze more details for a given topic: 
![example_topic](images/example_topic.png)
The top 10 keywords and representative documents (comments) are used to describe a given topic. 
