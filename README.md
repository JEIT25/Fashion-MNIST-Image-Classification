Fashion MNIST Dataset

Questions:
1. What is the Fashion MNIST dataset?
The Fashion MNIST dataset is a collection of 70,000 grayscale images of fashion articles, split into 60,000 training images and 10,000 testing images. Each image is 28x28 pixels and categorized into one of 10 fashion classes (e.g., 'T-shirt/top', 'Trouser', 'Sneaker'). It's often used as a direct replacement for the original MNIST handwritten digit dataset.

2. Why do we normalize image pixel values before training?
Image pixel values, typically ranging from 0 to 255, are normalized to a 0-1 range (by dividing by 255.0) for several reasons:

Faster Convergence: Normalization helps optimization algorithms converge more quickly as input features are on a similar scale.
Improved Stability: It prevents certain features from dominating the learning process and can lead to better overall model performance and stability.
3. List the layers used in the neural network and their functions.
The neural network uses a simple sequential architecture:

keras.layers.Flatten(input_shape=(28, 28)):

Function: Reshapes the 2D input images (28x28 pixels) into a 1D array (784 pixels).
Parameters: 0 (it only transforms data, no trainable weights).
keras.layers.Dense(128, activation='relu'):

Function: A fully connected hidden layer with 128 neurons. The relu (Rectified Linear Unit) activation function introduces non-linearity.
Parameters: 100,480 (784 inputs * 128 neurons + 128 biases).
keras.layers.Dense(10):

Function: The output layer with 10 neurons, one for each fashion class. It produces raw scores (logits) that are then typically converted to probabilities by a Softmax activation.
Parameters: 1,290 (128 inputs * 10 neurons + 10 biases).
4. What does an epoch mean in model training?
An epoch signifies one complete pass through the entire training dataset. During an epoch, the model processes every training example, updates its internal parameters (weights and biases), and evaluates its performance (loss and metrics). This model was trained for 10 epochs.

5. Compare the predicted label and actual label for the first test image.
For the first test image, the model's prediction was accurate:

Predicted label: 9 (Ankle boot)
Actual label: 9 (Ankle boot)
6. What could be done to improve the model’s accuracy?
To potentially improve the model's accuracy, consider these strategies:

Increase Model Complexity: Add more hidden layers or increase the number of neurons per layer.
Regularization Techniques: Implement Dropout layers or L1/L2 regularization to prevent overfitting.
Convolutional Neural Networks (CNNs): For image data, CNNs are generally more effective as they can learn spatial hierarchies and features.
Hyperparameter Tuning: Experiment with different optimizers (e.g., Adam, SGD with momentum), learning rates, batch sizes, and number of epochs.
Data Augmentation: Generate more diverse training data by applying random transformations (e.g., rotations, shifts, zooms) to existing images.
Early Stopping: Monitor performance on a validation set and stop training when validation loss starts to increase, preventing further overfitting.
Advanced Architectures: Explore pre-trained models or more complex network architectures suitable for image classification.
