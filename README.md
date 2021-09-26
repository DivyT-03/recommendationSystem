# Title: Recommendation System
## Explanation: 
A recommendation system can work in 2 ways:
1.	Recommend a user based on what other user with similar interests as him/her are interested in. For example:
If user 1 watches movies A,B,C,D and user 2 watches movies B,C,D,E, then the system will recommend Movie A to user 1 and movie A to user 2. This approach is called collaborative filtering
2.	Other approach to recommend can be based on an item’s similarity with other items that the user is already interested in. This can be developed by calculating similarity matrix between objects and using it to make recommendations.
We’ll be using both the approaches to build the recommendations. Both the approaches can be interlinked to further make a robust recommender system.

## Need of a recommender system: 
A recommender system as the name states, makes recommendations to users based on input data about the previous interactions the user has had with the system. This helps the company is selective marketing and targeting for specific users and hence build profits. It also helps to improve the overall user experience for the users.

## Dataset used: 
Dataset used for this project is an open-source dataset from GroupLens Research (movielens.org)

## Working
1.	Using collaborative filtering: 
First, we import the necessary libraries and data into a DataFrame. Once the data is imported, we preprocess it (Handle missing values and unwanted data). The we perform EDA (analyzing data sets to summarize their main characteristics). Next, we filter users and movies that have been reviewed or have reviewed 3 or less than 3 movies as they won’t be adding any useful insights to the data. Finally, we train our SVD (Singular Value Decomposition) model
2.	Using Cosine Similarity Matrix: 
This is content based approach. Again, we start by importing the necessary libraries and the CSVs and start with the data preprocessing. In this approach we list important keywords related to a movie against it. These keywords are the defining keywords for the movie based on which the similarity will be calculated with the other movies. Once this is done, we calculate the similarity matrix between all the movies and then use this matrix to fetch movies with 70% similarity to other movies. And these movies can be recommended to the user if he liked the 1st movie.
