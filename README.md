# GalaxyZoo_Image_Classification
This repository contains all the trial and error versions for the Rlag1998/image_classification project

## Introduction

Galaxy classification is a complex system. In basic terms there are 4 different categories: ellipticals, spirals, lenticulars, and irregulars. The final nomenclature and classification of a galaxy depends on the brightness of it, the existance of the bulge, number of arms, whether there is structure or is it smooth, and its shape. In this project, we do not delve too deep into the specifics of it but it is important to understand main properties of the system. Figure 1, Hubble-De Vaucouleurs diagram, describes the main way galaxies are usually labelled.

![image](https://user-images.githubusercontent.com/119504274/225613215-45396bf5-8720-4508-84b2-4ce3debceb96.png)
Figure 1: The diagram may suggest progression from elliptical galaxies to spiral galaxies, however, the reality of galaxy evoltion is far more complex. (Image credit: Antonio Ciccolella/M. De Leo)

The Galaxy Zoo astronomy project (https://www.zooniverse.org/projects/zookeeper/galaxy-zoo/) collects data by inviting individuals to answer questions in a decision tree based on an astronomical image of a galaxy. The questionnaire in the form of a decision tree can be seen below (Figure 2). Humans select the attributes they can see in the image and their answers are aggregated, along with some error analysis, to find the final morphological classification of a galaxy.

![image](https://user-images.githubusercontent.com/119504274/225607939-fa9d1b0f-ae32-41ac-bac4-0189e7a53730.png)
Figure 2: The Galaxy Zoo 2 decision tree with 11 questions and 37 answers (Hart et al., 2016)

In the dataset, there are following features:
* The unique Galaxy ID
* The final classification
* Fraction of the votes for the each answer in the each question, so there were 11 questions with a total of 37 possible answers

Galaxy Zoo has had multiple data releases, in this project the table from the Galaxy Zoo 2 (Hart et al., 2016) was used. There were 2 ways to classify galaxies in this project. One method was to use the final classification and label each image with a more general class. For example, as the final nomenclature was based, also, on the number of arms and brightness, the galaxy was just said to be a spiral with arms or no arms. Another method used was to take the fraction of votes and perform a regression analysis and predict the fractions which could be used to create a final nomenclature for each image in the dataset. This method would enable for the model to behave like a hunman eye which is the baseline. However, ideally the model should be performing even better than the human eye.

In the following sections these 2 methods and models are explored in more detail.
