## Breast cancer analysis problem

I created a project focused on finding decision making model for predicting of breast cancer, with use of KNearestNeighbors method.
Learning was made on Wisconsin dataset. Proces resulted in 0.967 accuracy.

### Dataset information

###### Name: Breast Cancer Wisconsin (Original) Data Set 

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

![](https://github.com/KrzysiekJa/knn-on-health/blob/master/knn%20on%20breast%20cancer/decission_tree.png)

### K-NearestNeighbors

Results showed on plot below:

![](https://github.com/KrzysiekJa/knn-on-health/blob/master/knn%20on%20breast%20cancer/knn_plot.png "Plot KNN")

Extra plot showing how important are particular factors:
<p align="center"><img src="https://github.com/KrzysiekJa/knn-on-health/blob/master/knn%20on%20breast%20cancer/pca_components.png" width="750" height="700" /></p>

![](https://github.com/KrzysiekJa/knn-on-health/blob/master/knn%20on%20breast%20cancer/confusion_matrix.png)

### Perceptron

![](https://github.com/KrzysiekJa/knn-on-health/blob/master/perceptron/learning_rate.png)

![](https://github.com/KrzysiekJa/knn-on-health/blob/master/perceptron/decision_boundary.png)

![](https://github.com/KrzysiekJa/knn-on-health/blob/master/perceptron/confusion_matrix.png)
