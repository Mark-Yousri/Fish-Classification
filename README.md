## Classification of marine animals
The notebook aims to build and compare two models for classifying images of five types of marine animals: shark, jelly, whale, tuna, and fish.

## Data preparation
The notebook imports various libraries and defines the train and validation directories. It uses ImageDataGenerator to augment the train data and rescale the val data. It creates train and val generators with a target size of 224 x 224 and a batch size of 32.

## ResNet50 model
The notebook loads a pre-trained ResNet50 model without the top classification layers and freezes the convolutional layers. It adds a flatten layer, a dense layer with 256 units and relu activation, and a dense layer with 5 units and softmax activation. It compiles the model with Adam optimizer, categorical crossentropy loss, and accuracy metric. It trains the model for 10 epochs and plots the loss and accuracy curves.

## CNN model
The notebook defines a custom CNN model with three convolutional layers, three max pooling layers, a flatten layer, a dense layer with 256 units and relu activation, and a dense layer with 5 units and softmax activation. It compiles the model with RMSprop optimizer, categorical crossentropy loss, and accuracy metric. It trains the model for 30 epochs with a reduce learning rate on plateau callback and plots the loss and accuracy curves.

## Conclusion
This notebook provides a comprehensive guide to building and comparing two models for classifying images of marine animals. The ResNet50 model and the custom CNN model are both effective in achieving high accuracy on the validation set. The notebook demonstrates how to use Keras and TensorFlow to preprocess the data, build the models, train the models, and evaluate the models. It also shows how to visualize the training process and the performance metrics. The notebook can be used as a starting point for further research on marine animal classification or as a template for other image classification tasks.
