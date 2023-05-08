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


- ***6019*** rows and ***14*** columns 


</br>

## 4. Data Processing


### 4.1. 데이터 살펴보기


<img width="883" alt="data" src="https://user-images.githubusercontent.com/120240261/236746713-df23f1b3-63f0-4158-b9e8-da0cdc5653f5.png">




### 4.2. 컬럼명 바꾸기
```python
df_data.columns = ['Brand', 'Location', 'Year', 'Driven', 'Fuel', 'Trans', 'Owner', 'Mileage', 'Engine', 'Power', 'Seats', 'Price']
```



### 4.3. 브랜드명 추출
```python
df_data['Brand'] = df_data.Brand.str.split(' ').str[0]
```



### 4.4. Mileage, Engine, Power 단위 
- 단위 제거

```python
df_data['Mileage'] = df_data.Mileage.str.split(' ').str[0]
df_data['Engine'] = df_data.Engine.str.split(' ').str[0]
df_data['Power'] = df_data.Power.str.split(' ').str[0]
```
  
  

- 숫자형 변환
```python
df_data['Mileage'] = pd.to_numeric(df_data['Mileage'])
```



- Fuel_Type = 'CNG', 'LPG' -> Mileage 단위 km/kg
- Fuel_Type = 'Diesel', 'Petrol' -> Mileage 단위 kmpl
- 'CNG', 'LPG'에 각각 1.64, 1.3을 곱해서 kmpl로 단위 통합
```pyhton
df_data['Mileage'][df_data['Fuel'] == 'CNG'] = df_data[df_data['Fuel'] == 'CNG']['Mileage']*1.64
df_data['Mileage'][df_data['Fuel'] == 'LPG'] = df_data[df_data['Fuel'] == 'LPG']['Mileage']*1.3
```


### 4.5. 이상값 및 결측값 제거

- ['Driven'] 컬럼에 이상값 한 개
<img src="https://user-images.githubusercontent.com/120240261/236746743-ca32f490-93e2-4dd0-b5b4-92aeb68708d7.png" width="40%" alt="driven1" height="40%">  


- 이상값 제거 후
<img src="https://user-images.githubusercontent.com/120240261/236748667-dd681ab3-b2a7-4bec-b220-15405c8b6212.png" width="40%" alt="driven2" height="40%">


  

### 4.6. One-Hot Encoding

```python
df_data = pd.get_dummies(df_data, columns = ['Brand', 'Location', 'Fuel', 'Trans', 'Owner'])
```


### 4.7. Heatmap
- 모든 변수 포함

<img src="https://user-images.githubusercontent.com/120240261/236746753-0c98b960-9a87-443f-aa6d-c94eaf2c6ecd.png" alt="heatmap1" width="80%" height="80%">







- 주요 변수 포함

<img src="https://user-images.githubusercontent.com/120240261/236746756-6ceb91cc-ea50-473b-9f84-79d766c3d748.png" alt="heatmap2" width="60%" height="60%">




</div>
</details>

</br>

## 5. Machine Learning


### 5.1. Linear Regression


<img src="https://user-images.githubusercontent.com/120240261/236746757-7cda6471-e2aa-455f-b07a-0da901b078ea.png" alt="linear regression" width="70%" height="70%">



### 5.2. Random Forest


<img src="https://user-images.githubusercontent.com/120240261/236746762-b1719d64-0f9d-43f7-a7bf-95873be5d98d.png" alt="random forest" width="70%" height="70%">




### 5.3. Decision Tree Regressor


<img src="https://user-images.githubusercontent.com/120240261/236746764-980b3eb5-f981-43e6-8648-942a12894a2b.png" alt="decision tree" width="50%" height="50%">




### 5.2. MLP Regressor


<img src="https://user-images.githubusercontent.com/120240261/236746767-1a2848dc-7a7b-4110-a9ab-3d44c38b9da7.png" alt="MLP regressor" width="50%" height="50%">




</br>


## 6. Conclusion
- 제일 적합했던 모델:



