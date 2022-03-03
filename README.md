# Emotion recognition using facial expressions
This project is 2020 summer project of brain and cognitive society ,Science and Technlogy council , **IIT Kanpur**. 
As the name suggests it is meant for leveraging the computer with the ability of classifying seven basic emotions using the facial expressions of 
humans.The seven basic emotions we're gonna classify are:

* Happy 
* Sad
* Angry
* Disgust
* Fear
* Surprise
* Contempt

## Dataset
We used the extended cohn kanade (CK+) dataset which can be found [here](https://www.kaggle.com/shawon10/ckplus)

## Reference Paper
The reference paper we used is [this](https://drive.google.com/file/d/1qMUhEFLUEuJlHO5SKjULNYfSS25ZSw4a/view) reasearch paper published on springer.

## Preprocessing
We performed the following preprocessing methods:

* [Face alignment](https://github.com/Av-hash/EmoRec/blob/master/FaceAlignment.ipynb)
* [Face cropping](https://github.com/Av-hash/EmoRec/blob/master/FaceCropping.ipynb)
* [Data normalization](https://github.com/Av-hash/EmoRec/blob/master/DataNormalization.ipynb)
* [Data augmentation](https://github.com/Av-hash/EmoRec/blob/master/DataAugmentation.ipynb)

## CNN model
We will be making a Sequential [model](https://github.com/Av-hash/EmoRec/blob/master/CNNmodel.ipynb) comprising of using two convolutional layers (conv2D), two MaxPooling2D layers , a Flatten layer followed by a output Dense layer with softmax activation , with adam optimizer and categorical crossentropy loss.

## Evaluation
We have evaluated our model on three different cropping methods:

* Cropping with background
* Cropping without background
* Cropping without forehead

Also we varied the neuron number of hidden dense layer as 0, 256, 512, 1024.
And we performed a ten fold [cross validation](https://github.com/Av-hash/EmoRec/blob/master/CrossValidation.ipynb) on our model keeping the cropping method fixed (without background) but varying the neuron number.

## Code
The link to the whole assembled code is [here](https://github.com/Av-hash/EmoRec/blob/master/Facial_Expression_Recognition.ipynb).

## How to run
For running the model , just run the python script [facial_expression_recognition.py](https://github.com/Av-hash/EmoRec/blob/master/facial_expression_recognition.py)

## Documentation
The documentation of this project can be found [here](https://drive.google.com/file/d/1ixtQco-1SQW4hH6pwLHVACqwrIZqrYbP/view?usp=drivesdk).

## Results
The results of various evaluation methods we used are illustrated in this table :

### Cropping without background

|No. of neurons     |Accuracy graph   |Confusion matrix   |
|---|---|---|
|0   |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/FER%20acc%20graph%20with%200%20neurons%20without%20background.jpg)  |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/Confusion%20matrix%20with%200%20neuron%20without%20background.jpg)   |   
|256  |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/FER%20acc%20graph%20with%20256%20neurons%20without%20background.jpg)   |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/Confusion%20matrix%20with%20256%20neuron%20without%20background.jpg)  |     
|512   |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/FER%20acc%20graph%20with%20512%20neurons%20without%20background.jpg)   |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/Confusion%20matrix%20with%20512%20neuron%20without%20background.jpg)  |      
|1024   |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/FER%20acc%20graph%20with%201024%20neurons%20without%20background.jpg)  |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/Confusion%20matrix%20with%201024%20neuron%20without%20background.jpg)  | 

### Cropping without forehead

|No. of neurons     |Accuracy graph   |Confusion matrix   |
|---|---|---|
|0   |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/FER%20acc%20graph%20with%200%20neurons%20without%20forehead.jpg)  |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/Confusion%20matrix%20with%200%20neuron%20without%20forehead.jpg)   |   
|256  |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/FER%20acc%20graph%20with%20256%20neurons%20without%20forehead.jpg)   |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/Confusion%20matrix%20with%20256%20neuron%20without%20forehead.jpg)   |     
|512   |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/FER%20acc%20graph%20with%20512%20neurons%20without%20forehead.jpg)   |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/Confusion%20matrix%20with%20512%20neuron%20without%20forehead.jpg)   |   
|1024   |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/FER%20acc%20graph%20with%201024%20neurons%20without%20forehead.jpg)   |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/Confusion%20matrix%20with%201024%20neuron%20without%20forehead.jpg)   | 

### Cropping with background

|No. of neurons     |Accuracy graph   |Confusion matrix   |
|---|---|---|
|0   |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/FER%20acc%20graph%20with%200%20neurons%20with%20background.jpg)  |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/Confusion%20matrix%20with%200%20neuron%20with%20background.jpg)   |   
|256  |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/FER%20acc%20graph%20with%20256%20neurons%20with%20background.jpg)   |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/Confusion%20matrix%20with%20256%20neuron%20with%20background.jpg)   |     
|512   |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/FER%20acc%20graph%20with%20512%20neurons%20with%20background.jpg)   |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/Confusion%20matrix%20with%20512%20neuron%20with%20background.jpg)   |      
|1024   |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/FER%20acc%20graph%20with%201024%20neurons%20with%20background.jpg)   |[Link](https://github.com/Av-hash/EmoRec/blob/master/images/Confusion%20matrix%20with%201024%20neuron%20with%20background.jpg)   | 

### Cross Validation
We have done a ten-fold cross validation on our dataset. Following the research paper , it was done with same cropping method (without background) but with different neuron numbers.

|No. of neurons   |Accuracy  |      
|---|---|
|0   |97.96   |         
|256   |98.27   |         
|512   |96.62   |   
|1024   |97.14   |   

#### Average accuracy

|On the paper   | On our Model   |
|---|---|
|97.38   |97.49   |

## Reference Links

* https://link.springer.com/article/10.1186/s13640-018-0324-4
* https://machinelearningmastery.com/how-to-configure-image-data-augmentation-when-training-deep-learning-neural-networks/
* https://blog.keras.io/building-powerful-image-classification-models-using-very-little-data.html
* https://coursera.org/share/111ff958aae8ede07800d98664152420
* https://www.pyimagesearch.com/2017/05/22/face-alignment-with-opencv-and-python/
* https://machinelearningmastery.com/k-fold-cross-validation/


