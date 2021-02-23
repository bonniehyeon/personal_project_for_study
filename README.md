### personal_project_for_study with AIboostcamp U STAGE PEERS
-------------
#### *프로젝트 명 : 레드벨벳 이미지 분류 모델 학습
#### *모델 : CNN 
#### *성능 평가 : K-FOLD cross validation (단순 교차 검증)
#### *데이터 : 각 멤버별 이미지 데이터를 크롤링, 얼굴 crop 전처리 함
* 크롤링과 crop(OpenCV 사용) 포함되어 있지 않음.
-------------
#### 학습 세팅
* CNN 구조 매우 형편없음

  학습 데이터가 적고, K-FOLD 를 적용해보는 것이 목표라(변명) 더 나은 구조로 설계하지 않았음.
  
  다른 동료들의 경우 resNet 과 같은 모델을 사용했는데 학습 결과 50% 이상 Accuracy 를 보였음.
* K-FOLD : 10
* EPOCH : 30
* 학습 환경 : Google Colab, 

#### 결과 (output)

* 평균 정답률 : 32% 

  <img src="https://user-images.githubusercontent.com/50580028/108875760-d9438f00-7640-11eb-92c2-7c0359bdacd8.png" width="50%" height="50%">

* 각 COLOR BOX는 한번의 K iteration 이 실행되는 동안의 epoch에 따른 loss 값의 변화를 보여준다.

  k 가 새로 실행 될 때마다 다시 학습을 시작함을 확인 할 수 있으며, 전반적으로 모든 데이터에 대해 비슷한 학습 결과를 보이고 있다.
  
  <img src="https://user-images.githubusercontent.com/50580028/108874102-2cb4dd80-763f-11eb-920b-d09101b2044a.png"  width="40%" height="40%">
  
* K-FOLD 의 각 학습 결과를 저장한다.

  <img src="https://user-images.githubusercontent.com/50580028/108874873-f1ff7500-763f-11eb-9d6d-b5707aa0cadb.png"  width="20%" height="20%">
 
#### 추후 개선 과제
* K-FOLD의 각 데이터 SET은 torchvision.datasets.ImageFolder() 와 torch.utils.data.Subset() 을 사용하여 만들었다.

* Custom Dataset으로 구현한다면 TEST DATA 이미지에 다양한 AUGMENTATION 효과를 주어 학습 효과를 늘릴 수 있을 것으로 기대 된다.
  
#### 참고자료
https://github.com/skywalker023/deep_iab

https://www.machinecurve.com/index.php/2021/02/03/how-to-use-k-fold-cross-validation-with-pytorch/


