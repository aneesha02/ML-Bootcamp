# ML-Bootcamp
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
  y:label values after conversion
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
 

 



Algorithm Implemented:Neural Network
Class Name:smallneur
Methods:

 2)sigmoid():
 parameters:
 x-array whose sigmoid is to be found out
 method description: 
 This method finds the sigmoid value of the parameter.

 3)sig_der():
 parameters:
 x-array whose sigmoid derivative is to be found
 method description:This methos finds the sigmoid derivative of the parameter.

 4)softmax()
  parameters
  x-array whose softmax function is to be found
  method description:This method calculates the soft max function of the input parameter.
 
 5)fitting()
  parameters:
  x-feature set
  y-one hot encoded values of the labels
  method description: this method uses the sigmoid function and softmax function to calculate the activation values at hidden layer and output layer 
  respectively. We are using 1 hidden layer consisting of 10 nodes. The cross entropy cost function has been used. In the backpropagation 
  the derivatives are calculated in 2 phases i.e output layer followed by hidden layer. Hence the improved weights are calculated and this 
  has been repeated over maxitr number of times.

 5)predict()
  parameters:
   x-features of the test data
  method description:to calculate the predicted values of labels at the outer layer based on the test data using the weights obtained after training using
  forward propagation.

 6)accuracy()
  parameters:
  y-label values
  ypred-predicted values of y
  method description: This method finds the accuracy of the model

Training and Testing:
 The training data available contains 20000 rows and 785 columns (labels and 784 features). The program reads the training data as a csv file and 
 separates the data for label and features. The features data is normalized to bring it in the range of 0-1. Using sigmoid function and softmax function
 at hidden and output layer respectively, we calculate the predicted values by forward propagation. Using back propagation we find the improved weights.
 This is iterated maxitr number of times.
 The testing data available contains 10000 rows and 785 columns (labels and 784 features). The program reads the test data as a csv file and separates
 the label and features. The feature data is normalized to bring it in the range of 0-1. We use the final weights obtained after training the model to 
 predict the values of y at the output layer.

 The model uses sigmoid function and softmax function to predict the label which returns a value between 0-1. If the sigmoid value>=0.5 we will 
 consider it as 1 otherwise 0.These predicted values will be compared with the converted label values. We count the total number of matches and 
 divide it by number of rows. The accuracy has been found to be 11.35% taking alph=0.0001 and maxitr= 100 and hidden nodes=100. Due to limitations 
 of the resources of the machine, the model could not be improved to the fullest extent.
 
