# Covid Xray Classifier

The 2019 novel coronavirus (COVID-19) presents several unique features. While the diagnosis is confirmed using polymerase chain reaction (PCR), infected patients with pneumonia may present on chest X-ray and computed tomography (CT) images with a pattern that is only moderately characteristic for the human eye Ng, 2020. COVID-19’s rate of transmission depends on our capacity to reliably identify infected patients with a low rate of false negatives. In addition, a low rate of false positives is required to avoid further increasing the burden on the healthcare system by unnecessarily exposing patients to quarantine if that is not required. Along with proper infection control, it is evident that timely detection of the disease would enable the implementation of all the supportive care required by patients affected by COVID-19.

In late January, a Chinese team published a paper detailing the clinical and paraclinical features of COVID-19. They reported that patients present abnormalities in chest CT images with most having bilateral involvement Huang 2020. Bilateral multiple lobular and subsegmental areas of consolidation constitute the typical findings in chest CT images of intensive care unit (ICU) patients on admission Huang 2020. In comparison, non-ICU patients show bilateral ground-glass opacity and subsegmental areas of consolidation in their chest CT images Huang 2020. In these patients, later chest CT images display bilateral ground-glass opacity with resolved consolidation Huang 2020.

## Challenge

I decided to face the challenge to build a new image classifier to detect COVID by xray exams, considering that new kinds of diagnose would be too helpfull to relieve the health public systems that are dealing with a huge number of tests requests, also it was a good opportunity to put in pratice some skills learned on my last completed courses.

## Dataset

The dataset used in these notebooks is available at [Kaggle](https://www.kaggle.com/) plataform by accessing this [link](https://www.kaggle.com/tawsifurrahman/covid19-radiography-database).
The dataset was created by a team of researchers from Qatar University, Doha, Qatar and the University of Dhaka, Bangladesh along with their collaborators from Pakistan and Malaysia in collaboration with medical doctors have created a database of chest X-ray images for COVID-19 positive cases along with Normal and Viral Pneumonia images. At the current moment that this project was developed, in the last release there are 219 COVID-19 positive images, 1341 normal images and 1345 viral pneumonia images. We will continue to update this database as soon as we have new x-ray images for COVID-19 pneumonia patients.

## The project

Before build the new model architecture and fitting it, the earlier steps was to analyse the image dataset that I have on hands, visualizing some images of the three possible pacient conditions (COVID-10, normal and pneumonia) and checking the pixels intensity distribution that affects the training model.

(/Screenshot (26).png)
