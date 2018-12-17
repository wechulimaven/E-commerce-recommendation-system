# E-commerce-recommendation-system
##On Amazon Beauty Products
Recommender System； Collaborative Filtering；Content-Based Algorithm
##Abstract
Collaborative filtering and content-based technique have been proved to be two of the most successful techniques in recommender systems. In this paper we introduce and implement the recommender system by using Amazon beauty products data, through both collaborative filtering and content-based approaches. Collaborative filtering method includes memory-based approaches and model-based approaches. After performing evaluation based on the precision, we conclude that all the methods above are efficient when giving recommendation to users and model-based method has the largest precision.
## Introduction
Today, more and more business entities and industries are on the way to e-commerce, and with the popularity of machine learning and artificial intelligence, a lot of companies have adopted these techniques to serve their marketing and even doubled their sales.
According to Sucharita Mulpuru, a Forrester analyst, Amazon’s conversion to sales of on-site recommendations could be as high as 60% in some cases based on the performance of other e-commerce sites. And 35% of sales come from their recommender system.[1] This project will introduce and implement the recommender system by using Amazon beauty data because their data volume is large enough and the dimensions are wide enough to be used in a recommender system. Hope this project can give some suggestions to the platform that is considering to introduce the recommender system in the future.
Data Introduction
The dataset is accessed from Julian McAuley, UCSD. This dataset contains product reviews and metadata from Amazon, including 142.8 million reviews spanning May 1996 - July 2014.[2] In this project, we only choose the data in the beauty category from 2013 to 2014. The dataset includes 91,238 reviews (ratings, text, helpfulness votes) and 11,346 product metadata (descriptions, category information, price, brand, also bought items and image features).
## Recommender System
Many e-commerce and retail companies are leveraging the power of data and boost sales by implementing recommender systems on their websites. Recommender systems, in short, are designed to predict users’ interests and recommend items a user might be interested in. Recommender system typically generates recommendation lists in the following two ways -- collaborative filtering and content-based filtering (also known as a personalized-based approach).
### Collaborative Filtering
Collaborative filtering approaches build a model from a user’s past behavior (items previously purchased or ratings given to those items) as well as similar decisions made by other users. This model is then used to predict items (or ratings for items) that the user may have an interest in. Collaborative filtering approaches could be divided to memory-based or model-based approaches. In the memory-based approach, all ratings are stored as-is into memory (in contrast to learning an abstraction), and a recommendation for the test user can be generated by sorting the memorized ratings of similar users or items. User-based and item-based filterings fall under this category. In the model-based approach, training ratings are used to generate a model that is able to predict the ratings for items that a test user has not rated before. The advantage of the memory-based methods is having less parameters have to be tuned. However, the data sparsity and scalability problems are not handled very well. The model-based methods have the resulting ‘compact’ models to solve the data sparsity problem to a certain extent, but some useful information may be discarded during the reduction. For both memory-based and model-based methods, we choose the same way to separate the data into  training set and test set. We choose the users who rated items more than once from the year of 2013 to 2014 . Then we split the data into training set and test set by a ratio of roughly 9 to 1 such that the following requirements are satisfied. The items with rating in test set must have rating history in training set. We will discuss several specific approaches to construct algorithms and different evaluation methods in this section.
### Content-Based Algorithm
Content-based recommender systems recommend a list of items to a user based on the description of the item and a profile of the user’s interests. Content-based recommender systems can be applied to different situations such as recommending web pages, news articles, restaurants, television programs, and items for sale. Although the details of various systems differ, content-based recommender systems share in common a means for describing the items that may be recommended, a means for creating a profile of the user that describes the types of items the user likes, and a means of comparing items to the user profile to determine what to recommend. The user profile will be created and uploaded automatically according to users’ purchase history and rating scores. And the item profile will be updated as long as the description of new items are loaded in the dataset. 
In this content-based recommender system applied to the amazon beauty data, item profile is created by the item descriptions, and the user profile is created by customer’s purchase history and historical ratings. The system conduct recommendations for a specific customer based on the items that have ratings higher than the customer’s average rating.
## Summary
Recommender system is a powerful new technology for extracting additional value for a business from its user database. These systems benefit users by enabling them to find similar products they viewed or purchased, which helps business generates more sales and help consumers shop more efficiently. Recommender systems are rapidly becoming a basic and necessary tool in E-commerce on the Web. Recommender systems are being stressed by the huge volume of user data in existing corporate databases and will be stressed even more by the increasing volume of user data available on the Web. New technologies are needed that can significantly improve the scalability of recommender systems.[7]
Collaborative filtering and content-based technique have been proved to be two of the most successful techniques in recommender systems.[12] In this paper we implemented both content-based and collaborative filtering method to make recommendation to Amazon Beauty user. Model-based and memory-based approaches are included in collaborative filtering method. Each approach is evaluated by Precision, Recall, F-1 score or MAE. In our dataset, user behavior (user purchase history) is not that adequate to make full use of the advantages of collaborative filtering technique, while we have detailed description for products. It turned out that content-based approach has better performance than collaborative filtering approach on the precision basis. We also analyzed advantages and disadvantages of each approach in previous sections.
In the future we should increase the size of the dataset by collecting additional user evaluations and enlarging the time period of purchase and review records. With a larger dataset we could build larger back test dataset which could lead to a more precise evaluation result of each approach. Given the advantages and disadvantage of collaborative filtering and content-based method, we might combine advantages of these two methods by joining them, in order to reduce the limits from current approaches, such as user preference shift, Matthew effect.
