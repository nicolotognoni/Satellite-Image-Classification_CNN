# Satellite-Image-Classification_CNN

I created a satellite image classification with a CNN.

The code is entirely written in python using TensorFlow, I used Google Colab and stored the images in Google Drive

To load the images I used ImageDataGenerators. I applied Data Augmentation to reduce overfitting and improve the accuracy of the model.

The CNN used is the following: 
The model is trained with Batches of size 32, and is composed by the following layers:

- Conv2D with 8 filters and a kernel of 3,3
- ReLU
- MaxPool2D with pool size 2,2
- Conv2D with 16 filters and a kernel of 3,3
- ReLU
- MaxPool2D with pool size 2,2
- Conv2D with 32 filters and a kernel of 3,3
- ReLU
- MaxPool2D with pool size 2,2
- Flatten
- Dense of 300 units with Sigmoid function
- Dense of 21 units with Softmax function

This model reached an accuracy of 82%

In the last part of the code I implemented Transfer Learning by using pre-trained InceptionV3 on ImageNet from Google and it reached an accuracy of 93% on the validation set.
