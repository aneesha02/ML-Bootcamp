Algorithm Implemented:Logistic Regression
Class:LogReg
Methods:
 1)__init__():
 parameters:
 alph:learning rate
 maxitr:maximum number of iteration for training

 method description:constructor to initialize the variables of the class-alph,maxitr,thres
 
 2)convert():
  parameters:
  y-label values
  rowcnt-number of rows in data
  nclass-number of classes 
  method description:
  This method is used for conversion of label values for the objective of multiclass logistic regression

 3)predict()
  parameters:
   x-features of the test data
  method description:to calculate the predicted values of labels based on the test data using the weights and independent variables 
  and applying the sigmoid function

 4)fitting():
 parameters:x,y1,colcnt,nclass
 method description:to train the model. Starting with initial weights for each class of multiclass logistic regression, it calculates 
    the initial predicted values of labels and corresponding error for all the classes. 
    Gradient descent is performed over 'maxitr' number of iterations to find the new weights for each class.
    We fix the optimum value of 'maxitr' by running the model by various trials.
    We also assume the learning rate 'alph' at optimum level
 5)accuracy():
  parameters:
  y:label values after conversion\
  ypred:predicted values of y
  method description:This method is used to test the accuracy of the predicted result.

 
Training and Testing:
 The training data available contains 20000 rows and 785 columns (labels and 784 features). The program reads the training data as a csv file and 
 separates the data for label and features. The features data is normalized to bring it in the range of 0-1. The labels are transformed via one hot encoding
 (i.e, 0-1 principle). Over maxitr number of iterations, we have initiated the weights with random values, then at every iteration we have calculated the 
 MSE and we perform gradient descent to find the improved values of the weights.
 The testing data available contains 10000 rows and 785 columns (labels and 784 features). The program reads the test data as a csv file and separates
 the label and features. The feature data is normalized to bring it in the range of 0-1.The labels are transformed via one hot encoding (i.e, 0-1 principle)
 We use the final weights obtained after training the model to predict the values of y.

The model uses sigmoid function to predict the label which returns a value between 0-1. If the sigmoid value>=0.5 we will consider it as 1 otherwise 0.
These predicted values will be compared with the converted label values. We count the total number of matches and divide it by number of rows. 
The accuracy has been found to be 46.37% taking alph=0.0000001 and maxitr= 1000. Due to limitations of the resources of the machine, the model
 could not be improved to the fullest extent.
 



