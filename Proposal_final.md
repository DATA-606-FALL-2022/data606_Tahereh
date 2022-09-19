## Object detection and localization

Object detection is a task that determines whether there is a specific object in an image or not. On the other hand, object localization draws a bounding box around the object of interest in the image.

### Application of object detection and localization

Object detection and localization have a lot of applications in different areas such as self-driving cars, video surveillance, and climate change. For example, Autonomous vehicles rely on the perception of their surroundings to ensure safe and robust driving performance. This perception system uses object detection algorithms to accurately determine objects such as pedestrians, vehicles, traffic signs, and barriers in the vehicle's vicinity. Or video surveillance uses object detection algorithms to detect moving objects in a surveillance video and predict whether it is a human or not.

### Challenges in object detection and localization

Although these tasks are very easy to solve for humans, they require sophisticated algorithms to be implemented by the computers. As explained above, two consecutive tasks should be solved so that the algorithm can predict the box around the object. These tasks are as follows:

1. Binary classification (for object detection) 
2. Nonlinear regression (for object localization)

To solve the first task one should minimize the logistic loss for training examples. Also for the second task one should minimize the mean square error loss to teach the model to predict bounding boxes. Therefore, one should answer the following questions:

1. Can a deep neural network solve both tasks simultaneously?
2. Is there a loss function that can be used to solve both tasks?
3. If yes, what is that?
4. If not, how can we combine both means square error and logistic loss to solve these two tasks?
5. What percentage of data does not include an object and how does this ratio affect the designation of the loss function?

### Data

The data for training and testing will be a synthetic data set that can generate as many as samples that are required.

Objects that are to be detected are all parallelograms with random sides at a random position in an image which is contaminated with noise. To generate such parallelograms I do the following:

1. Denote (1,0), (0,1), (-1,0), and (0,-1) on the 2D plane.
2. Rotate both (1,0) and (-1,0) with a random degree clockwise using a rotation matrix.
3. Do the same rotation process for (0,1) and (0,-1). (step 2 and 3 guarantee that diagonals are not perpendicular to each other. Otherwise, we get a rhombus instead of parallelograms.)
4. Once we have all four corners we stretch x-values and y-values to get a bigger parallelogram that fits in the image size.
5. Randomly rotate the parallelogram clockwise to make sure its rotation is random. 
6. Translate the center of parallelogram from (0,0) to a new random center. 
7. Fill all the points on the sides of the parallelogram and put it on a noisy picture. 

For the data I save the image and for the label, I save the center, rotation and stretch values. In an IPython notebook file I have implemented all the above processes that generate a picture that has a parallelogram in it. I will use this code to create however many samples that are needed for my project.

### How can we measure the accuracy of the model?

For examining the accuracy of the algorithm we need to consider two things separately. First, the Accuracy, Precision, Recall and F1-Score of the binary classifier that is responsible for object detection. Second we need to examine the accuracy of the object localization. To do that we need to consider Intersection over Union (IoU) which is an evaluation metric used to measure the accuracy of an object detector.

### The type of deep neural network

As the studied data is a set of images including objects, I will be using convolutional neural networks to build a binary classification and to build a network that does object localization.


### The ultimate goal

By the end of this project, I would like to have a deep knowledge about object detection and localization. To achieve this goal, I need to understand how loss functions in deep neural networks are utilized and how I can use them for my problem. In addition, I would be required to utilize deep neural networks which will help me to be familiar with deep neural networks. Hopefully, by the end of this project I will acquire skill sets that help me solve object detection and localization efficiently.
