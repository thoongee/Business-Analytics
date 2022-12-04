- basic_data : 동 별 반려가구수
- dong_size : 동 면적
- animal_household : basic_data + dong_size + 반려가구 밀도
- animal_hospitalpharmacy : merge animal hosiptal.xlsx and animal pharmacy.xlsx using excel file. And each file is downloaded from 서울열린데이터광장.
- animal_hospitalpharmacy_result : 각 동 별 동물병원약국 개수 
- animal_hospitalpharmacy_result2 : 법정동 -> 행정동

- animal_shelter : 동 별 유기동물 보호 현황 (인도, 입양분양, 폐사안락사 수)
- preprocessing_data : 서울시 동,가구원수,서울시 구,구별 가구수,	반려동물 비율,반려동물 가구수 구,반려동물 가구수 동,면적,	반려동물 가구밀도,	폐사안락사수, 보호소 수,보호소 밀도,폐사안락사 비율,동물병원약국개수,동물병원약국 밀도

- seoul_geo.json : using EDA to see map of seoul

- train : train dataset for use in logistic regression
- test : test dataset for use in logistic regression