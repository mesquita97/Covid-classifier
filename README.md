# Covid Xray CNN Classifier

## COVID-19

The 2019 novel coronavirus (COVID-19) presents several unique features. While the diagnosis is confirmed using polymerase chain reaction (PCR), infected patients with pneumonia may present on chest X-ray and computed tomography (CT) images with a pattern that is only moderately characteristic for the human eye Ng, 2020. COVID-19’s rate of transmission depends on our capacity to reliably identify infected patients with a low rate of false negatives.

## Challenge

I decided to face the challenge to build new image classifier to detect COVID by xray exams, considering that new kinds of diagnose would be too helpfull to relieve the health public systems that are dealing with a huge number of tests requests, also it was a good opportunity to put in pratice some skills learned on my last completed courses.

It was decided to work only with Convolution Neural Networks models, a new model was created by me based on one of the best image classifier called LeNet-5. After fitting the new CNN model, I apply the LeNet-5 on the same task to compare how well my model is doing.

## Dataset

The dataset used in these notebooks is available at [Kaggle](https://www.kaggle.com/) plataform by accessing this [link](https://www.kaggle.com/tawsifurrahman/covid19-radiography-database).
The dataset was created by mergin two datasets: The first one was created by a team of researchers from Qatar University, Doha, Qatar and the University of Dhaka, Bangladesh along with their collaborators from Pakistan and Malaysia in collaboration with medical doctors. At the current moment that this project was developed, in the last release there are 219 COVID-19 positive images, 1341 normal images and 1345 viral pneumonia images. We will continue to update this database as soon as we have new x-ray images for COVID-19 pneumonia patients.
The second database of COVID-19 x-ray images was obtained by the kaggle member from the Italian Society of Medical and Interventional Radiology (SIRM) COVID-19 DATABASE [1], Novel Corona Virus 2019 Dataset developed by Joseph Paul Cohen and Paul Morrison and Lan Dao in GitHub [2] and images extracted from 43 different publications.

(/images/xray_samples)
Some samples of dataset


### Results

The new classifier obtained these following scores for validation and evaluation, respectively: 

| Accuracy | Val. accuracy |                      
|----------|---------------|            
| 0.9870   | 0.9534        |
| 0.9466   | -             |
|          |               |

(/images/confusion_mat)

The new model had a good score both in validation and in the test with unseen data, but we can see in confusion matrix that the sensitivity for COVID-19 didn't work so well, probably because the small number of samples from pacients with this virus.
