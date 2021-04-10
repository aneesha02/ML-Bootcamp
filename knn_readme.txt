Algorithm Implemented:K Nearest neighbours
Class Name:KNN
Methods:
 1)__init__():
 parameters:
 x:the feature data
 y: the label values
 k:parameter to classify the test data points i.e the number of nearest neighbours
 method description:constructor to initialize the variables of the class-x,y,k.

 2)euc_dist():
 parameters:
 A:first vector
 B:second vector
 This method performs calculates the euclidean distance between 2 vectors.

 3)predict():
 parameters:x
 method description:
    This method predicts the y values that is,the labels of the test dataset.This is done by calculating the distances of each test data point 
    from each row of the training data set,sorting and obtaining the k nearest neighbours of each test data and the most frequently occurring 
    class is found out. The test point is given the label value of the most frequently occurring class among the k nearest neighbours.

 6)accuracy()
  parameters:
  y-label values
  ypred-predicted values of y
  method description: This method finds the accuracy of the model by counting the number of matches of label values.

Training and Testing:
 The training data available contains 20000 rows and 785 columns (labels and 784 features). The program reads the training data as a csv file and 
 separates the data for label and features. The features data is normalized to bring it in the range of 0-1. 
 The testing data available contains 10000 rows and 785 columns (labels and 784 features). The program reads the test data as a csv file and separates
 the label and features. The feature data is normalized to bring it in the range of 0-1. The distance of each point of the test data is calculated wrt all
 the rows of the training data. The k nearest neighbours are found for each record of test data and the label of the most frequently occurring class
 among them is given to the test data point.
 The model calculates the accuracy by adding the number of matches of the predicted values and the label values and dividing by the number of rows.
 The accuracy has been found to be 96.05% taking k as 3. Due to limitations of the resources of the machine, the model could not be improved to 
 the fullest extent.
 

 



