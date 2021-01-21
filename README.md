# Flaring black smoke detection
A CNN to detect black smoke from flaring activities.

Flaring images were collected from Google and manually label as NOT OK and OK based on the presence of black smock.

Due to the small sample size ~70 images per class, we apply image augmentation such as zooming and rotation to create variability in our training images so that our model can recognise the black smoke irregardless of the position in the images.

Keras was used to build a Convolution Neural Network, we splits our images to 80% training and 20% test dataset, fit the model and measure the accuracy and loss. To prevent overfitting, early stopping function to stop the model training process and use the callback function to save the best model on validation accuracy to make predictions on our test dataset.

From our best trained model, we observed test accuracy at 96.4% with just 61 epoch which is pretty amazing! 

To further validate our model, we then plot the test images, prediction, probability and label to visually inspect the result. 

From the plot, we observed only 1 image predicted incorrectly, this is perhaps due to the hazy greyish background which makes our model suggest the presence of black smoke. 

![Alt text](test_images.png?raw=true "Prediction on test images")

This is part of the project for IND5002 Digital-Physical Integration (NUS MSc. Industry 4.0).
