Clickbait Classsifier
=====================  

진행 상황
--------

+ **계획 변경**
  - 기존 참고 논문 내용 중 특징 추출 부분에서 큰 어려움이 있어, 같은 주제지만 [다른 방법론](https://github.com/2alive3s/Fake_news/blob/master/%5BJIPS%5DFake%20news%20detection%20using%20deep%20learning.pdf)으로 변경
  - [역할 분담](https://github.com/rjhwang08/Clickbait-Classsifier/issues/2) 재조정

+ [**데이터셋**](https://github.com/2alive3s/Fake_news/tree/master/data)
  - 10만 개의 뉴스 기사 크롤링 데이터(위 깃헙의 데이터셋을 이용하되, 시간적 여유 시 test 데이터는 자체 가공) 

+ **모델 조사**
  - Yoon Kim(2014)의 [**Convolutional Neural Networks for Sentence Classification**](https://arxiv.org/pdf/1408.5882.pdf)
    * CNN을 텍스트 처리에 응용한 연구
  - 워드 임베딩 모델 (**Word2Vex, FastText**)
    * 단어를 벡터로 표현하는 대표적인 방법
  
+ **코드 분석 및 개발 환경 구축**
  - 기존 프로젝트에서 CNN을 활용해 작성한 affine 관련 코드 3개와 train 코드에 대해 직접 주석을 달며 분석 및 오류 수정
  - KoNLPy 한국어 처리 패키지 및 FastText 설치

진행 계획
---------
+ **데이터 로드 및 전처리**
  - csv 파일을 github에서 불러오기
  - Word2Vex와 FastText를 이용하여 데이터 

+ **모델 제작**
  - 6월 첫째 주까지 코드 분석 과정에서 발견한 오류 수정을 통해 모델 제작
  
+ **성능 개선**
  - 6월 둘째 주까지 기존 프로젝트의 낮은 성능을 해결하기 위해 layer를 더 쌓기 등 여러 방법 시도 하여 정확도 개선 및 프로젝트 
  완료
