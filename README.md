# UMBC DATA 606 Project Report

## Project Descreption
 
Object detection and localization have a lot of applications in different areas such as self-driving cars, video surveillance, and climate change. For example, autonomous vehicles rely on the perception of their surroundings to ensure safe and robust driving performance. This perception system uses object detection algorithms to accurately determine objects such as pedestrians, vehicles, traffic signs, and barriers in the vehicle's vicinity. 

To explore the task of object detection and localization I generated 10,000 images whose sizes are 64x64. Inside of each image there are at most 3 objects with nine different classes. The size of each object and the position is random.

Data processing for training the deep neural network is standardization using mean subtraction and division by standard deviation.
I use DenseNet which is a convolutional neural network. The benefit of using DenseNet is that for each layer, the feature-maps of all preceding layers are used as inputs, and its own feature-maps are used as inputs into all subsequent layers.
To train the model I considered 100 epochs and I use minibatch size of 64. For the optimizer I use Adam optimizer with a learning rate of 0.001.




## Code
The comlete ccode implementing the project including data generation, trainig, test, and analysis of the result be found [here](https://github.com/DATA-606-FALL-2022/data606_Tahereh/blob/main/02_train_and_test_DenseNet.ipynb).

## Data
The data for the project is a synthetic dataset which is obtained by running [this notebook](https://github.com/DATA-606-FALL-2022/data606_Tahereh/blob/main/01_data_Generator.ipynb).

## Presentaion
- The video associated with the presentation is on YouTube and can be found [here](https://youtu.be/MDEWD0ut4Sc).
- The presentation is provided in two formats, a pdf file that can be found [here](https://github.com/DATA-606-FALL-2022/data606_Tahereh/blob/main/presentation/Presentation_Capstone606_Tahereh_Hematian.pdf) and a power point file which can be downloaded from [here](https://github.com/DATA-606-FALL-2022/data606_Tahereh/blob/main/presentation/Presentation_Capstone606_Tahereh_Hematian%20(2).pptx). Both of these files are in [the presentation folder](https://github.com/DATA-606-FALL-2022/data606_Tahereh/tree/main/presentation).
