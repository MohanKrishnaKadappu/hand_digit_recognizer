# hand_digit_recognizer
classifier of 2 digit 
Handwritten digit recognition on MNIST Dataset
October 19, 2020
 Project Phase 2
In this article, I would be explaining a basic handwritten digit recognition using  LogisticRegression. But there are many ways classification can be done using algorithms such as Gradient Descent[SGD], Support Vector Machines[SVM], etc, which can be trained using the mnist dataset including deep learning [Convolutional Neural Network].
Source : Wikipedia , images from mnist test dataset
I ] First of all What is MNIST?
The MNIST database (Modified National Institute of Standards and Technology database) is a large database of handwritten digits that is commonly used for training various image processing systems. The database is also widely used for training and testing in the field of machine learning. It was created by "re-mixing" the samples from NIST's original datasets. The creators felt that since NIST's training dataset was taken from American Census Bureau employees, while the testing dataset was taken from American high school students, it was not well-suited for machine learning experiments. Furthermore, the black and white images from NIST were normalized to fit into a 28x28 pixel bounding box and anti-aliased, which introduced grayscale levels.

The MNIST database contains 60,000 training images and 10,000 testing images. Half of the training set and half of the test set were taken from NIST's training dataset, while the other half of the training set and the other half of the test set were taken from NIST's testing dataset. The original creators of the database keep a list of some of the methods tested on it. In their original paper, they use a support vector machine to get an error rate of 0.8%. An extended dataset similar to MNIST called EMNIST has been published in 2017, which contains 240,000 training images, and 40,000 testing images of handwritten digits and characters.

II ] Why mnist dataset only?

The MNIST dataset is known as hello world in machine learning and the data is already preprocessed and split properly into 60000  for training and 10000 for testing.

III ] How to obtain the Dataset?


The dataset has been successfully loaded


Here, there are 70,000 images and each image has 784 (28*28) features. Each image is 28*28 pixels, and each feature simply represents one pixel’s intensity from 0 (white) to 255 (black).

IV ] Analysis of the data


Data = 70,000 one-dimensional array, label is in object data type
Here,  the data is in a 1-d array.
The label is an object format. So, to build predictions of a digit, we have to convert it into an integer format.


V ] Plot of 1D Array [one dimensional] 
-> I had chosen 36001 image of the dataset



Note that → Here, interpolation='nearest' simply displays an image without trying to interpolate between pixels if the display resolution is not the same as the image resolution. It will result in an image in which pixels are displayed as a square of multiple pixels.
There is no relation between interpolation=’nearest’ and the grayscale image is displayed in color. By default, imshow uses the jet colormap to display an image. If you want it to be displayed in greyscale, call the gray() method to select the gray colormap.

VI ]  Split the Dataset in train and test  and shuffle index



Here, we are splitting x_train and x_test to 60000 and y_train and y_test also to 60000.
We are also shuffling the index of our training set using the NumPy array.

VII ] Test of our model [Creation of 2 detector] using LogisticRegression

As we can see our 2 digit model is able to classify any digit whether its 2 = true and not 2 = false




Conclusion:

Average Accuracy of Logistic Regression= 0.97815

Github link with readme :

https://github.com/MohanKrishnaKadappu/hand_digit_recognizer



I am thankful to the team ofsuvenconsultants for giving me this opportunity for this coding internship experience.



