Sentiment Analysis of Nepal’s 2025 Election News
In September 2025, Nepal gained global attention after electing its first female Prime Minister using Discord as the “maiden”. Unlike prior regime changes, this election was significantly shaped by online discourse and digital platforms, an unprecedented intersection of democracy and the internet. This Project is a sentiment analysis of data created by scraping web news articles and blogs to examine how major English language media outliers portrayed this political transition. 

Experimental analysis was performed using a transformer, however, the final analysis was done using TextBlob and VADER. 

This project helped me develop an intuitive understanding of two important concepts 1.Overfitting vs Generalization  
and 2. Importance of collecting good quality data. 

A very interesting thing that I realized about my code is that every time the scrapping script is run, it collects data from the most recent version of each website. This causes slight variations in the collected data which also affects the end results which can be observed through the difference in visualizations gathered on December 4th and December 15th. 
TextBlob provided a sentiment distribution for long form news articles which was quite different from the results produced by VADER which exhibited greater sensitivity to contextual modifiers. 

With analysis done on a wider range/ better quality of data I can say that I prefer the analysis done by Textblob- 
1. Using polarity as a metric, Textblob provides a more factual analysis of the text collected from these articles.
2. VADER seems to sway its output with short bursts of emotional words (protest=’always negative’, new prime minister=’ always positive’). It misses a lot of nuance which is extremely necessary for accurate sentiment analysis. It over amplifies the intensity often resulting in a poor analysis of long form content where relative meaning of phrases and the context of the situation are extremely important to consider.
3. Textblob explicitly models subjectivity which helps clearly distinguish facts from opinions. It can work well with text which has a lot of sentimental noise which could otherwise trick algorithms like VADER.
4. TextBlob works well on full articles, like newspaper text, because it computes polarity based on the sum of all words’ sentiment.
5. Gives a polarity between -1 and +1, which is easy to interpret.

