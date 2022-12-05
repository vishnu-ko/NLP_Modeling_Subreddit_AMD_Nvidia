# Project3:  Web API & NLP
---
### Problem Statement
---
As a Data Scientist working at a startup company, I recieved a request from Reddit in which it informed that there was a bug in their system that caused switching of similar subreddits. Due to Reddit being busy with other issues, they assigned us to help with the problem. Our company agreed to work on the issue. To be able to analyze and figure out how to look at the subreddits, I started with a sample in which I chose Nvidia and AMD. To be able to distinguish these subreddits I used different models that include Logistic Regresion, RandomForest, and DecisionTree. By using these methods I will make a confusion matrix in which I can look at true negatives, true negatives, false positives, and false negatives. From looking at the confusion matrix, I can see if the three models worked or not. A successful final model would have the lowest number of false positives and false negatives.  


### Background
---
The dataset that will be used to obtain the model was from two subreddits: Nvidia and Amd. The two companies are competitors when it comes to making GPU. They are known to enhance gaming performance and have a subreddit page on Reddit.  

https://graphicscardhub.com/amd-vs-nvidia/#:~:text=Both%20AMD%20and%20NVIDIA%20are%20reputed%20and%20big,competitor%20of%20Intel%20in%20the%20desktop%20processors%20category.

---
### Datasets used
amd_df.csv : This includes multiple features: subreddit, id, author, created_utc, is_self, selftext, and title.  

nvidia_df.csv : This includes multiple features: subreddit, id, author, created_utc, is_self, selftext, and title

combined_dataframe.csv : This includes multiple features from both nvidia_df.csv and amd_df.csv and will be the dataframe that gets analyzed to solve the problem statement. 

---
### EDA Analysis
---
After cleaning up the data and looking at the multiple histograms and correlation pots, I will be able to answer the problem statement. This is due to the fact that I'm able to believe with the cleaning that was done, it will be able to distinguish without having unnecessary noise. When it comes to the outliers, I will keep them due to the fact that they have content that will help in dinstinguishing the data as well. Overall, after comparing the data, I believe I can answer the problem statement present and help reddit. 

---
### Preprocessing Analysis
---
After doing the lemmatization and stemmation and looking at both of the columns, I felt that Lemmatization used the right words when it came to explaining the ideas or the conversations in the columns. I felt Stemmation, didn't do a good job, so moving forward, I'm going to go with the lemmatization column. 

---
### Conclusion
---
From the three models that were presented above with countvectorizer, it can be seen that the logistic regression with countvectozier did the best. This can be seen from the fact that we ended up with no false positive or false negatives. In this model, we saw that there were 2,625 in total of true posiitve and true negative categories. The best parameters for logistic regression was max_df of 0.9, max_features of 1000, mind_df of 1, and ngram range of (1,1). This is the model that we will be going with due to the lowest number of false positives and false negatives. When comparing that to randomforest and Decisiontree, they both came out with similar results, but were lower than Logistic Regression. They did have the same parameters as logistic regression. As it can be seen from the gs score for both of them. They had a training score of 1 and a testing score of .9988. These also portrayed really good models at the end in which only 3 were found in the false positive group. Overall, all three models did better than the baseline. Even though the data and models are showing good results, there needs to be a consideration on why the model is doing so well. From what can be seen, it seems that the two subreddits are very similar when it comes to what the companies do and what they are providing. In my further steps, I will need to look into more indept the similarities in words that exist between the two companies. Even though the model did a great job when it came to these two subreddits, it needs to be checked thorougly for other subreddits.  
