### K Nearest Neighbors

KNN or k nearest neighbors is another modeling technique we can use along with linear and logistic regression in supervised learning models.  KNN can be used to predict either continuous or categorical data.  It makes predictions by testing each input point against every point in your test data.  It then determines the k-nearest, or most similar neighbors from the training data and makes a prediction based on the mean (in the case of continuous data) or most represented category (for discrete data).  The distance is determined one of three ways: Euclidean distance, Manhattan distance, or the Minkowski distance.  In the fit stage of KNN modeling, the model simply takes in the data and stores it, all the calculation happens in the predict method. To save computing cost, the predict method will often call multiple helpers. 