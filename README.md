## Brain Tumor MRI Convolutional Neural Network

In this project, we will modify a Convolutional Neural Network (CNN) to explore how adding and altering layers affects the model's performance. The task involves creating functions for reading image data, shuffling it, and reshaping it to be compatible with the CNN's expected input format. We'll train a model to classify images using TensorFlow and assess the impact of various modifications, including the addition of new layers and the removal of dropout layers.


# Purpose

The purpose of this project is to experiment with CNN architecture modifications to understand their impact on model performance, particularly on classification tasks. This project will help identify how changes in architecture, such as adding layers and dropout regularization, influence accuracy and model stability.

# Data source:  
https://wiki.cancerimagingarchive.net/display/Public/Brain-Tumor-Progression


# Function
We begin by defining several helper functions that read image data, shuffle it, and reshape it appropriately:

shuffle(X, y): Shuffles the images and labels to ensure they are not grouped by class.
read_image_data(filename): Reads grayscale image data into a 2D numpy array.
image_dir_to_array(dir): Converts images from a specified directory into a numpy array.
load_data(negative_images_path, positive_images_path): Loads negative and positive image datasets, shuffles them, and normalizes the pixel values.
reshape_X(X, img_channels, img_rows, img_cols): Reshapes the image data to match the input requirements of the CNN.
step_decay(epoch): Defines the learning rate schedule used for training.
create_model(img_channels, img_rows, img_cols): Defines and compiles the CNN model.

# Model Structure
Original Model:
We create a basic CNN with several convolutional layers, batch normalization, ReLU activations, max-pooling layers, dropout regularization, and a final sigmoid activation for binary classification.
Modified Models:
Without Dropout: We remove the dropout layers and observe the model’s performance. This may lead to overfitting.
With Additional Layers: After adding a new convolutional layer, we retrain the model to assess any improvement in classification performance.

# Model Training
Data Preprocessing: We load and preprocess the data, splitting it into a training set (67%) and a test set (33%).
Training: The model is trained for 10 epochs, and a learning rate scheduler is used to adjust the learning rate over time.
Evaluation: The ROC-AUC score is calculated to evaluate the model's performance, comparing the results before and after modifications.

# Results and Evaluation
ROC-AUC Score: This score provides insight into the model's ability to distinguish between the classes. We compare the performance of the models with and without dropout regularization and with the added convolutional layer.

# Conclusion
The final model, which includes the additional convolutional layer and dropout regularization, is expected to improve the ROC-AUC score compared to the original model.
