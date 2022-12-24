# K Nearest neighbors

- The KNN is a non parametric ML algorithm which can be used in both regression and classification. In this case we are using it to classify(Iris and Digits) classes.
- Implementation -
-- The utils conains two functions euclidean distance and manhattan distance between two numpy arrays.
--The euclidean distance is the l2 norm of the two vectors of d features while the manhattan distance is the l1 norm.

- The fit function in knn python file just initializes the class variables _X and _y to the train data and train labels as there is no "parameter learning" in knn.
- The get_weight_metric returns 1 if the weights are uniform as we won't assign weights to the neighbors in this case. If the weight is distance then we will weight the neighbors which will be inversely proportional to the distance between the test sample and the neighboring datapoint. To avoid divide by 0 exception, I am returning 1 if the distance is 0 else i'll return the inverse of the distance.
- In the predict function, we will iterate over all the test points, calculate the distance between the points. Then we need to sort the distance in order to get the k nearest data points'(neighbors) labels.
- For the k nearest data points, we will find the mode of the k labels and append it to the predictions list.