# Statistical analysis: IGN game review

### Introduction

This R notebook uses the IGN game dataset.

The goals/questions to answer are:

* How do the sales relate to the scores, platform, genre or platform type?
* Do the scores from IGN relate to the scores from other sources? For example, reviews from users collected from GameSpot.
* What are the differences between the consoles from the same time period? For example, the consoles at the time period of PlayStation 2 vs. XBOX, PlayStation 1 vs Nintendo 64...

I will perform some statistical analysis (Anderson-Darling normality test, Wilcoxon rank sum test with continuity correction, mean via Bootstrapping) and visualizations to answer the previous set of questions.

### Data collection and Data cleaning

I use the games scores and sales from VGChartz http://www.vgchartz.com which contains a compilation of scores from different webpages and critics for the last $\sim$40 years. The data has been obtained by scrapping the webpage and stored in a csv file.

With python we have cleaned the data. In short, we performed the following:

+ We removed the fields with empty game name (unique)
+ We replaced the empty cells by NaNs
+ We created a new variable which groups the different platforms into three categories: Console, Handheld System and OS.
