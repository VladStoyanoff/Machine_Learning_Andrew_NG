![Anomaly_Detection_1](https://github.com/VladStoyanoff/Stanford_Machine_Learning_Coursera/blob/main/Week_9/In-Video_Questions/Anomaly_Detection_1.png)

Option 1: If epsilon marks the boundary where the algorithm distinguishes anomalies from non-anomalies, and when the density estimation p(x) =< epsilon marks it as an anomaly, then the density estimation p(x) > epsilon is a non-anomaly. In this problem, the algorithm is flagging too many examples as anomalies, thus, increasing the parameter epsilon, will widen the boundary, resulting in even more flagging of anomalies as non-anomalies. Incorrect.

Option 2: Following the logic on option 1, this is the correct answer. Decreasing the parameter epsilon will tighten the boundary and make sure that any sample outside this boundary get flagged as an anomaly. Correct.

![Anomaly_Detection_2](https://github.com/VladStoyanoff/Stanford_Machine_Learning_Coursera/blob/main/Week_9/In-Video_Questions/Anomaly_Detection_2.png)

Option 1: On the plot, it is clearly seen that the mean parameter mu lays between -4 and -2, which is -3. Assuming that our data's probability distribution is Gaussian with mean mu and variance sigma^2, the formula for calculating the probability of x, includes computing the result from SUBTRACTING the mean value from all the samples' values. -(-3) = + , so option 1 and 2 fall out. Incorrect.

Option 2: Following the logic on option 1, this is incorrect as well.

Option 3: Sigma is the width a.k.a the standart deviation of the gaussian distribution. 2 * 4 in the denominator means that the sd = 2, because the formula notes that we should take sigma and take it to the power of 2. On the plot we see that a value of sigma = 2, is very plausible (and much more likely, than 2 * 1/2, which is the next answer). In practice, sigma can be precisely measured by calculating the average squared difference between all the values minus the mean mu, but here the values are not given, so one must rely on eyeballing it. Correct.

Option 4: Following the logic on option 3, this is incorrect.

![Anomaly_Detection_3](https://github.com/VladStoyanoff/Stanford_Machine_Learning_Coursera/blob/main/Week_9/In-Video_Questions/Anomaly_Detection_3.png)

Option 1: To calculate the squared standart deviation sigma(j)^2, one would first need to calulcate the mean(j), and use it while calculating the squared difference between the data minus the mean. Keeping true to this, option 1 and 3 fall out, because they're not calculating the squared difference with mu(j). Incorrect

Option 2: The mean is calculated by taking the average of the sum of all the samples in the dataset, neing considered (j). But not the sum of all the samples squared. Incorrect.

Option 3: Following the logic on option 1, this is incorrect as well. Incorrect.

Option 4: Following the logic on option 3, this is the correct answer. Correct.

![Anomaly_Detection_4](https://github.com/VladStoyanoff/Stanford_Machine_Learning_Coursera/blob/main/Week_9/In-Video_Questions/Anomaly_Detection_4.png)

Option 1: For problems where the positive class << negative class (for example less or equal than 1% of the total data), classification accuracy is not a good idea to measure the algorithm's performance, because even if we predict that all the examples are non-anomalous then we would have 99% accuracy, which does not really do the job of telling us the performance of this algorithm (the algortihm didn't distinguish even one anomaly, which should give us a very big warning). Incorrect.

Option 2: Splitting the data on a training set containing 60% of the data filled with all the non-anomalous samples (on which to evaluate the gaussian distribution and figure out where the boundary, denoted by the parameter epsilon should be), cross-validation set that contains 20% of the data with non-anomalous samples and 50% of the anomalous samples and a test set with the rest 20% of the non-anomalous samples and the rest 50% of the anomalous samples, would give us the best architecture for measuring the performance. The CV and test sets do have binary labels, to be able to train and distinguish the anomalous from non-anomalous. Incorrect.

Option 3: Following the logic of option 1, this is the correct answer. Correct.

Option 4: This doesn't make much sense, because CV set and test set are identical when it comes to proportion of the total data. They serve different functions, but within the same architecture of measuring accuracy, described in option 2. Incorrect.

![Anomaly_Detection_5](https://github.com/VladStoyanoff/Stanford_Machine_Learning_Coursera/blob/main/Week_9/In-Video_Questions/Anomaly_Detection_5.png)

Option 1: Anomaly detection algorithm should be good at distinguishing anomalous examples from a very small training dataset of anomalous examples in the dataset, and also be able to distinguish anomalous samples it has never seen before in the training set. On the other hand, supervised learning algorithms would be working with huge number of positive and negative examples, huge enough so that the algorithm has a good sense of what positive examples will look like, increasing the probability that future positive examples will be as similar as possible to the ones in the training set. Hence, this option would fall under the category of anomaly detection algorithm. Correct.

Option 2: Following the logic of option 1, this is inccorect. Incorrect.

Option 3: Following the logic of option 1, this is inccorect. Correct.

Option 4: Following the logic of option 1, this is inccorect. Incorrect.

![Anomaly_Detection_6](https://github.com/VladStoyanoff/Stanford_Machine_Learning_Coursera/blob/main/Week_9/In-Video_Questions/Anomaly_Detection_6.png)

Option 1: In the case that algorithm is outputting a large value for both the anomalous and non-anomalous examples, then this means that the Gaussian distribution does not distinguish anomalous from non-anomalous examples (even if one updates the boundary, then that would still not help, because then both the types of data will just go the other extreme - if at the start they were both non-anomalous, then after changing epsilon, they would be classified as both anomalous). This could be fixed by adding new features to the dataset, or using a more complex method - Multivariate Gaussian. This being said, using fewer features will not help. Incorrect.

Option 2: Following the logic of option 1, then this is the correct answer. Correct.

Option 3: Getting a larger dataset, while not fixing the internal structure of the features or the gaussian variables, will not help, because then one would just have even more wrongly classified examples. Incorrect.

Option 4: Following the logic of option 1, this is incorrect. Incorrect.

![Anomaly_Detection_7](https://github.com/VladStoyanoff/Stanford_Machine_Learning_Coursera/blob/main/Week_9/In-Video_Questions/Anomaly_Detection_7.png)

Option 1: Looking at the plots, one can conclude that they capture x1 and x2 in a negative correlation region (meaning that x1 doesnt scale linearly with x2, but it's the opposite happening). This is only possible if the off-diagonal entries of the covariance matrix, capital sigma, are negative. Thus, option 1 and 2 are excluded. Incorrect.

Option 2: Following the logic on option 1, this is also incorrect. Incorrect.

Option 3: From the plot, one can clearly see that the mean is centered at [1, 0] with x1 at 1 and x2 at 0. So this is the correct answer. Correct

Option 4: Following the logic on option 3, this is the incorrect answer. Incorrect.

![Anomaly_Detection_8](https://github.com/VladStoyanoff/Stanford_Machine_Learning_Coursera/blob/main/Week_9/In-Video_Questions/Anomaly_Detection_8.png)

Option 1: Theoretically, the only difference between the original Gaussian and the multivariate gaussian is the values at the off diagonals. At the original, it's all zeros, while at the multivariate the can take any value, giving the developer more flexibility in designing the right density estimation model p(x). Correct.

Option 2: The covariance matrix would be non-invertalbe if m =< n, and for optimal quality of the result, it should be m =< 10n. Incorrect.

Option 3: Thanks to the magic of covariance matrices and matrix algebra, Multivariate Gaussian density estiomation model p(x) automatically captures correlations between features, whereas one has to manually set them when using the original density estimation model p(x). Correct.

Option 4: The reason why the multiavariate gaussian density estimaton model p(x) is computationally expensive is because, computing the covariance matrix, involves transposing, often huge, matrix - the differnce between all the samples in the data and the mean of the gaussian. Correct.

![Recommender_Systems_1](https://github.com/VladStoyanoff/Stanford_Machine_Learning_Coursera/blob/main/Week_9/In-Video_Questions/Recommender_Systems_1.png)

Option 1: This option describes that user1 has not given a rating on movie 2 which is correct, although the rating isn't 1. It should be undefined. Incorrect.

Option 2: This option describes that user1 has given a rating on movie 2 which is 1. We see that’s not the case though, because he has not given any rating. Incorrect.

Option 3: This option describes that user1 has not given a rating on movie 2. And the rating value is undefined, which is the case. Correct.

Option 4: This option describes that user1 has given a rating on movie 2, but the rating is undefined, which is illogical. Incorrect.

![Recommender_Systems_2](https://github.com/VladStoyanoff/Stanford_Machine_Learning_Coursera/blob/main/Week_9/In-Video_Questions/Recommender_Systems_2.png)

Option 1: The formula for calculating a rating on a movie, based on the features and the theta parameters is as follows: theta’ * x. Substituting the values here in the formula, for movie 1, would give the rating of 4.5, which is not the case for Carol (theta(3)). Incorrect.

Option 2: Substituting the values here in the formula theta’ * x, for movie 4, would give the rating of 1 for Carol, which is not the case. Incorrect.

Option 3: Substituting the values here in the formula theta’ * x, for movie 1, would give the rating of 1 for Carol, which is not the case. Incorrect.

Option 4: Substituting the values here in the formula theta’ * x, for movie 1, would give the rating of 0 for Carol, which is the case, so one should test with all the other movies. As it turns out, the rating is accurate for each movie, so this is the correct answer. Correct.

![Recommender_Systems_3_1](https://github.com/VladStoyanoff/Stanford_Machine_Learning_Coursera/blob/main/Week_9/In-Video_Questions/Recommender_Systems_3_1.png)

Option 1: The formula for calculating a rating on a movie, based on the features and the theta parameters is as follows: theta’ * x. Substituting the values here in the formula with x(1) being 0.5 would give the rating of 0 for the first film, 1.5 for the second, and 3 for the third. Correct.

Option 2: Substituting the values here in the formula with x(1) being 0.5 would give the rating of 0 for the first film, 3 for the second, and 5 for the third. Incorrect.

Option 3: Substituting the values here in the formula with x(1) being 2 would give the rating of 0 for the first film, 6 for the second, and 10 for the third. Incorrect.

Option 4: As one can see, the ratings change when changing the value of feature x(1). Incorrect.

![Recommender_Systems_3_2](https://github.com/VladStoyanoff/Stanford_Machine_Learning_Coursera/blob/main/Week_9/In-Video_Questions/Recommender_Systems_3_2.png)

Option 1: When computing the gradient in a gradient descent algorithm, one would want to subtract the regularized cost, for i != 0. One would want to subtract it, so that the lowe the cost is, the smaller the steps the algorithm takes, to optimize the gradient. This option here adds the cost, so this is incorrect.

Option 2: Following the logic on option 1, this would be correct only if i = 0, which is not the case, as described in the question. Incorrect. 

Option 3: Following the logic on option 1, this would be incorrect because it adds the cost, even though it’s regularized.

Option 4: Following the logic on option 1, this would be the correct answer because it subtracts the regularized cost. One wouldn’t want to regularize for i = 0, because that’s a row (or a column, if transposed) full of ones, so regularizing would be pointless. Correct.

![Recommender_Systems_4](https://github.com/VladStoyanoff/Stanford_Machine_Learning_Coursera/blob/main/Week_9/In-Video_Questions/Recommender_Systems_4.png)

Option 1: Initializing theta and x to random values when implementing a collaborative filter algorithm, over initializing to all zeros, would give the advantage that the algorithm could start optimizing towards the lowest cost. If it were all zeros, then no movie would be preferred over any else, and there wouldn’t be a starting point from which to optimize. Incorrect.

Option 2: Random initialization is not always necessary. For example, one could initialize theta parameters to all zeros, if doing a linear regression, because that wouldn’t have computational errors when starting to optimize for cost. Incorrect.

Option 3: The features and parameters do not have any special correlation among each other, when it comes to values. In other words there’s no problem if both are the same. Correct.

Option 4: Just as for neural networks, when the features are different from the start, then that would ensure that a proper cost optimization will start taking place. Correct.

![Recommender_Systems_5](https://github.com/VladStoyanoff/Stanford_Machine_Learning_Coursera/blob/main/Week_9/In-Video_Questions/Recommender_Systems_5.png)

Option 1: Matrix algebra. Incorrect.

Option 2: Matrix algebra. Incorrect.

Option 3: Matrix algebra. Correct.

Option 4: Matrix algebra. Incorrect.

![Recommender_Systems_6](https://github.com/VladStoyanoff/Stanford_Machine_Learning_Coursera/blob/main/Week_9/In-Video_Questions/Recommender_Systems_6.png)

Option 1: Feature scaling works when the value being outputted is both real-valued and continuous. Incorrect.

Option 2: The movie ratings are on the same scale, so scaling the features is not needed. Correct. 

Option 3: Subtracting the mean is a completely different computation than dividing by the standard deviation or the range (max - min). One would want to do both in a single computation to perform the full mean normalization. Incorrect. 

Option 4: Any parameters which aren’t on the same scale and aren’t scaled properly, would hinder the performance of the algorithm. Incorrect.


