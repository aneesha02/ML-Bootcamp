Algorithm Implemented:Linear Regression
Class Name:LinReg
Methods:
 1)__init__():
 parameters:
 alph:learning rate
 maxitr:maximum number of iteration for training
 thres:threshold value to check the convergence of MSE

 method description:constructor to initialize the variables of the class-alph,maxitr,thres

 2)gradient_descent():
 parameters:
 GD-to store the gradient descent details for each row
 method description: 
 This method performs gradient descent to update the weights to find the new values of y

 3)fitting():
 parameters:x,y,colcnt,rowcnt
 method description:This method is used to train the model. Starting with initial weights, we calculate the predicted values 
    of labels and corresponding mse.Gradient descent is performed over 'maxitr' number of iterations until it converges to find 
    the new weights for each class. We also assume the learning rate 'alph' at optimum level.

 4)plotmse()
  method description:This method is used to plot the MSE values vs the iteration numbers graphically

 5)predict()
  parameters:
   x-features of the test data
  method description:to calculate the predicted values of labels based on the test data using the weights obtained after training

 6)accuracy()
  parameters:
  y-label values
  ypred-predicted values of y
  method description: This method finds the accuracy of the model

Training and Testing:
 The training data available contains 20000 rows and 785 columns (labels and 784 features). The program reads the training data as a csv file and 
 separates the data for label and features. The features data is normalized to bring it in the range of 0-1. Over maxitr number of iterations, we have 
 initiated the weights with zero, then at every iteration we have calculated the MSE and we perform gradient descent to find the improved values of
 the weights.
 The testing data available contains 10000 rows and 785 columns (labels and 784 features). The program reads the test data as a csv file and separates
 the label and features. The feature data is normalized to bring it in the range of 0-1. We use the final weights obtained after training the model to 
 predict the values of y.

 The model calculates the accuracy of the predicted values of y by the R square method. The accuracy has been found to be 52.413% taking alpha as 0.01, 
 maxitr as 10000 and thres as 0.001. Due to limitations of the resources of the machine, the model could not be improved to the fullest extent. 



