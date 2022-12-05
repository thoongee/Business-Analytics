# Business-Analytics Term project
TOPIC : A Proposal on Optimal Location Choice of animal burial facilities: Focusing on Seoul Area


## Topic description


#### Problem
- Demand for pet funerals is increasing, but supply is not available
- Pet carcasses are classified as waste and it is illegal to bury them on land which is not their own land
<p align="center"><img width="200" alt="image" src="https://user-images.githubusercontent.com/94193480/205587112-56af8046-54e8-40d0-baca-07c02e94f923.png">

#### Goal
- Propose location in areas where animal burial faility's demand is expected to be high
- High animal hospital, high euthanasia rates at animal shelters, and a large number of pet households will be the optimal area for establishing animal burial facilities

#### Data we get
![image](https://user-images.githubusercontent.com/94193480/205491656-aff76e9e-698e-4d11-976d-d0f687fc6fea.png)


#### ➡️ Step : Preprocessing -> EDA -> Clustering -> Classificaiton

## Preprocessing & EDA
#### Preprocessing
- Extracting the density of pet household, animal hospital and pharmacy, animal shelter, animal death/euthanasia
- Making each instance of preprocessing data represents administrative dong (행정동)

#### EDA
- Seeing distribution of each features using bar graph and line graph
- Visualizing Seoul map to see how data distributed in Seoul

<img src="https://user-images.githubusercontent.com/94193480/205539829-3f95345d-5c9a-4c02-9bb5-96948c0af919.png" width="280" height="280"/><img width="350" alt="image" src="https://user-images.githubusercontent.com/94193480/205582257-bade1d15-db17-4397-8f36-607a987e3eb7.png">


## Clustering
#### Choose optimal clustering model
- K-means have highest sillhouette score than GMM, Hierarchical clustering and K-medoids

#### Make target label
- Clusters with average of all feature values >=0 is set to target as 1
- 1 == good to install an animal burial facility

## Classification

#### Purpose : Predict good district to install animal burial facility

#### Make train & test dataset
- trian dataset : Drop variables of VIF >= 10
- test dataset : Each instance is distirct of seoul
#### Find best model & best parameter
- Decision Tree's f1 score is higher than Logistic regression, Random Forest, KNN
- best parameter
  - criterion : gini
  - max_depth : 6
  - min_sampels_leaf : 4

## Result

#### Solutions of the problem
- Density of animal hospitals & pharmacies is a feature that greatly affects the installation of funeral facilities
- Optimal districts(gu) are Seongbuk-gu, Dongaemun-gu, Mapo-gu, Jung-gu, Gwangjin-gu, Dongjak-gu, Gwanak-gu, Songpa-gu

<img width="400" alt="image" src="https://user-images.githubusercontent.com/94193480/205583005-fadbcdd2-06fa-4bf1-b05e-2a5f75d36de9.png"> <img width="280" alt="image" src="https://user-images.githubusercontent.com/94193480/205582976-c4b4f67e-5eb1-428f-8e69-e6d8c4077f64.png"> 

## Limitation
- We cannot reflect the various factors related to the surrounding environment encountered when approaching the funeral facility
- We did not consider the budget issues and project performance capabilities of districts of Seoul

## Getting Started
download all files and upload it on your colab notebook

### Environment
[Google Colab notebook](https://colab.research.google.com/)

#### Code_readme & Data_readme is in each folder !
