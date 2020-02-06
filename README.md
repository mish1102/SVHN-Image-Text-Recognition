# SVHN-Image-Text-Recognition

SVHN is a real-world image dataset for developing machine learning and object recognition algorithms with minimal requirement on data preprocessing and formatting.The dataset is available on http://ufldl.stanford.edu/housenumbers/. 
The dataset is divided into three files namely, test, train and extra. 

#Overview of the Dataset : 
There are 10 classes, 1 for each digit. 
Digit '1' has label 1, '9' has label 9 and '0' has label 10.
1. Training dataset : 73257 digits
2. Test Dataset : 26032 digits
3. Extra Dataset : 531131 digits
#The extra dataset can be use to increase the training dataset if required.

The datset comes in two formats:
1. Original images with character level bounding boxes.
2. MNIST-like 32-by-32 images centered around a single character (many of the images do contain some distractors at the sides).

The bounding box information are stored in digitStruct.mat inside each dataset. This can be loaded in Matlab.The digitStruct.mat file contains a struct called digitStruct with the same length as the number of original images. Each element in digitStruct has the following fields: name which is a string containing the filename of the corresponding image. bbox which is a struct array that contains the position, size and label of each digit bounding box in the image. Eg: digitStruct(300).bbox(2).height gives height of the 2nd digit bounding box in the 300th image. 

#Scripts: 

convert.py : This file is responsible for converting .mat files in respective dataset record to the much readable json format. 
SVHN_problem_CV.ipynb : This is the file response file which take the image as an input and displays the Numerical digits as the output. 

