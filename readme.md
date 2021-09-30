# Transfer Learning Model to Predict Food Image Beauty

This repository contains code to train a model to predict the beauty of food images. To achieve this, a model is first trained to classify different foods using the Food-11 dataset. Then the weights of the model are frozen and the last linear layer is removed. It is replaced with a linear layer to classify the images into appealing and non-appealing food images. This last layer is trained using the GPA dataset.

## Data
GPA: https://github.com/Openning07/GPA - choose the Positive/Negative Partition (Resized)
Food-11: https://www.epfl.ch/labs/mmspg/downloads/food-image-datasets/

## Training instructions:
1. Make sure the food-11 images are split into training and testing data and are put in folders according to the 11 categories. The same goes for the GPA data (with 2 categories). You may use the move.ipynb file to do so.
1. Open model.ipynb in google colab.
1. Enable GPU in google colab.
1. Run the model.ipynb
1. You can use the resulting pretrained_model.pth to classify food images into the 11 categories, as well as the final_model.pth to predict whether an image is appealing or not.

In my test run I achieved 45% accuracy on the Food11 classification and 65% accuracy on the GPA classificaton.