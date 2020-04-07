# Recommendation Systems
There are two main types of recommender systems: content-based and collaborative-filtering.  These differ in the sense of how they measure similarity in order to determine predictions.  In a content-based strategy, the system will recommend items to you that are similar to other items you've bought/used/seen before.  In a collaborative-filtering strategy, the system will look at similarity between your user profile and other user profiles, and try to recommend items that similar users have liked.  There are also what's called memory-based, and model-based recommenders.  These have to do with how the model uses it's data to make predictions.  Memory-based recommenders will use existing ratings to compute user->user or item->item similarity, while model-based recommenders use ML techniques to make predictions based on data it was trained on.

In all of these situations, you will likely start with a matrix (R) of users and products showing which users have used or rated which products.  It is recommended to store this data as a sparse matrix because many users will not have used most products.  Next you would factor this matrix R into a user matrix P and an item matrix Q^T (R=PQ^T).  This type of factoring results in the isolation of latent features, or the features where the rows of P match the columns of Q^T.  This is a method of dimensionality reduction, but we could also use SVD or Alterating Least Squares.
### Content based
- determine which row (item) to recommend to user based on item(s) they like
- use cosine of row vectors to determine likeness of two items 
  - identical vectors would have a cosine 1, orthogonal vectors would have cosine 0 (so the highest cosine value will be the most-like item)
### Collaborative Filtering
- recommend items to user based on what similar users have enjoyed
- can use cosine similarity of row (user) vector to calculate similarity to other users
- could also use Pearson Correlation