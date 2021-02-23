### personal_project_for_study with AIboostcamp U STAGE PEERS
-------------
#### 프로젝트 명 : 레드벨벳 이미지 분류 모델 학습
#### 모델 : CNN 
#### 성능 평가 : K-FOLD cross validation (단순 교차 검증)
#### 데이터 : 각 멤버별 이미지 데이터를 크롤링, 얼굴 crop 전처리 함
* 크롤링과 crop(OpenCV 사용) 포함되어 있지 않음.
-------------
#### 학습 세팅
* CNN 구조 매우 형편없고 얕음.

  학습 데이터가 적고, K-FOLD 를 적용해보는 것이 목표라(변명) 더 나은 구조로 설계하지 않았음.
  
  다른 동료들의 경우 resNet 과 같은 모델을 사용했는데 학습 결과 50% 이상 Accuracy 를 보였음.
* K-FOLD : 10
* EPOCH : 30
* 학습 환경 : Google Colab, 

#### 결과 (output)
* 평균 정답률 : 31%
* 
