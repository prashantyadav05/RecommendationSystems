# Recommendation Systems
Systems or techniques that recommend or suggest a particular product, service, or entity.
* The prediction problem
Aims to predict the missing values using all the information it has at its disposal.
* The ranking problem
## Types of recommender systems
### Collaborative filtering 
leverages the power of community to provide recommendations.
#### User-based filtering
The main idea behind user-based filtering is that if we are able to find users that have bought and liked similar items in the past, they are more likely to buy similar items in the future too. Amazon's **Customers who bought this item also bought** is an example of this filter. 
#### Item-based filtering
If a group of people have rated two items similarly, then the two items must be similar. Therefore, if a person likes one particular item, they're likely to be interested in the other item too. Amazon's **You recently viewd items & featured recommendations** is an example of this filter.
##### Shortcomings
One of the biggest prerequisites of a collaborative filtering system is the availability of data of past activity. Amazon is able to leverage collaborative filters so well because it has access to data concerning millions of purchases from millions of users. Therefore, collaborative filters suffer from what we call the cold start problem. Imagine you have started an e-commerce website – to build a good collaborative filtering system, you need data on a large number of purchases from a large number of users. However, you don't have either, and it's therefore difficult to build such a system from the start.

### Content-based systems
Provide recommendations based on a user profile and metadata it has on particular items. Netflix is an excellent example of the aforementioned system. The first time you sign in to Netflix, it doesn't know what your likes and dislikes are, so it is not in a position to find users similar to you and recommend the movies and shows they have liked. 

since content-based systems don't leverage the power of the community, they often come up with results that are not as impressive or relevant as the ones offered by collaborative filters. In other words, content-based systems usually provide recommendations that are obvious. There is little novelty in a **Lord of the Rings** recommendation if **Harry Potter** is your favorite movie
### Knowledge-based recommenders
In such cases, you build a system that asks for certain specifics and preferences and then provides recommendations that satisfy those aforementioned conditions. In the real estate example, for instance, you could ask the user about their requirements for a house, such as its locality, their budget, the number of rooms, and the number of storeys, and so on. Based on this information, you can then recommend properties that will satisfy all of the above conditions.
### Hybrid recommenders
hybrid recommenders are robust systems that combine various types of recommender models. Hybrid systems try to nullify the disadvantage of one model against an advantage of another. Let's consider the Netflix example again. When you sign in for the first time, Netflix overcomes the cold start problem of collaborative filters by using a content-based recommender, and, as you gradually start watching and rating movies, it brings its collaborative filtering mechanism into play. This is far more successful, so most practical
recommender systems are hybrid in nature.

## The simple recommender
1. Choose a metric (or score) to rate the movies on
2. Decide on the prerequisites for the movie to be featured on the chart
3. Calculate the score for every movie that satisfies the conditions
4. Output the list of movies in decreasing order of their scores.
### The metric
The metric is the numeric quantity based on which we rank movies. A movie is considered to be better than another movie if it has a higher metric score than the other movie. It is very important that we have a robust and a reliable metric to build our chart upon to
ensure a good quality of recommendations. The choice of a metric is arbitrary. One of the simplest metrics that can be used is the movie
rating. However, this suffers from a variety of disadvantages. In the first place, the movie rating does not take the popularity of a movie into consideration. Therefore, a movie rated 9 by 100,000 users will be placed below a movie rated 9.5 by 100 users.
This is not desirable as it is highly likely that a movie watched and rated only by 100 people caters to a very specific niche and may not appeal as much to the average person as the former.
## The knowledge-based recommender
1. Ask the user for the genres of movies he/she is looking for.
2. Ask the user for the duration.
3. Ask the user for the timeline of the movies recommended.
4. Using the information collected, recommend movies to the user that have a high weighted rating (according to the IMDB formula) and that satisfy the preceding conditions.
## Building Content-Based Recommenders
