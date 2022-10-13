# Satellite Image Classification with a CNN
### Using a Convolutional Neural Network to classify satellite images into different categories.

The code is entirely written in python using TensorFlow, I used Google Colab and stored the images in Google Drive

To **load the images** I used ImageDataGenerators. I applied Data Augmentation to reduce overfitting and improve the accuracy of the model.

The **CNN used** is the following: 
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

This model reached an **accuracy of 82%**

In the last part of the code I implemented **Transfer Learning** by using pre-trained InceptionV3 on ImageNet from Google and it reached an accuracy of 93% on the validation set.


## How to run the notebook
We pre-run the entire notebook and kept the results of the different models.

However, if you want to run it you need to know a few things:

We stored our data on Google Drive so in order to run the code you need to upload the Folder with the images in your Google Drive under the following path: drive/MyDrive/Colab Notebooks/UCMerced_LandUse
We divided the code in 'Chapters' and we tried to make every single one indipendent from the rest of the code in order to be able to run them indipendently. In many of them we put a sub-chapter to load the right data to run the model.

## Dataset

As dataset I used the UC Merced Land Use Dataset composed by 21 classes, each of 256x256 pixels.
To download the dataset go to the official website: http://weegee.vision.ucmerced.edu/datasets/landuse.html
