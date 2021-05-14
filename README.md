# Fashion-MNIST-Image-Classification-using-Deep-Learning
The Fashion-MNIST clothing classification problem is a new standard dataset used in computer vision and deep learning. The ‘target’ dataset has 10 class labels, as we can see from above (0 – T-shirt/top, 1 – Trouser…9 – Ankle Boot). Given the images of the articles, we need to classify them into one of these classes, hence, it is essentially a ‘Multi-class Classification’ problem. A suitable algorithm is used to solve this dataset and help in the prediction and classification of the images.

It is a dataset comprised of 60,000 small square 28×28 pixel grayscale images of items of 10 types of clothing, such as shoes, t-shirts, dresses, and more. Each pixel is a value from 0 to 255, describing the pixel intensity. 0 for white and 255 for black. The mapping of all 0-9 integers to class labels is listed below.

0: T-shirt/top
1: Trouser
2: Pullover
3: Dress
4: Coat
5: Sandal
6: Shirt
7: Sneaker
8: Bag
9: Ankle boot


# Model Used:

Convolution Neural Network is used to construct the model for classification of images. For the convolutional front-end, we can start with a Three convolutional layer with a small filter size and a modest number of filters (64) followed by a max pooling layer. The filter maps can then be flattened to provide features to the classifier.

Given that the problem is a multi-class classification, we know that we will require an output layer with 10 nodes in order to predict the probability distribution of an image belonging to each of the 10 classes. This will also require the use of a softmax activation function. Between the feature extractor and the output layer, we can add a dense layer to interpret the features, in this case with 128 nodes.

Keras library is used to assemble and plot the neural network work flow using sequential layers and kernel size of 3. All layers will use the ReLU activation function and the He weight initialization scheme, both best practices.

The model is compiled and then fit with 20 epochs and loss of sparse categorical cross entropy. After this, the model is put to test using the predict method following which the evaluation is done
