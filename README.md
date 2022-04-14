# MNIST-
Predict the value of handwritten digits

You can check dataset by this link http://yann.lecun.com/exdb/mnist/ 

The dataset is a collection of 70.000 images of handwritten digits. First i load the data using scikit-learn provides fetch_openml convenience function 
to download the data set if is not found on disk and read it into an object. Some samples given bellow. 

![image](https://user-images.githubusercontent.com/99141535/163464249-72ec0457-97d0-4f31-9a86-fd0144c2736a.png)

The MNIST data set is partitioned into a trainig set of 60.000 images and test set of 10000 images. The dataset is commonly used to evaluate a variety of machine learning models.  It is popular because little preprocessing is required . Let’s use scikit learn to build a classifier that can predict the digit depicted in an image

# First import all necessary Libraries 
  _from sklearn.pipeline import Pipeline_ </br>
  _from sklearn.preprocessing import scale_ </br>
  _from sklearn.model_selection import train_test_split_ </br>
  _from sklearn.svm import SVC_ </br>
  _from sklearn.model_selection import GridSearchCV_  </br>
  _from sklearn.metrics import classification_report_ </br>

# After importing liblaries we load our dataset with fetch_openml function

  _from sklearn.datasets import fetch_openml_ </br>
  _mnist = fetch_openml('mnist_784')_ </br>
  
# Then we split the preprocessed data into training and test using 
 _X_train,X_test,y_train,y_test=train_test_split(X,y,random_state=11)_ 
 
# Next  instantiate an SVC or support vector classifier, object. 
  This object exposes an API like that of scikit-learn’s other estiomators. 
 The classifier is trained using the fit method and predictions are made using predict Method.
  The mods interesting hyperparameters of SVC are set bu the kernel,gamma and c keyword arguments. The kernel keyword arguments specifies the kernel 
  to be used. Scikit-learn provides implementations of the linear,polynomial,sigmoid,and radial basis function kernels . The degree argument should also be set when teh polynomial kernel is used. C controls regularization .G
  amma is kernel coefficient for the sigmoid . And our Final output is the following.
  
  
 # Results 
 ![image](https://user-images.githubusercontent.com/99141535/163465278-0bc9807a-1df8-4807-9796-096537fca0bc.png)
 
 
 # Files 
  You can find ipynb file from repository. As well as report for this project and Colab link for running it on Google Colab. 
  
