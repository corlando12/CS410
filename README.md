# CourseProject

Intelligent Dining Decision Assistant 

Application Overview

Choosing a restaurant can be a complex decision-making process, made even more challenging due to the vast amount of online information available. This application intends to make the process more manageable and intelligent. The application incorporates concepts such as semantic analysis, relevance, probabilistic ranking, and collaborative filtering to improve the accuracy and relevance of restaurant recommendations and insights. A user is simply able to launch the program and input their desired food of choice along with a location. In return the application will produce a resultant restaurant that provides the food inputted by the user.

Datasets and Algorithms

Datasets: Used publicly available restaurant APIs for obtaining detailed information, reviews, and ratings.

Algorithms: Our current algorithm for relevance (R) is R = (Number of unique query terms in document / Number of query terms) * 100

Techniques and Concepts from the Course:

Semantic Analysis: Understanding user queries and reviews to generate relevant restaurant recommendations.

Bag of Words Representation & Vector Space Model: For text representation and understanding the context of user preferences and restaurant information.

Probabilistic Relevance Ranking for Text Retrieval: Ensuring that the most suitable restaurant recommendations are shown to the users.

Collaborative Filtering: Using user-item interactions for personalizing restaurant recommendations.

Evaluation Metrics (Precision, Recall, MAP): To evaluate the performance and relevance of our recommendations.

Application Outcome:

Every time a user enters a query and clicks the “Find Restaurants” button, the system will generate a Python list that consists of a collection of restaurants that are relevant to the query. The generation of this list is made possible by an inverted index. Next to each restaurant in the results, the city, state, and a relevance score will be displayed. The relevance score is calculated based on the following formula:

Relevance = (Number of unique query terms in document / Number of query terms) * 100

The only exception to the relevance formula is when certain stop words are entered, such as “and” and “the”. Stop words are ignored during the relevance calculation.

In this scenario, each restaurant name displayed in the results represents a document. Each document is a text file that contains the name of the restaurant on the first line. The city and state are included on the second line. The next lines contain information about the restaurant, which is mostly the food items offered by the restaurant. When the program is not running, more restaurant text files can be added to the main folder and the program will incorporate these files into the inverted index when it starts.

There is no limit to the number of queries a user can enter. While the program is actively running, the user can continually keep entering queries and all results will be maintained. Each new result list will be displayed at the top of the previous results. If the collection of result lists exceeds the window height, the user will be able to scroll down to the bottom of the results.

The user has the option to filter the results by specifying their location with a city and state name. If the user decides to enter their location, the program will still return the original results, except the results that correspond to a different location will be replaced with the text “Location Filter Applied”.

The location filter will only allow the user to see the results that correspond to the specified location. The user will still be able to view the count of the other search results for different locations, which could encourage the user to try their query with a different location or remove the entire filter. To be the most effective, the user should specify their location in the query and the location filter.
