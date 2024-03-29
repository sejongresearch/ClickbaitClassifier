Clickbait Classsifier
=====================  

진행 상황(~5/31)
---------------

+ **계획 변경**
  - 기존 참고 논문 내용 중 특징 추출 부분에서 큰 어려움이 있었음 -> 모델 완성이 어렵다고 팀원 모두 판단
  - 같은 주제(Fake news)지만 CNN모델을 이용한 [프로젝트](https://github.com/2alive3s/Fake_news/blob/master/%5BJIPS%5DFake%20news%20detection%20using%20deep%20learning.pdf) 발견
  - 위 프로젝트 모델의 베이스인 Yoon Kim(2014)의 CNN에 대한 참고 할 수 있는 자료가 매우 많다는 것을 확인
  - 또한 위의 깃헙에서 10만개의 뉴스 기사 크롤링 데이터를 공유하고 있어 데이터 수집에 대한 부담을 덜 수 있다고 판단
  - 팀원 모두 기존 모델을 포기하고 위의 방법을 따라하기로 결정

+ **역할 분담(~5/31)**
  - 황정현 : Yoon Kim의 CNN 모델 공부, 깃헙 관리 및 중간보고서 작성
  - 서예진 : Yoon Kim의 CNN 모델 공부, 참고 프로젝트의 affine_attentive_sim 주석 달기 및 버그 잡기
  - 이현지 : Yoon Kim의 CNN 모델 공부, 참고 프로젝트의 affine 코드 주석 달기 및 버그 잡기
  - 최지연 : Yoon Kim의 CNN 모델 공부, 참고 프로젝트의 affine_bilstm 코드 주석 달기 및 버그 잡기
  - 김재형 : Yoon Kim의 CNN 모델 공부, 참고 프로젝트의 train 코드 주석 달기

+ [**데이터셋**](https://github.com/2alive3s/Fake_news/tree/master/data)
  - 3만 개의 뉴스 기사 크롤링 데이터(위 깃헙의 데이터셋 이용) 

+ **모델 조사**
  - Yoon Kim(2014)의 [**Convolutional Neural Networks for Sentence Classification**](https://arxiv.org/pdf/1408.5882.pdf)
    * CNN을 텍스트 처리에 응용한 연구
    * 해당 논문에서는 영화 댓글 감정 분석에 적용 
  - 워드 임베딩 모델 (**Word2Vex, FastText**)
    * 단어를 벡터로 표현하는 대표적인 방법
  
+ **코드 분석 및 개발 환경 구축**
  - 기존 프로젝트에서 CNN을 활용해 작성한 affine 관련 코드 3개와 train 코드에 대해 직접 주석을 달며 분석 및 오류 수정(진행 중)
  - KoNLPy 한국어 처리 패키지 및 FastText 설치

진행 계획
---------
+ ~~**데이터 로드 및 전처리(~6/7)**~~
  - ~~csv 파일을 github에서 불러오기~~
  - ~~Word2Vex와 FastText를 이용하여 데이터 전처리~~

+ ~~**모델 제작(~6/9)**~~
  - ~~6월 첫째 주까지 코드 분석 과정에서 발견한 오류 수정을 통해 모델 제작하여 깃허브에 코드 업로드~~
  
+ **모델 성능 개선(~6/16)**
  - 6월 둘째 주까지 기존 프로젝트의 낮은 성능을 해결하기 위해 layer를 더 쌓기 등 여러 방법 시도 하여 정확도 개선 및 프로젝트 
  완료


진행 상황(~6/9)
---------------

+ **데이터 로드 및 전처리**
  - 100개의 기사로 이루어진 검증용 csv파일을 읽어서 형태소 분석 및 라벨링 성공(6/6)
  - 단어를 벡터로 표현해 주는 fasttext를 이용하여 라벨링된 데이터를 임베딩 성공(6/6)
  - 3만개의 학습용 데이터를 읽어서 전처리 성공(6/8)
  
+ **모델 제작**
  - 기존 프로젝트의 CNN 모델 코드와 학습 코드를 분석 및 정리하여 colab 개발환경에 맞도록 버그 수정(6/7)
  - 임베딩된 데이터를 학습 코드에 넣어 loss와 accuracy가 정상적으로 출력 되는 것을 확인(6/7)
  
+ **역할 분담**
  - 데이터 로드 및 전처리(황정현)
  - 모델 제작 : 코드 분석 및 정리, 버그 수정(이현지, 최지연, 서예진)
  

진행 계획(~6/16)
---------------

+ **모델 성능 개선(~6/14)**
  - 모델의 낮은 성능을 해결하기 위해 수업 시간에 배운 지식을 최대한 활용하여 layer를 더 쌓기 등 여러 방법 시도 하여 정확도 개선 및 프로젝트 
  완료
  - 모델 제작 이외에 완성도를 위해 추가적으로 해야할 일 고려하여 업데이트하기
  
프로젝트 완료(~6/23)
-------------------
+ **3가지 모델을 이용하여 분류기 제작**
  - CNN -> Accuracy : 0.47
  - APS -> Accuracy : 0.49
  - LSTM -> Accuracy : 0.41
  
+ **모델 성능 개선 실패**
  - 학습데이터 오버피팅문제 해결 실패 : 적절한 validation 찾기 실패
  - Layer 더 쌓기 실패 : colab의 RAM 용량 초과
  - 각종 파라미터 조정 : 큰 영향 없었음

+ **논문 및 발표자료**
  - [논문](https://github.com/sejongresearch/ClickbaitClassifier/blob/master/%EA%B8%B0%EB%A0%88%EA%B8%B0%ED%86%B5%20%EB%85%BC%EB%AC%B8.pdf)
  - [발표자료](https://github.com/sejongresearch/ClickbaitClassifier/blob/master/%EA%B8%B0%EB%A0%88%EA%B8%B0%ED%86%B5%20ppt.pptx)
