# Building a Recommender System

Ever wondered how Spotify, Amazon, and Netflix generate recommendations for their users? In this notebook, we will build our own recommendation system using the MovieLens dataset (100k ratings) and consider various aspects such as user-similarity, movie popularity, and recency to suggest the best movies possible to the user.

## Outline

This project is broken down into 6 steps:

1. Importing the dependencies
2. Loading the data
3. Building custom tables and data exploration
4. User-based collaborative filtering and recommendations based on recency
5. Evaluating the model
6. Model improvements and putting it all together

## Step 0: Understanding the Model

### User-Based Collaborative Filtering

Firstly, let's understand how User-based collaborative filtering works.User-based collaborative filtering makes recommendations based on user-product interactions in the past. The assumption behind the algorithm is that similar users like similar products.

The user-based collaborative filtering algorithm usually has the following steps:

- Find similar users based on interactions with common items.
- Identify the items rated highly by similar users but have not been exposed to the active user of interest.
- Calculate the weighted average score for each item.
- Rank items based on the score and pick the top n items to recommend.

### Hybrid Model

We're not stopping there! Our system's got a little extra kick with a hybrid model. If we don't know much about a user, we'll throw in some popular and recent movies in their favorite genres to keep things interesting
