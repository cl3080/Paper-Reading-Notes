# YouTubeDNN: Deep Neural Networks for YouTube Recommendations
pdf:[Deep Neural Networks for YouTube Recommendations](https://static.googleusercontent.com/media/research.google.com/zh-CN//pubs/archive/45530.pdf)

This paper is one of the most **classic** work in recommendation, especially in industry application. The goal of this paper is to present the architecture for video recommendations developed by youtube team. The paper seems to be a "standard" architecture at first glance, however, there are many details worth deep dive and further thinking.

In a typical recommendation system, the architecture usually has two stages: **candidate generation** and **ranking**.
1. **Candidate generation:** select hundreds of items from the whole database that might be interested to users, speed is important
2. **Ranking:** find dozens of items from hundrends of items and recommend them to users, accuracy is imporant

Note: in recent applications, some systems might have a middle stage between canidate generation and ranking.

Let break down the system and explain these two stages one by one.

## Candidate Generation
Features: **watch vector**, **search vector**, geographic embeddng, **example age**, etc

Watch vector is the taking the average of vectors for historical watched video vectors. The video vector is the embedding vectors trained from the model. Similar for search vectors.

Example age is an important feature introduced in this work to consider the freshness of the video. Typically, users prefer fresh content. The age of the video is used during training. **This feature is set to zero when predicting** so that the prediction is made at the very end of the time window.
