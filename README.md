# ImageClassificationProject
Final Project for The Developer Academy

The dataset for this project can be found here:
  https://www.kaggle.com/andrewmvd/leukemia-classification
  
**Acute lymphoblastic leukemia (ALL)**
Acute lymphoblastic leukemia (ALL) is the most common type of childhood cancer.

**Task**: Create a image classification model to distinguish between normal and cancer cells.

**Dataset**
In total there are 15,135 images from 118 patients with two labelled classes:
- Normal cell,
- Leukemia blast.

![alt text](https://github.com/Este-code/ImageClassificationProject/blob/main/images/dataset.jpg)

The dataset has 3 different folder: 
  - Traning 
  - Test 
  - Validation.
  
The first step is to extract every image from the training folder, and put them into an array, and, while saving them I am resizing every image in case they have different sizes. Every image was divided in 2 folders, (ALL --> Acute lymphoblastic leukemia, hem --> cells without leukemia), therefore I will asign a label to every image. Due to the large amount of data, there are another 3 folder inside the training directory, therefore I decided to use only one of them, for practical reasons and due to my pc performances.
Into the validaton folder, you can find a csv file with Patients ID and labels. You also will find, a second directory with the images of every observations of the previous file.

**Countplot**

Here I am creating a simple countplot that represent the amount of images of cells affected and not affected by leukemia.

![alt text](https://github.com/Este-code/ImageClassificationProject/blob/main/images/graph.jpg)

**Cells images**

I have decided to show one of each cases.

![alt text](https://github.com/Este-code/ImageClassificationProject/blob/main/images/all.jpg)

Above is a cell, **affected** by leukiema

![alt text](https://github.com/Este-code/ImageClassificationProject/blob/main/images/hem.jpg)

Above is a cell, **not** affected by leukiema

**Model**


![alt text](https://github.com/Este-code/ImageClassificationProject/blob/main/images/model.jpg)

In this step I will define the CNN model layers. It has 5 hidden layers where it's filtering(Conv2D creates a feature map that summarizes of detected features, here I,m using relu as activation function) and pooling (MaxPool2D selects the maximum element from the feature map covered by the filter) every image. In every hidden layers there is a Dropout layer that helps prevent overfitting. Flatten converts the multi-dimensional image data array to 1d array.

**Accuracy and Loss**


![alt text](https://github.com/Este-code/ImageClassificationProject/blob/main/images/graph1.jpg)

From the graphs I can assume that more training for the model would bring more accuracy and less loss of data.
However, an Image Classification model for this dataset is not the best option to choose.

**Recommendation**

- L1 and L2 regularization..
- Use the rest of the data.
- Calculate more statistics (such as precision etc.)
- Compare with a different model.




