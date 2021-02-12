# ResNet_KeyFacialPoints

- [Overview](#overview)
- [The problem](#the-problem)
- [Technical Details](#technical-details)
- [Use Cases](#use-cases)
- [Credits](#credits)


## Overview

This is a Coursera project on EmotionAI that I have completed. The project uses deep neural network (DNN) based on Convolutional Neural Networks (CNN) and Residual Blocks (ResNet) for learning the keypoints in face image data. These keypoints can be used to learn and predict human emotions. The course certificate link is given below

[Coursera Certificate](https://www.coursera.org/account/accomplishments/certificate/KQACF3CSLKL8)

## The problem

- Facial Key-Point Detection serves as the basis of Emotional AI applications like detecting customer emotional responses to Ads and Driver Monitering systems.
- In this project I am using a face image dataset to train a DNN to identify the key facial points which are the x- and y- cordinates of points capturing the positions of eyes, nose and lips.
- The dataset is very small with only ~2000 images. So, there is a serious need for doing data augmentation.
- The business direction that I have in mind is actually two-fold. One is directed towards individuals looking for places to eat or even people looking for places to rent based on restaurant types or frequency. The other direction is for corporations/individuals looking to open a new restaurant.

## Technical Details

The grave details of the project are all mentioned in the [notebook](https://github.com/jyotisman-ds/Coursera_Capstone/blob/master/Exploring%20LA%20restaurants.ipynb)

- Location data was obtained from  [here](https://usc.data.socrata.com/dataset/Los-Angeles-Neighborhood-Map/r8qd-yxsr)

- The number of neighborhoods was truncated to 199 using a distance function from the LA central coordinates.

- Two ideas are explored here in detail. One idea is to find the density of restaurants in each neighborhood. This will help anyone trying to open a new restaurant by either avoiding overcrowded areas or alternately could also help finding popular venues for someone looking to avoid competition. The above data also includes the area of each neighborhood in square miles which can be used to compute this density I mentioned. A K-Means clustering technique is then used to segment neighborhoods based on this data.

- Second idea is to explore the kind of restaurants. Here, one can again use clustering but now based on the frequency of occurrence of each restaurant in a neighborhood. Once we find the relevant cluster here, we can then look for its intersection with the clusters found above to fine tune the relevant neighborhood where one wants to open his/her restaurant. A snippet of such a final cluster with all the information included is shown below -

![cluster1](/images/cluster_1.png)

- Figure shows the Cluster labelled as '1'. It plots the number of restaurants in each category from the most common restaurant venues list. On top of that, it also shows how many of them are in low, medium and high density neighborhoods.

## Use Cases



## Credits
A huge shoutout to the Coursera community for hosting the [course](https://www.coursera.org/projects/facial-key-point-detection) and to the course instructor Ryan Ahmed.
