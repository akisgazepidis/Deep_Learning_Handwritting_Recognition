Handwriting Recognition Project
===============================

Overview
--------

This project focuses on developing a handwriting recognition system using machine learning techniques. The primary goal is to create a dataset from handwritten phrases in images of letters, train a classification model, and evaluate its performance on recognizing handwritten letters.

Dependencies
------------

Make sure to install the required Python libraries before running the code. You can install them using the following commands:

bashCopy code

`pip install pandas numpy matplotlib seaborn tensorflow scikit-learn`

Dataset
-------

The dataset used in this project consists of handwritten phrases captured in image format. The images are processed to extract features for training and evaluation.

### Loading and Preprocessing

The dataset is loaded and preprocessed in several steps:

1.  Loading images and labels from pre-saved numpy files.
2.  Taking subsets of the datasets for faster training and evaluation.
3.  Normalizing pixel values to the range \[0, 1\].
4.  Reshaping images to the required dimensions (28x28x1).

Model Architecture
------------------

The handwriting recognition model is built using TensorFlow and Keras. It consists of convolutional and dense layers.

### Model Compilation

The model is compiled using the Adam optimizer and categorical crossentropy loss function.

### Training

The model is trained using the training subset of the dataset. Training parameters include the number of epochs and batch size. Additionally, learning rate reduction and early stopping callbacks are applied during training.

Evaluation
----------

The trained model is evaluated on a separate test subset of the dataset. Performance metrics, such as accuracy and loss, are printed, and a confusion matrix is generated to assess the model's classification capabilities.

Visualization
-------------

The project includes visualizations to help understand the model's training and validation performance. This includes plots of loss and accuracy curves and a confusion matrix visualization.

Saving the Model
----------------

After training, the model is saved to disk in HDF5 format for future use.

TensorBoard
-----------

TensorBoard is utilized for monitoring the training process. Log files are stored in the 'logs' directory.

JSON File
---------

A JSON file containing a dictionary mapping numerical labels to corresponding letters is created and saved.