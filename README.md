# Handwritten-digit-recognition-using-CNN

## Program has been separated into two 
  1. Classifying the MNIST dataset.
  2. Recognising the digit .
 
 
## About Dataset 

It is an inbuilt dataset from keras.
The training part of the datas contains 60000 datas with 28*28 each .
The testing part of the datas contains 10000 datas with 28*28 each .
The 28*28 matrix of each data represents the pixel's color values of each data.

![MNIST Dataset](https://user-images.githubusercontent.com/59074144/117337012-7da44600-aeba-11eb-9cf6-e2d535d579f7.png)

## Classifying the MNIST dataset

1. The pixel values are converted into binary values by one-hot encoding(to categorical()). 
2. CLassifying the dataset is carroed out through three layer of network. The sequential layers of the network is created using "Sequential()". The first two layers consist of 64 and 32 nodes respectively with kernel size as 3 and input shape = (28*28*1)
3. Relu and softmax activation functions have been used to build the model.
4. Inorder to optimize the model , Adam optimizer is used , to calculate the loss values for every iteration I used "categorical_crossentropy". There is other method  i.e., by using mean square error.
5. The values of model are predicted.

![prediction](https://user-images.githubusercontent.com/59074144/117341183-716eb780-aebf-11eb-965d-dde67009ee10.png)

The above snap shows the predicted values of each array which is further narrowed down to a single value by using the functionality called "argmax()" which is available in numpy module. It gives the classified mnist sample data.

![classification](https://user-images.githubusercontent.com/59074144/117341589-f5c13a80-aebf-11eb-82ce-d5e79776295b.png)

## Recognition 

1. This part of program comprises of two models where one model contains 2 layers and in other hidden layers are used.
2. In this same activation functions had been used. But, inorder to find the loss value for the optimizer , "sparce categorical crossentropy" which is similar to categorical crossentropy which had been used for the classification part.
3. After training the model with 2 layers ,heatmap is used to count the visualisation.

![heatmap](https://user-images.githubusercontent.com/59074144/117342366-ca8b1b00-aec0-11eb-91cc-3a7e5855af27.png)

1. This heatmap denotes the count of occurance of digits .

 The accuracy of the two layer model is 92% ( 0.9253) . Inorder to increase the accuracy, hidden layer is used. It improves the accuracy of the model to 98%.
 
 ![accuracy](https://user-images.githubusercontent.com/59074144/117343060-8cdac200-aec1-11eb-8b5f-f7f67b3843fc.png)
 
 The model is saved and is loaded for recognising.
 
 ## NOTE: USE ONLY GRAYSCALE IMAGE FOR RECOGNISING
