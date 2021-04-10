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
 

