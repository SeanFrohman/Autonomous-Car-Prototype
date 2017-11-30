# Autonomous Car

This project uses various Deep Learning model architectures to classify the self-generated road data for building an autonomous car.

### Car Prototype
<img src="https://github.com/First-Of-His-Name/Autonomous-Car-Prototype/blob/master/Car_image.jpg"/>

### Images
The bluetooth controlled car was driven on an indoor track and the training data was generated by taking images from a camera mounted on the car. The images were labelled manually into 4 categories:
1. Front (F)
2. Left  (L)
3. Right (R)
4. Stop  (S)

<img src="https://github.com/First-Of-His-Name/Autonomous-Car-Prototype/blob/master/track_image1.jpg" width="270px" height="270px"/> <img src="https://github.com/First-Of-His-Name/Autonomous-Car-Prototype/blob/master/track_image2.jpg" width="270px" height="270px"/> <img src="https://github.com/First-Of-His-Name/Autonomous-Car-Prototype/blob/master/track_image3.jpg" width="270px" height="270px"/>

### Image Processing
In order to reduce the computation, images were resized from 480x640 to 24x32 pixels.
Then the images were cropped to keep only the track area. Final image size was 14x32 pixels.
The images were normalized before giving them to the input layer.

### Model Architectures
#### 1. CNN
The first model of cnn was of two convolutional layer followed by 1 fully connected and then the output layer.
The model accuracy was around 91%.
Since, the images were manually labelled, there was a huge human error. 91% accuracy of model is hence justified.
[Go to file](https://github.com/First-Of-His-Name/Autonomous-Car-Prototype/blob/master/tf_model_cnn.py)
#### 2. RNN
The RNN model was trained with two LSTM layers. Accuracy was 89.8%.
[Go to file](https://github.com/First-Of-His-Name/Autonomous-Car-Prototype/blob/master/tf_model_rnn.py)
#### 3. CNN + RNN
The final model was cnn followed by rnn. This model performed very badly on the training data with the accuracy of 70% since, after the convolutional layer, there was huge loss in the temporal features of the data.
[Go to file](https://github.com/First-Of-His-Name/Autonomous-Car-Prototype/blob/master/tf_model_cnn_rnn.py)

Find more details about the project [here].(https://github.com/First-Of-His-Name/Autonomous-Car-Prototype/blob/master/Review.ipynb)
