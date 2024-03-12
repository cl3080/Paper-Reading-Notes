# YouTubeDNN: Deep Neural Networks for YouTube Recommendations
pdf:[Deep Neural Networks for YouTube Recommendations](https://static.googleusercontent.com/media/research.google.com/zh-CN//pubs/archive/45530.pdf)

This paper is one of the most **classic** work in recommendation, especially in industry application. The goal of this paper is to present thee architecture for video recommendations developed by youtube team. The paper seems to be a "standard" architecture at first glance, however, there are many details worth deep dive and further thinking.

In a typical recommendation system, the architecture usually has two stages: **candidate generation** and **ranking**.
1. **Candidate generation:** select hundreds of items from the whole database that might be interested to users, speed is important
2. **Ranking:** find dozens of items from hundrends of items and recommend them to users, accuracy is imporant

Note: in recent applications, some systems might have a middle stage between canidate generation and ranking.
