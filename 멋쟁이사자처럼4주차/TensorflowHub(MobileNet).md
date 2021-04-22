# TensorFlow Hub

 : 재사용 가능한 모델을 쉽게 이용할 수 있는 라이브러리
 
## MobileNet 버전 2

 - ResNet-50(2560만 개), ResNet-12(6000만 개)에 비해 상대적으로 적은 파라미터 수를 가지고 있다.
 
 - ImageNet 데이터로 학습
 
  : ImageNet에는 1천 종류의 이미지 존재, 만약 어떠한 것도 분류되지 않는다면은 인덱스 0 반환(background 해당)
  
 -> skip connection: 깊이가 깊어지는 신경망은 학습이 어려운데 중간에 왜곡되거나 연산적 병목현상이 일어날 가능성이 높아 일정부분 건너뛰어 앞으로 가주는 방식이다.
 
 -> Depth-Wise Separable Convolution: 네트워크 경량화를 해야한다면 깊이를 줄이는 것보다 신경망의 height, width를 줄이는게 좋다.
  
## ImageNetV2

 : ImageNet의 데이터 중 일부만을 모아놓은 데이터
 
 -> 아마존 메키니컬 테크를 이용해 다수의 참가자에게서 클래스 예측값을 받아 선별한 데이터
 
 (ex. MobileNetV2.ipynb)
 
