# Starting a Research Project

This post presents the first activity performed for the Data Analysis course. It details the dataset chosen to study, presents the research question and brief reviews the problem based on the literature.


## Dataset

The dataset selected was [New York Times blog articles](https://www.kaggle.com/c/15-071x-the-analytics-edge-competition-spring-2015/data). It comprises features from online news published on NYT blog in a period of 3 months. The dataset was published as part of a [Kaggle competition](https://www.kaggle.com/c/15-071x-the-analytics-edge-competition-spring-2015).

The features available are:

  * NewsDesk
  * SectionName
  * SubsectionName
  * Headline
  * Snippet
  * Abstract
  * WordCount
  * PubDate
  * UniqueID
  * Popular

Most of the features are related to the content (Abstract, Snippet, and Headline) or to a category (NewsDesk, SectionName, and SubsectionName). UniqueID is provided only for managing purpose, while WordCount consists of a feature extracted from the full publication. PubDate provides the date and time of the publication, while Popular indicates whether a post received more than 24 comments.

## Research Interest -- Hypothesis and Question

Create popular publications is an interest for newspapers, blogs, other social media content creators. It is obvious that the content of a publication impacts on its popularity, but there are also related aspects that might influence. In this sense, the research interests led me to the question: are there other factors that impacts on the popularity of a publication with impact relatively close to the content?

To answer this question, it will be important to analyze the impact of content and category, but also use features extracted from PubDate (e.g. week day and hour). The hypothesis is: week day and hour have significant impact on determining if a publication will become popular or not.

## Related Work -- Literature Review

In order to identify relevant papers with similar interests, I have used the search terms: predicting news popularity. As result, seven papers were found to be interesting for study:

  * **Szabo and Bernardo, 2010**: perform an analysis under the perspective of general online content, not only news. Popularity is assessed in term of votes (for Digg) and views (for Youtube). The analysis considered time to identify the popularigy along week days and how online resources keep attracting attention or not. A Bayesian Network was used considering features such as day of the week, hour of the day and category.
  * **Lerman et al., 2010**: considered online news as target. The data source used was Digg, which provided as popularity measure the number of votes. The analysis was performed considering social aspects, such as the author’s network of friends/fans and their initial reaction to the post.
  * **Tatar et al., 2011**: analyzed the content of an online newspaper related to 4 years of publications and interactions with users. The popularity measure used was the number of comments. Authors use a Linear Regression to perform the prediction and considered as independent variable the number of comments in a certain period of observation.
  * **Bandari et al., 2013**: considered online news publications. To measure the popularity, the number of tweets referencing the resource was considered.  Four categories of features were considered: source, category, content subjectivity and entities referenced. Regression and Classification algorithms were used to perform the predictions. The most relevant feature found was the source of the news.
  * **Hensinger et al., 2013**: analyzed online news papers considering as popularity measure the fact that the publication was between the most read resources in a day. Instead of considering the prediction as a binary classification problem, they analyzed is as individuals competing for the popularity, which was solved by a ranking function. The features used were only based on the content, which resulted in top words from each publication.
  * **Tatar et al., 2014**: considered the context of selecting top online news for mobile users. For this purpose, used the number of comments as popularity metric and created a ranking function. The content of two online newspapers were used as datasets. The features used were: news lifetime and popularity distribution.
  * **Fernandes et al., 2015**: created a system that anticipates if the paper will be popular before the publication. The popularity measure used was the number of shares. About 60 features were used to perform the prediction, which can be categorized as related to Words, Links, Digital Media, Time, Keywords and Natural Language Processing Metrics. Several algorithms were used to make prediction, from which Random Forest obtained the best results.

The study reveled a diversity in terms of popularity metrics (e.g., shares, views, and votes) and also in terms of features. The time features identified as interesting in our analysis (i.e., week day and hour) were directly considered only in 1 paper. Other papers considered the content analysis, social aspects and popularity progress.

As result of the review, it is possible to observe the relevance and complexity of the problem, which can be approached under different assumptions and perspectives. However, the literature has indicated that it is possible to predict the post popularity based on quantitative and qualitative metrics, supporting hour hypothesis and interest.

It is worth noticing that the dataset chosen contains a limited number of information available. As the study presented, there are several attributes that might affect or have predictive influence of the popularity, such as the author popularity, users’ social aspects, number of images, subjectivity, and other.

## Bibliography

[1] Szabo, Gabor, and Bernardo A. Huberman. "Predicting the popularity of online content." Communications of the ACM 53.8 (2010): 80-88.

[2] Lerman, Kristina, and Tad Hogg. "Using a model of social dynamics to predict popularity of news." Proceedings of the 19th international conference on World wide web. ACM, 2010.

[3] Tatar, Alexandru, et al. "Predicting the popularity of online articles based on user comments." Proceedings of the International Conference on Web Intelligence, Mining and Semantics. ACM, 2011.

[4] Bandari, Roja, Sitaram Asur, and Bernardo A. Huberman. "The pulse of news in social media: Forecasting popularity." arXiv preprint arXiv:1202.0332 (2012).

[5] Hensinger, Elena, Ilias Flaounas, and Nello Cristianini. "Modelling and predicting news popularity." Pattern Analysis and Applications 16.4 (2013): 623-635.

[6] Tatar, Alexandru, et al. "From popularity prediction to ranking online news." Social Network Analysis and Mining 4.1 (2014): 1-12.

[7] Fernandes, Kelwin, Pedro Vinagre, and Paulo Cortez. "A Proactive Intelligent Decision Support System for Predicting the Popularity of Online News." Progress in Artificial Intelligence. Springer International Publishing, 2015. 535-546.
