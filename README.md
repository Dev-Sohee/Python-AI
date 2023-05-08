# :pushpin: 중고차 가격 예측하기

</br>

## 1. 기간 & 참여 인원
- 2023년 4월 23일 ~ 5월 13일
- 이소희, 신경훈, 안은정, 정은서, 윤아람, 김준구 총 6인 

</br>

## 2. 사용 기술
  - Pandas
  - Numpy
  - Matplotlib
  - Seaborn
  - Sklearn
  - Linear Regression
  - Random Forest

</br>

## 3. Introduction
- Data:  https://www.kaggle.com/datasets/avikasliwal/used-cars-price-prediction


- Kaggle에서 주최한 "인도 중고차 예측하기" 데이터셋의 train data를 바탕으로 중고차 가격 예측하기


- **6019** rows and **14** columns 


</br>

## 4. Data Processing


### 4.1. 데이터 살펴보기
'''python
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 6019 entries, 0 to 6018
Data columns (total 14 columns):
 #   Column             Non-Null Count  Dtype  
---  ------             --------------  -----  
 0   Unnamed: 0         6019 non-null   int64  
 1   Name               6019 non-null   object 
 2   Location           6019 non-null   object 
 3   Year               6019 non-null   int64  
 4   Kilometers_Driven  6019 non-null   int64  
 5   Fuel_Type          6019 non-null   object 
 6   Transmission       6019 non-null   object 
 7   Owner_Type         6019 non-null   object 
 8   Mileage            6017 non-null   object 
 9   Engine             5983 non-null   object 
 10  Power              5983 non-null   object 
 11  Seats              5977 non-null   float64
 12  New_Price          824 non-null    object 
 13  Price              6019 non-null   float64
 '''


### 4.2. 컬럼명 바꾸기
![](https://zuminternet.github.io/images/portal/post/2019-04-22-ZUM-Pilot-integer/flow_vue.png)

- **URL 정규식 체크** :pushpin: 
- (https://github.com/Integerous/goQuality/blob/b587bbff4dce02e3bec4f4787151a9b6fa326319/frontend/src/components/PostInput.vue#L67)
  - Vue.js로 렌더링된 화면단에서, 사용자가 등록을 시도한 URL의 모양새를 정규식으로 확인합니다.
 

### 4.3. 브랜드명 추출




### 4.4. Mileage, Engine, Power 단위 
- 단위 통합 후 단위 제거, 숫자형으로 바꾸기

  


### 4.5. 이상값 및 결측값 제거

![](https://zuminternet.github.io/images/portal/post/2019-04-22-ZUM-Pilot-integer/flow_repo.png)

  

### 4.6. One-Hot Encoding


### 4.7. Heatmap
![](https://zuminternet.github.io/images/portal/post/2019-04-22-ZUM-Pilot-integer/flow_repo.png)


</div>
</details>

</br>

## 5. Machine Learning
### 5.1. Linear Regression
Result


### 5.2. Random Forest


### 5.3. Decision Tree Regressor


### 5.2. MLP Regressor

</br>


## 6. Conclusion
- 제일 적합했던 모델:



