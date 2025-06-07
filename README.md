# AI-ML-Core-Project



Project: Neural Networks from Scratch (MNIST Project)

- In this project, I have built a Neural Network from Scratch for classifying handwritten digits.
- Note: No Neural Network built-in libraries have been used.


Files:-

- Data Set: MNIST dataset.
- Data Set Classification: 42000 training set (train.csv) + 28000 test set (test.csv)
- Prediction's file: mnist_submission.csv  (following the format of sample_submission.csv)
- Jupyter Notebook: Neural_Networks_from_Scratch_(MNIST_Project)_final.ipynb


Data:-

1. train.csv contains 42000 training set data with first column containing the labels (y_train) and the rest 784 columns containing the 784 pixels of 28x28 MNIST handwritten digit images (X_train).
2. test.csv  contains 28000 test set data with only 784 columns corresponding to the 784 pixels of MNIST images. On this set, the generated model will have to predict the label/number (y-hat).


Approach:-

1. Importing fundamental libraries- NumPy, Matplotlib, Pandas.
2. Importing the training data from the file 'train.csv' using pandas.
3. Converting this data-frame into NumPy array using NumPy.
4. Extracting X_train and y_train from the train_data NumPy array.
5. Normalizing the X_train by bringing the values of pixels between [0,1].
6. Choosing a Neural Network Architecture.
7. Initializing random initial values to our parameters.
8. Performing Forward Prop.
9. Performing Back Prop.
10. Defining a Cost Function (Cross-Entropy Loss function).
11. Defining a Gradient Descent Function.
12. Run this Gradient Descent to get the model parameters and also at intervals calculate the Cost (to check if it is decreasing, as expected).
13. Define a function to get the Predictions from the model using any input and the model parameters found using Gradient Descent.
14. Importing the test-set ('test.csv') using Pandas and converting it into NumPy array.
15. Store all the predictions of test.csv in the form of an array with the label (y-hat) corresponding to the same index as the test-set example. (1-based indexing)
16. Using Pandas convert this array of predictions of test-set into a csv file - 'mnist_submission.csv'


Neural Network Architecture:-

- Input Layer of array = 42000 x 784
- Hidden Layer 1: relu activation; 25 units; W1.shape = (42000, 25); b1.shape = (25,)
- Hidden Layer 2: relu activation; 15 units; W2.shape = (25, 15) ; b2.shape = (15,)
- Output Layer : softmax activation; 10 units; W3.shape = (15,10) ; b3.shape = (10,)


Neural Network Model:-

  A. Forward Prop:-
  - Helps to find Outputs of every layer.
  - Requires the definition of various activation functions: ReLU and Softmax.

  B. Back Prop:-
  - Helps to find the gradients in reverse direction of Forward Prop.
  - Requires the definition of derivative of ReLU function and also requires One-Hot encoding of Y_train.


Cost Function:-

- Finds the Cross-entropy Cost function.
- It should be decreasing at every iteration of Gradient Descent.


Gradient Descent:-

- Helps to find the parameters of the model.
- Runs Forward Prop, Back Prop and Update Parameters simultaneously.
