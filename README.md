👗 Fashion MNIST Image Classification

🔗 Google Colab Notebook:
[https://colab.research.google.com/drive/1HsfEQ7qbvpBw98vKFbFK4b5Q2Jmh50lz?usp=sharing](Google_Collab_File_Link)

Questions and Answers:
1. What is the Fashion MNIST dataset? <br> The Fashion MNIST dataset is a group of 70,000 pictures of clothes in black and white. It is split into 60,000 pictures for training the computer and 10,000 for testing it. Every picture is small, only 28x28 pixels, and fits into one of 10 categories like shirts, sneakers, or pants.
2. Why do we normalize image pixel values before training? <br> We normalize the pixel values by dividing them by 255 to change the range from 0–255 down to 0–1. This is important because it makes the math easier for the computer. It helps the model learn faster and keeps the training process stable so one feature doesn't overpower the others.
3.  List the layers used in the neural network and their functions. <br> The neural network has three main layers. First, the Flatten layer takes the square picture and turns it into a long line of pixels. Second, a hidden Dense layer with 128 neurons uses the "relu" function to learn patterns. Finally, the last Dense layer has 10 neurons to decide which of the 10 clothing types the picture is.
4. What does an epoch mean in model training? <br> An epoch is just one full round of studying the whole dataset. During one epoch, the model looks at every training example to update its internal settings and learn better. For this project, I let the model train for 10 epochs.
5. Compare the predicted label and actual label for the first test image. <br> I checked the very first iage in the test group to see if the model was working right. The model guessed that the image was class 9, which is an Ankle boot. This was the correct answer, so the prediction was accurate.
6. What could be done to improve the model’s accuracy? <br> To make the model even better, I could use a Convolutional Neural Network (CNN) which is smarter at understanding images. I could also try adding more layers to the network or using "Dropout" to stop it from memorizing answers. Another idea is data augmentation, which creates slightly different versions of the pictures to give the model more practice.
