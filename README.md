# IceCreamLabs-Assignment

## Assignment 1 - Toxic Comment Classification Challenge

Model 1 --- 

![alt text](https://github.com/anantiitml/IceCreamLabs-Assignment/blob/master/block.png)

![alt text](https://github.com/anantiitml/IceCreamLabs-Assignment/blob/master/Model1.PNG)

Model 2 ---

![alt text](https://github.com/anantiitml/IceCreamLabs-Assignment/blob/master/block1.png)


![alt text](https://github.com/anantiitml/IceCreamLabs-Assignment/blob/master/Model2.PNG)

Model 3 ----

![alt text](https://github.com/anantiitml/IceCreamLabs-Assignment/blob/master/block2.png)

![alt text](https://github.com/anantiitml/IceCreamLabs-Assignment/blob/master/Model3.PNG)


Kaggle Submission---

![alt text](https://github.com/anantiitml/IceCreamLabs-Assignment/blob/master/Kaggle%20submission.PNG)

Conclusion : 
As I have mentioned in the notebook max-pooling does not give an advantage here as it just takes the maximum in that window and try to predict the results but thats not the case as from the given input sequence we have to predict the probabilities for each type of class so for example some information in that window may be not maximum but due to max-pooling it gets lost. 

Further we can improve on scores by not taking in to account the words which does not have any meaning for the context to predict the possibilities of each of the class contents. Also we can fine tune the max-words for which we have to learn an embedding say for example if we take 80,000 words and some insignificant word comes after 80,000 then the accuracy can be improved drastically.

## Assignment 2 - Dog Breed Classification 

Model 1 -------

1. Convetional layer (detect features in image matrix)
2. Pooling layer (recongise features in different angle and/or size)
3. Convetional layer
4. Pooling layer
5. Flattening layer (flatten layers in array of imput)
6. Full connected layer (full connected ANN)
7. Output layer

Score --- 4.66735 Number of Epochs -- 2

![alt text](https://github.com/anantiitml/IceCreamLabs-Assignment/blob/master/acc2.PNG)

As seen from the figure the validation accuracy tracks the training accuracy fairly well. This case indicates that this model capacity is not high enough: So we have to make the model larger by increasing the number of parameters.

Model 2 ----

1. Convetional layer (detect features in image matrix)
2. Pooling layer (recongise features in different angle and/or size)
3. Convetional layer
4. Pooling layer
5. Convetional layer
6. Pooling layer
7. Flattening layer (flatten layers in array of imput)
8. Full connected layer (full connected ANN)
9. Output layer

Score --- 4.69661 Number of Epochs -- 2

![alt text](https://github.com/anantiitml/IceCreamLabs-Assignment/blob/master/acc.PNG)

So even after increasing the model capacity our score goes low instead of validation accuracy does not show overfitting but as we seen training accuracy does not follow up with validation accuracy, this indicates that the loss function isn't converging this is due to we have less data even MNIST data has 60,000 training samples to get accuracy of 98%. So we have to augment the data to create more data by introducing rotation or applying other Affine transformations as CNN is location invariant due to pooling. Also we can use many pretrained models like Xception, InceptionV3, VGG_Net, RES_NET but with keep in mind we have to do data augmentation as cleared from the next model.

Model 3 ----

1. Xception 
2. Flatten
3. Dense 512
4. Dense 120 (Output layer)

![alt text](https://github.com/anantiitml/IceCreamLabs-Assignment/blob/master/acc1.PNG)

As seen from figure the model is highly overfitted so we have to do Data Augmentation. I am working on will update that Soon!!!
