# Covid Xray CNN Classifier

The 2019 novel coronavirus (COVID-19) presents several unique features. While the diagnosis is confirmed using polymerase chain reaction (PCR), infected patients with pneumonia may present on chest X-ray and computed tomography (CT) images with a pattern that is only moderately characteristic for the human eye Ng, 2020. COVID-19’s rate of transmission depends on our capacity to reliably identify infected patients with a low rate of false negatives. In addition, a low rate of false positives is required to avoid further increasing the burden on the healthcare system by unnecessarily exposing patients to quarantine if that is not required. Along with proper infection control, it is evident that timely detection of the disease would enable the implementation of all the supportive care required by patients affected by COVID-19.

In late January, a Chinese team published a paper detailing the clinical and paraclinical features of COVID-19. They reported that patients present abnormalities in chest CT images with most having bilateral involvement Huang 2020. Bilateral multiple lobular and subsegmental areas of consolidation constitute the typical findings in chest CT images of intensive care unit (ICU) patients on admission Huang 2020. In comparison, non-ICU patients show bilateral ground-glass opacity and subsegmental areas of consolidation in their chest CT images Huang 2020. In these patients, later chest CT images display bilateral ground-glass opacity with resolved consolidation Huang 2020.

## Challenge

I decided to face the challenge to build new image classifier to detect COVID by xray exams, considering that new kinds of diagnose would be too helpfull to relieve the health public systems that are dealing with a huge number of tests requests, also it was a good opportunity to put in pratice some skills learned on my last completed courses.

It was decided to work only with Convolution Neural Networks models, this family of algorithms that has been showing the bests results for image classifiers.

## Dataset

The dataset used in these notebooks is available at [Kaggle](https://www.kaggle.com/) plataform by accessing this [link](https://www.kaggle.com/tawsifurrahman/covid19-radiography-database).
The dataset was created by a team of researchers from Qatar University, Doha, Qatar and the University of Dhaka, Bangladesh along with their collaborators from Pakistan and Malaysia in collaboration with medical doctors have created a database of chest X-ray images for COVID-19 positive cases along with Normal and Viral Pneumonia images. At the current moment that this project was developed, in the last release there are 219 COVID-19 positive images, 1341 normal images and 1345 viral pneumonia images. We will continue to update this database as soon as we have new x-ray images for COVID-19 pneumonia patients.

## The project

Before build the new model architecture and fitting it, the earlier steps was to analyse the image dataset that I have on hands, visualizing some images of the three possible pacient conditions (COVID-10, normal and pneumonia) and checking the pixels intensity distribution that affects the training model.

(Screenshot (26).png)
Samples in dataset

(Screenshot (27).png
Histogram and Cumulative Distribution Function of pixels from the images above.

Also in the beginning the data was split in test and train folders. The train folder contains the images to fit and validate the model (0.2 was set to validation), finally test folder contains the images that will be used in the final evaluation.

The next step was testing the perfomance of three models that was created based on some of the best CNN clasifiers: LeNet-5 and VGG. The skeleton architecture of each model was selected by a sequence of layers:

1. Conv-Pol-Conv-Pol
2. Conv-Pol-Conv-Pol doubling the filter values for each layer
3. Conv-Conv-Pool-Conv-Conv-Pool

The two firsts model perfomed better for the dataset, so their skeleton was used to build a new model.

### New model

Before create the model, some image preprocessing techniques was applied, like: rotation, reshape, standartization and so on. This process is known as augmentation dataset and is used in orden to obtain a diversed data that will result in in more skillful models, and the augmentation techniques can create variations of the images that can improve the ability of the fit models to generalize what they have learned to new images.
Doing that, some parameters was tested till the best results was reached. You can see the new model architecure on the image below:

--- foto

During the training process with 50 epochs the best accuracy obtained was an accuracy of 0.9478 validate accuracy of 0.9751 
You can check how these metrics varied during the training:

-- foto

### Results

The results in validation process was satisfactory, but in evaluate process the result seems that was not so good, but checking another papers I realize that the diagnosis of COVID using only XRay image is a really hard task, that's why health authorities in China abandoned this approach and reverted back to PCR-based testing, also considering the small dataset that I have on hands and its poor qualitity images the model had a good perfomance even in evaluation. For comparing, the VGG model obtained an accuracy of 0.66 for the same task.
