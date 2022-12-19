유데미에서 다양한 강의들을 공부하며 나만의 것으로 하고자 정리하였다.

[1. ANN](#ann)

[2. CNN](#cnn)

[3. RNN](#rnn)

[4. SOM](#som)
* * *
# ANN
### 은행의 데이터 세트

고객들의 비상적으로 높은 이탈률을 목격하여 문제가 무엇이고 해결가능한지 알아보자.

![dsg](https://user-images.githubusercontent.com/118944645/208113523-321b4a96-776c-444b-af27-076e57ef2336.png)

독립변수: 행 번호, 고객 번호, 성(姓), 신용점수, 국가(프랑스, 스페인, 독일), 성(性), 근무기간, 계좌 잔고, 이용하는 상품, 신용카드 보유 여부, 활성 고객여부, 예상 급여

반응변수: 은행 이탈 여부 이탈: 1 아님: 0
* * *
# CNN
### 개와 강아지 분류하기

CNN은 데이터의 특징을 추출하여 특징들의 패턴을 파악하는 구조로 정보추출, 문장분류, 얼굴인식 등의 분야에서 사용한다.

![cat_or_dog_1](https://user-images.githubusercontent.com/118944645/208114637-d5a8ebf6-cf86-458c-a316-b813286eb91c.jpg)

8000개의 사진을 분류하는 훈련을 시킨 후 위의 사진을 보여주고 개인지 고양이인지 평가를 해본다.
* * *
# RNN
### 구글 주가를 예측하기

미래를 예측하기는 어렵지만 상승과 하락 추세를 예측해본다.

LSTM을 만들기, 드롭아웃 정규화를 통해 과적합을 없애보려고 한다.

![afs](https://user-images.githubusercontent.com/118944645/208302281-08b94e67-808b-4937-b440-c06d04cb2f4e.png)

![zvx](https://user-images.githubusercontent.com/118944645/208302305-b3e10a7d-9f5e-4378-b1f9-193041ceedb1.png)


4년 데이터 2017넌 1월 주가를 예측 해본다. 예측값과 실제 1월 주가를 비교해보자.
* * *
# SOM
### 은행데이터를 보고 잠재적 사기를 저지르는 고객을 추출하기

기존 ANN을 이용하여 이진수인 Class 종속변수를 통해 여부를 찾는게 아닌

비지도학습인 SOM을 통해 예측해본다.

![123](https://user-images.githubusercontent.com/118944645/208428996-2d57cc2b-898e-4b9f-81e9-f7c0d3b6b062.png)

15개의 뉴런을 통해 딥러닝을 실행하여

뉴런 사이의 유클리드 거리를 계산 후 동떨어진 뉴런을 찾아 사기꾼인 것을 찾아낸다.

![dwq](https://user-images.githubusercontent.com/118944645/208429969-60b1cff9-0c54-4679-a919-8912c5f26fc4.png)

2차원의 그리드에 최초 위닝 노드를 표기하고 각 위닝 노드마다 가장 중요한 정보인 평균 뉴런 거리를 볼 수 있다.

MID는 특정 위닝 노드와 주변의 이웃 위닝 노드 간의 평균거리를 뜻한다. 이웃간의 반지름을 뜻하는 sigma를 사용한다.

즉, MID가 클수록 위닝노드와 이웃 간의 거리가 멀어진다. 더 많은 위닝노드가 동떨어진 노드, 곧 아웃라이어(사기꾼)가 된다.

이런 방법으로 아웃라이어를 감지 뉴런마다 MID를 구하고 가장 큰 MID를 가진 위닝 노드를 가져온다.

숫자 대신 색깔로 사용 MID에 가까울소록 흰색으로 표현하였다.

또한, SOM에서 그치지 않고 ANN을 하는 비지도학습에서 지도학습까지 연결해서 부정 행위를 저지를 가능성을 예측을 해보는 실험을 한다.
