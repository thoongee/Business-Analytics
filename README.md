# Business-Analytics Term project
TOPIC : A Proposal on Optimal Location Choice of animal burial facilities: Focusing on Seoul Area


## Topic description


#### Problem
- Demand for pet funerals is increasing, but supply is not available
- Pet carcasses are classified as waste and it is illegal to bury them on land which is not their own land

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
<img src="https://user-images.githubusercontent.com/94193480/205539829-3f95345d-5c9a-4c02-9bb5-96948c0af919.png" width="300" height="280"/><img width="350" alt="image" src="https://user-images.githubusercontent.com/94193480/205582257-bade1d15-db17-4397-8f36-607a987e3eb7.png">


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
- 
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

## Limitation
- We cannot reflect the various factors related to the surrounding environment encountered when approaching the funeral facility
- We did not consider the budget issues and project performance capabilities of districts of Seoul

## Getting Started
download all files and upload it on your colab notebook

### Environment
[Google Colab notebook](https://colab.research.google.com/)

### Code we made..
1. Preprocessing : result is preprocessing_data.xlsx
2. EDA : see what preprocessing data looks like
3. Clustering : Kmeans, GMM, Hierarchical clustering, Kmedoids, calculate silhoutte coefficient
4. Make_training_dataset : make target column using Kmeans clustering & drop some 
5. Make_test_dataset : make test dataset which each row is gu
6. Classification : find proper district to build animal burial facility

### Data we made..
- basic_data
  - number of pet household
- dong_size
  - size of each dong
- animal_household
  - merge basic_data, dong_size and calculate density of pet household
- animal_hospitalpharmacy
  - merge animal hosiptal.xlsx and animal pharmacy.xlsx using excel file. And each file is downloaded from 'Seoul Open Data Plaza'
- animal_hospitalpharmacy_result2
  - change from instance based on legal dong(법정동) to administartive dong (행정동) and count the number of animal hospitals and pharmacies of each dong
- animal_shelter 
  - number of animal shelter, animal death/euthanasia
- preprocessing_data
  - result of preprocessing
- seoul_geo.json
  - using EDA to see map of seoul
- train
  - train dataset used in classificaiton
- test
  - test dataset used in classification
