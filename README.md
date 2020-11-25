
# An Analysis of Hateful Online User Comments
2020 has truly been a rollercoaster ride of a year so far- a worldwide pandemic, economic downturn, racial unrest following the death of George Floyd, just to name a few. In light of recent events, I wanted to analyze online user comments to uncover the different types of online hate speech and extract insightful patterns. This analysis was based on web scraping comments from Disqus, an online public comment sharing platform where users create profiles to participate in interactive conversations. 

# Overview - Topic Modeling
![hate_overview](images/hate_overview.png)
Topic Modeling is an unsupervised NLP method which aims to discover the abstract "topics" (themes) that are present in a collection of documents (in this case, a bunch of comments). Specifically, I used Nonnegative Matrix Factorization (NMF), which is widely used for dimensionality reduction as it automatically extracts sparse and meaningful features from a set of nonnegative vectors. 

It's evident that in terms of hate speech, comments are either extremely racist (topic 1) or indicate violent intentions/behaviors (topic 4). 

![proportion_bargraph](images/proportion_bargraph.png)
![proportions_overtime](images/proportions_overtime.png)
Data visualizations are also used to analyze topic proportions. For example, we can see that almost 20% of tokenized comments fall under topic 9, a highly racist topic with racial slurs and demeaning words. In addition, the proportion of comments under this topic (pink line) also began spiking from August to September, which corresponded to the heightened racial tensions in the United States following the Black Lives Matter movement and months of civil unrest during the summer. Note that the topic proportions over time graph is supposed to be interactive, which utilizes the plotly library. 

# Detailed Analysis 
![example_topic](images/example_topic.png)

Diving even deeper, the top 10 keywords and representative documents (comments) are used to describe a given topic. In this example, topic 4 is filled with comments attacking the Democrats (i.e. comment 3: "Obama administration criminals like Biden") as well as displaying violent intentions (i.e. comment 8: "cut all their heads off"). Indeed, topic 4's top keywords correspond to the violence mentioned in the representative comments mentioned above.

![hate_fluctuation](images/hate_fluctuation.png)
![proportion_to_total](images/proportion_to_total.png)

The volume of hate speech (figure 1: Hate Speech Fluctuation) moves in the same directions as the overall topic proportions over time, which peaks at August and September. Subsequently, I analyzed the ratio of hate/offensive speech to the total volume of online comments.

Interestingly, the proportion of hate speech (to total volume) started increasing since May (figure 2: Proportion to Total Volume) while the proportion of offensive speech began decreasing. In fact, the hate and offensive speech proportions had been moving inversely, which indicates that users in general might've started substituting offensive words with more hateful language.

We can also take a look at the offensive speech topics at a high level. These comments are still racist and bipartison but to a lesser extent compared to the hate speech. There are a few interesting yet distinct "offensive" topics, such as topic 13 where people were talking about how they no longer support watching pro sports such as the NBA. In addition to the racist and violent topics, another fascinating one is topic 7, where users were saying Biden would "get covid an hour before the presidential debate." 
![offensive_overview](images/offensive_overview.png)
