# A Proposal on Optimal Location Choice of animal burial facilities: Focusing on Seoul Area

## Project description
#### Problem
- Demand for pet funerals is increasing, but supply is not available
- Pet carcasses are classified as waste and it is illegal to bury them on land which is not their own land

#### Goal
- Propose location in areas where animal burial faility's demand is expected to be high

#### Result
- Density of animal hospitals & pharmacies is a feature that greatly affects the installation of funeral facilities
- Optimal districts(gu) are Seongbuk-gu, Dongaemun-gu, Mapo-gu, Jung-gu, Gwangjin-gu, Dongjak-gu, Gwanak-gu, Songpa-gu

## Getting Started
Please download all files, and upload .ipynb files in your colab notebook
#### Environment
Google Colab notebook






#### Preprocessing
- Extracting the density of pet household, animal hospital and pharmacy, animal shelter, animal death/euthanasia
- 



## Code we made..
1. Preprocessing: result is preprocessing_data.xlsx
2. EDA : see what preprocessing data looks like
3. Clustering : Kmeans, GMM, Hierarchical clustering, Kmedoids, calculate silhoutte coefficient
4. Make_training_dataset: make target column using Kmeans clustering & drop some 
5. Make_test_dataset: make test dataset which each row is gu
6. Classification : find proper district to build animal burial facility


## Data
#### Data we get
![image](https://user-images.githubusercontent.com/94193480/205491656-aff76e9e-698e-4d11-976d-d0f687fc6fea.png)

#### Data we made..
- basic_data : number of 동 별 반려가구수
- dong_size : 동 면적
- animal_household : basic_data + dong_size + 반려가구 밀도
- animal_hospitalpharmacy : merge animal hosiptal.xlsx and animal pharmacy.xlsx using excel file. And each file is downloaded from 서울열린데이터광장.
- animal_hospitalpharmacy_result : 각 동 별 동물병원약국 개수 
- animal_hospitalpharmacy_result2 : 법정동 -> 행정동

- animal_shelter : number of animal shelter동 별 유기동물 보호 현황 (인도, 입양분양, 폐사안락사 수)
- preprocessing_data : result of preprocessing which have 서울시 동,가구원수,서울시 구,구별 가구수,	반려동물 비율,반려동물 가구수 구,반려동물 가구수 동,면적,	반려동물 가구밀도,	폐사안락사수, 보호소 수,보호소 밀도,폐사안락사 비율,동물병원약국개수,동물병원약국 밀도 columns

- seoul_geo.json : using EDA to see map of seoul
- train : train dataset for use in classificaiton
- test : test dataset for use in classification
