# Recommendation_engine
Recommendation systems using python
Recommendatin Engine: A recommendation engine filters the data using different algorithms and recommends the most relevant items to users. It first captures the past behavior of a customer and based on that, recommends products which the users might be likely to buy.

              Recommendation engines basically are data filtering tools that make use of algorithms and data to recommend the most relevant items to a particular user.Or in simple terms, they are nothing but an automated form of a “shop counter guy”. You ask him for a product. Not only he shows that product, but also the related ones which you could buy. They are well trained in cross-selling and upselling.With the growing amount of information on the internet and with a significant rise in the number of users, it is becoming important for companies to search, map and provide them with the relevant chunk of information according to their preferences and tastes.     

         We can recommend items to a user which are most popular among all the users
         We can divide the users into multiple segments based on their preferences (user features) and recommend items to them based on the segment they belong to 
        Both of the above methods have their drawbacks. In the first case, the most popular items would be the same for each user so everybody will see the same recommendations. While in the second case, as the number of users increases, the number of features will also increase. So classifying the users into various segments will be a very difficult task.

How a recommendation engine works by going through the following steps.

Data collection:This is the first and most crucial step for building a recommendation engine. The data can be collected by two means: explicitly and implicitly. Explicit data is information that is provided intentionally, i.e. input from the users such as book ratings. Implicit data is information that is not provided intentionally but gathered from available data streams like search history, clicks, order history, etc.
Data storage: The amount of data dictates how good the recommendations of the model can get. For example, in a book recommendation system, the more ratings users give to books, the better the recommendations get for other users. The type of data plays an important role in deciding the type of storage that has to be used. This type of storage could include a standard SQL database, a NoSQL database or some kind of object storage.
Filtering the data: After collecting and storing the data, we have to filter it so as to extract the relevant information required to make the final recommendations.
There are various algorithms that help us make the filtering process easier. Those are 
popularity based recommendation
content based filtering recommendation
colloborative filtering recommendation
hybrid based recommendation
1.Content based filtering: content based filtering recommends products which are similar to the ones that a user has liked in the past. For example, if a person has liked the book “”, then this algorithm will recommend books that fall under the same features like authors,metadata.

      we save all the information related to each user in a vector form. This vector contains the past behavior of the user, i.e. the books liked/disliked by the user and the ratings given by them. This vector is known as the profile vector. All the information related to book is stored in another vector called the item vector. Item vector contains the details of each book, like genre, author, categeory etc.

The content-based filtering algorithm finds the cosine of the angle between the profile vector and item vector, i.e. cosine similarity.

cosine similarity: Suppose A is the profile vector and B is the item vector, then the similarity between them can be calculated as:

           sim(A,B) =  cos(θ) = A.B/|A||B| 

Based on the cosine value, which ranges between -1 to 1, the books are arranged in descending order and one of the two below approaches is used for recommendations:

Top-n approach: where the top n books are recommended (Here n can be decided by the business)
Rating scale approach: Where a threshold is set and all the Books above that threshold are recommended




2.Collaborative filtering: The collaborative filtering algorithm uses “User Behavior” for recommending items. This is one of the most commonly used algorithms in the industry as it is not dependent on any additional information.



3.Hybrid filtering: Most recommender systems now use a hybrid approach, combining colloborative filtering and content-based filtering.


