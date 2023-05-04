# :pushpin: 중고차 가격 예측하기
> https://www.kaggle.com/datasets/avikasliwal/used-cars-price-prediction

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



## 4. Data Processing
데이터 전처리 과정


### 4.1. 데이터 살펴보기
![](https://zuminternet.github.io/images/portal/post/2019-04-22-ZUM-Pilot-integer/flow1.png)

### 4.2. 컬럼명 바꾸기
![](https://zuminternet.github.io/images/portal/post/2019-04-22-ZUM-Pilot-integer/flow_vue.png)

- **URL 정규식 체크** :pushpin: 
- (https://github.com/Integerous/goQuality/blob/b587bbff4dce02e3bec4f4787151a9b6fa326319/frontend/src/components/PostInput.vue#L67)
  - Vue.js로 렌더링된 화면단에서, 사용자가 등록을 시도한 URL의 모양새를 정규식으로 확인합니다.
 

### 4.3. 브랜드명 추출

![](https://zuminternet.github.io/images/portal/post/2019-04-22-ZUM-Pilot-integer/flow_controller.png)

- **요청 처리** :pushpin: [코드 확인](https://github.com/Integerous/goQuality/blob/b2c5e60761b6308f14eebe98ccdb1949de6c4b99/src/main/java/goQuality/integerous/controller/PostRestController.java#L55)
  - Controller에서는 요청을 화면단에서 넘어온 요청을 받고, Service 계층에 로직 처리를 위임합니다.


### 4.4. Mileage, Engine, Power 단위 
- 단위 통합 후 단위 제거, 숫자형으로 바꾸기

![](https://zuminternet.github.io/images/portal/post/2019-04-22-ZUM-Pilot-integer/flow_service1.png)

- **Http 프로토콜 추가 및 trim()** :pushpin: [코드 확인]()
  


### 4.5. 이상값 및 결측값 제거

![](https://zuminternet.github.io/images/portal/post/2019-04-22-ZUM-Pilot-integer/flow_repo.png)

- **컨텐츠 저장** :pushpin: [코드 확인]()
  - URL 유효성 체크와 이미지, 제목 파싱이 끝난 컨텐츠는 DB에 저장합니다.
  - 저장된 컨텐츠는 다시 Repository - Service - Controller를 거쳐 화면단에 송출됩니다.

</div>
</details>

</br>

## 5. Machine Learning
### 5.1. Linear Regression
Result

### 5.2. Random Forest



## 6. Conclusion

