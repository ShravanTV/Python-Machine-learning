This code is an implementation of the research paper <b>"Experiments with Random Projections for Machine Learning"</b>

The data in the Real world is not clean and also contains huge information to be analyzed. We use Machine learning models to predict/ take decisions and for this purpose initially we would collect as many features as possible so that the Machine Leaning models can be trained and accurate results are obtained. However, the performance of model will be decreased if the number of elements increases also the sample density decreases and may lead to overfitting. Dimensionality Reduction plays a useful role in reducing the above problems and reduces the algorithm execution time, reduces memory consumption, eliminate irrelevant features. Also, I strongly believe that Data preprocessing is required to obtain accurate results from the Machine learning models. If we concentrate much on data preprocessing then our model accuracies increase. Hence, I have selected this paper where the author is performing various experiments on when to use Random Projections and when to use PCA with different number of features.

The author in the paper has used 5 different datasets for performing the experiments on PCA and Random Projections, but I have considered only 2 datasets (ads and spam base) which are low instance-low attribute(ads) and high instance-high attribute data(spam). And performed PCA and Random Projections of the data and passed to Decision Tree, KNN (5 neighbors) and SVM models respectively and plotted graph as below and found certain similarities and differences in the output when compared to the author in the above-mentioned paper.

Experimental Methodology: 
1.	Each dataset is split into Training and test dataset
2.	Data needs to be normalized 
3.	For each split of dimensions perform PCA on training data and project both training and test data.
4.	Create Random Projection and project both training and test data.
5.	Pass this data to the models discussed in Technique section and train the models
6.	Apply to test sets and note the performances.
The dimensions of the dataset need to be reduced based on the available of features in the data. For the dataset with 1500 features the dimensions were split like 50,100,150,200,250,300,350,400 and noted the performance of models at each of these splits.

Results:
Nearest neighbor method was less affected with reduction of dimensions using PCA and Random Projections. Performance of model was reduced when compared to SVM and Decision tree models. For dataset with low instances- low attribute and high instance-high attribute, this actually increased the performance compared to the baseline accuracy (without Dimensionality Reduction). And Random Projection performed well with Nearest neighbor.
SVM- initially when PCA and RP were used it performed worse than the baseline accuracy, but when the number of dimensions increases the performance was getting increased gradually. In case of low instance-low attribute and high instance-high attribute datasets, PCA performed well compared to Random Projections.
Decision tree- This model performed well with low dimensional PCA approach and its performance deteriorates and later doesn’t improved. It doesn’t feel well with reduction of dimensions and is quite sensitive to noise. Random projection and decision trees are not a good combination and performance is very low with low dimensions and it doesn’t improve much.

References:
Fradkin, D., & Madigan, D. (2003, August). Experiments with random projections for machine learning. In Proceedings of the ninth ACM SIGKDD international conference on Knowledge discovery and data mining (pp. 517-522).
ŷhat: Python Sparse Random Projections. (n.d.). Retrieved from http://blog.yhat.com/posts/sparse-random-projections.html
Cventr - Pca and Detection. (n.d.). Retrieved from https://www.kaggle.com/cventr/pca-and-detection
