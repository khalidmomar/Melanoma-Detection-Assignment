# Melanoma Cancer Detection
> To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.


## Table of Contents
* General Information
* Technologies Used
* Steps 
* Conclusions


## General Information
> Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths.The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

- Actinic keratosis
- Basal cell carcinoma
- Dermatofibroma
- Melanoma
- Nevus
- Pigmented benign keratosis
- Seborrheic keratosis
- Squamous cell carcinoma
- Vascular lesion

## Technologies Used
- Tensorflow  	- Version : 2.9.2
- numpy   	- Version : 1.21.6
- pandas  	- Version : 1.3.5
- matplotlib  - Version : 3.2.2
- Augmentor




## Steps 

* Data Reading/Data Understanding → Defining the path for train and test images.
* Dataset Creation Train and Validation 20% set for validation.
* Dataset Creation → Create train & validation dataset from the train directory with a batch size of 32. Also, make sure to resize images to `180x180`.
* Dataset visualization → Create a code to visualize one instance of all the nine classes present in the dataset.
* Model Building & training:
  - Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model, rescale images to normalize pixel values between (0, 1).
  - Choose an appropriate optimiser and loss function for model training.
  - Train the model for 20 epochs.
  - Write our findings after the model fit. You must check if there is any evidence of model overfit or underfit.
* Choose an appropriate data augmentation strategy to resolve underfitting/overfitting
* Model Building & training on the augmented data:
  - Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model, rescale images to normalize pixel values between (0, 1).
  - Choose an appropriate optimiser and loss function for model training.
  - Train the model for 20 epochs.
  - Write our findings after the model fit, see if the earlier issue is resolved or not?
* Class distribution: Examine the current class distribution in the training dataset
  - Which class has the least number of samples? Answer: seborrheic keratosis.
  - Which classes dominate the data in terms of the proportionate number of samples? Answer: pigmented benign keratosis.
  - melanoma and pigmented benign keratosis have proportionate number of classes.
* Handling class imbalances: Rectify class imbalances present in the training dataset with Augmentor library.
* Model Building & training on the rectified class imbalance data:
  - Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model, rescale images to normalize pixel values between (0, 1).
  - Choose an appropriate optimiser and loss function for model training.
  - Train the model for 50 epochs.
  - Write our findings after the model fit, see if the issues are resolved or not?


- Model 1 Build,Train,Evaluate and state findings: -- CNN Model with Normalization Layer
- Model 2 Build,Train,Evaluate and state findings:s -- CNN Model with Augmentation
 strategy and Dropout layer
- Model 3 Build,Train,Evaluate and state findings: -- CNN Model with Augmentor to rectify imbalance class data

## Conclusions
- Training accuracy is 83% and validation accuracy is 77.4 %
- After using Augmentor and treating imbalance of all classes, there is a magnificent improvement in the training and validation accuracies.
- 50 epochs were used and more can be added to increase the accuracy further.
- Model 3 shows no overfitting or underfitting.

## Contact
Created by [@Khalid Omar] 
