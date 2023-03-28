## Breast cancer analysis problem

Created project is focused on finding decision making model (classifier) for predicting whether breast cancer is benign or malignant, with use of KNearestNeighbors method from scikit-learn package and own design perceptron. 
Learning was made on Wisconsin dataset. Proces resulted in obtaining a model with predicting ability higher than 0.99 accuracy.

### Dataset information

###### Name: Breast Cancer Wisconsin (Original) Data Set 

[UCI Breast Cancer Wisconsin Dataset](https://archive.ics.uci.edu/ml/datasets/breast+cancer+wisconsin+%28original%29)

Samples arrive periodically as Dr. Wolberg reports his clinical cases. The database therefore reflects this chronological grouping of the data. This grouping information appears immediately below, having been removed from the data itself: 

Group 1: 367 instances (January 1989)  
Group 2: 70 instances (October 1989)  
Group 3: 31 instances (February 1990)  
Group 4: 17 instances (April 1990)  
Group 5: 48 instances (August 1990)  
Group 6: 49 instances (Updated January 1991)  
Group 7: 31 instances (June 1991)  
Group 8: 86 instances (November 1991)  

----------------------------------------- 
Total: 699 points (as of the donated datbase on 15 July 1992) 

Note that the results summarized above in Past Usage refer to a dataset of size 369, while Group 1 has only 367 instances. This is because it originally contained 369 instances; 2 were removed. The following statements summarizes changes to the original Group 1's set of data: 

Attribute Information:

1. Sample code number: id number 
2. Clump Thickness: 1 - 10 
3. Uniformity of Cell Size: 1 - 10 
4. Uniformity of Cell Shape: 1 - 10 
5. Marginal Adhesion: 1 - 10 
6. Single Epithelial Cell Size: 1 - 10 
7. Bare Nuclei: 1 - 10 
8. Bland Chromatin: 1 - 10 
9. Normal Nucleoli: 1 - 10 
10. Mitoses: 1 - 10 
11. Class/Status: (2 for benign, 4 for malignant)

### Initial insights

At the beginning, the data was analyzed in terms of possible recognition of potential attributes and their associated values that could be used to carry out an effective classification decision-making process.

![](https://github.com/KrzysiekJa/knn-on-health/blob/master/knn%20on%20breast%20cancer/decission_tree.png)

As we can see, for the classification decision-making process carried out on the data from the set, the most important is the Uniformity of Cell Size feature. Other important ones are: Bare Nuclei, Uniformity of Cell Shape and Clump Thickness.  
E.g. as we can find that cell with Uniformity of Cell Size <= 2.50, Bare Nuclei <= 5.50, Clump Thickness <= 6.50 we can classify as benign; and cell with Uniformity of Cell Size > 2.50 and Uniformity of Cell Shape feature > 2.50 we can classify as malignant. 

### K-NearestNeighbors

The usage of the K-NearestNeighbors algorithm brought the following classification results for the problem, which after transformation into 2D form (using PCA: 9 -> 2) are visible in the graph below.  
To obtain a highly accurate classifier, the data was augmented using the BorderlineSMOTE algorithm, algorithm that performs data augmentation by creating synthetic data points based on the original data points.

![](https://github.com/KrzysiekJa/knn-on-health/blob/master/knn%20on%20breast%20cancer/knn_plot.png "Plot KNN")

Principal axes in feature space are representing the directions of maximum variance in the data. Plot below show how important are particular factors for performed/obtained PCA dimensionality reduction:  
<p align="center"><img src="https://github.com/KrzysiekJa/knn-on-health/blob/master/knn%20on%20breast%20cancer/pca_components.png" width="750" height="700" /></p>

The confusion matrix below shows the results of the classifier testing:
![](https://github.com/KrzysiekJa/knn-on-health/blob/master/knn%20on%20breast%20cancer/confusion_matrix.png)

### Perceptron

![](https://github.com/KrzysiekJa/knn-on-health/blob/master/perceptron/learning_rate.png)

![](https://github.com/KrzysiekJa/knn-on-health/blob/master/perceptron/decision_boundary.png)

![](https://github.com/KrzysiekJa/knn-on-health/blob/master/perceptron/confusion_matrix.png)
