## Object detection and localization

### What is your issue of interest (provide sufficient background information)?

Object detection is a task that determines whether there is a specific object in an image or not. On the other hand, object localization draws a bounding box around the object of interest in the image.

### Why is this issue important to you and/or to others?

Object detection and localization have a lot of application in different areas such as self driving cars, video surveillance, and climate change. For example, Autonomous vehicles rely on the perception of their surroundings to ensure safe and robust driving performance. This perception system uses object detection algorithms to accurately determine objects such as pedestrians, vehicles, traffic signs, and barriers in the vehicle's vicinity. Or video surveillance uses object detection algorithms to for detecting moving objects in a surveillance video and predict whether it is a human or not.

### What questions do you have in mind and would like to answer?

Although these tasks are very easy to solve for humans, they are required suffisticated algorithms to be implemented by the computers. As explained above, two consecutive tasks should be solved so that the algorithm can predict the box around the object. Thesse tasks are as follows:
1. Binary classification 
2. Nonlinear regression
The first task should minimize the logistic loss and the second one should minimize the mean squere errors between true bounding boxes and the predicted ones. Therefore, one should answer the following questions:
1. Can a deep neural network solve both tasks simultaneously?
2. Is there a loss function that can be used to solve both tasks?
3. If yes, what that is?
4. If no, how can we combine both means square error and binary classification loss to solve these two tasks?
5. What percentage of data does not include an object and how this ratio affects the designation of the loss function?
### Where do you get the data to analyze and help answer your questions (creditability of source, quality of data, size of data, attributes of data. etc.)?

The data for training and testing can a be synthetic data set that can generate as many as samples that is required. For example, one can build a data generator that creates noisy pictures including random parallelograms with random sides. This data set generator should be established in way that the percentage of picture with no objects can be set before generating the data.

#### What will be your unit of analysis (for example, patient, organization, or country)? Roughly how many units (observations) do you expect to analyze?

For examining accuracy of the algorithm one needs to consider two things separately. First, the Accuracy, Precision, Recall and F1-Score of the binary classifire that is responsible for object detection. However, to examine the accuracy of the object localization one needs to consider Intersection over Union (IoU) which is an evaluation metric used to measure the accuracy of an object detector.
What variables/measures do you plan to use in your analysis (variables should be tied to the questions in #3)?
### What kinds of techniques/models do you plan to use (for example, clustering, NLP, ARIMA, etc.)?

As the studied data is a set on images including object, I will be using convolutional neural networks to create the binary classification and the part that creates the localization network.
How do you plan to develop/apply ML and how you evaluate/compare the performance of the models?

### What outcomes do you intend to achieve (better understanding of problems, tools to help solve problems, predictive analytics with practicle applications, etc)?

By the end of this project, I would like to have a depth knowledge about object detection and localization. To achieve this goal, I need to understand how loss functions in deep neural networks are utilized and how I can used them for my problem. In addition, I would be required to utilized deep neural networks which willhe help me to be familiar with deep neural networks. Hopefully, by the end of this project I aquire skill sets that help me solving object detection and localization efficiently.
