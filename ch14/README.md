머신 러닝 교과서 2판


## 14장 - 텐서플로의 구조 자세히 알아보기


### 목차

- 텐서플로의 주요 특징
- 텐서플로의 계산 그래프: 텐서플로 v2로 이전하기
  - 계산 그래프 이해하기
  - 텐서플로 v1.x에서 그래프 만들기
  - 텐서플로 v2로 이전하기
  - 입력 데이터를 모델에 주입하기: 텐서플로 v1.x 스타일
  - 입력 데이터를 모델에 주입하기: 텐서플로 v2 스타일
  - 함수 데코레이터로 계산 성능 높이기
- 모델 파라미터를 저장하고 업데이트하기 위한 텐서플로 변수 객체
- 자동 미분과 GradientTape을 사용해 그레이디언트 계산하기
  - 훈련 가능한 변수에 대한 손실의 그레이디언트 계산하기
  - 훈련하지 않는 변수에 대한 그레이디언트 계산하기
  - 여러 개의 그레이디언트 계산하기
- 케라스 API를 사용해 간단하게 일반적인 구조 구현하기
  - XOR 분류 문제 풀어보기
  - 케라스 함수형 API로 유연성이 높은 모델 만들기
  - 케라스의 Model 클래스 기반으로 모델 만들기
  - 사용자 정의 케라스 층 만들기
- 텐서플로 추정기
  - 특성 열 사용하기
  - 사전에 준비된 추정기로 머신 러닝 수행하기
  - 추정기를 사용해 MNIST 손글씨 숫자 분류하기
  - 케라스 모델에서 추정기 만들기
- 요약

### 코드 사용 방법 안내

이 책의 코드를 사용하는 가장 좋은 방법은 주피터 노트북(`.ipynb` 파일)입니다. 주피터 노트북을 사용하면 단계적으로 코드를 실행하고 하나의 문서에 편리하게 (그림과 이미지를 포함해) 모든 출력을 저장할 수 있습니다.

![](../ch02/images/jupyter-example-1.png)

주피터 노트북은 매우 간단하게 설치할 수 있습니다. 아나콘다 파이썬 배포판을 사용한다면 터미널에서 다음 명령을 실행하여 주피터 노트북을 설치할 수 있습니다:

    conda install jupyter notebook

다음 명령으로 주피터 노트북을 실행합니다.

    jupyter notebook

브라우저에서 윈도우가 열리면 원하는 `.ipynb`가 들어 있는 디렉토리로 이동할 수 있습니다.

**설치와 설정에 관한 더 자세한 내용은 1장의 [README.md 파일](../ch01/README.md)에 있습니다.**

**(주피터 노트북을 설치하지 않았더라도 깃허브에서 [`ch14_part1.ipynb`](https://github.com/rickiepark/python-machine-learning-book-3rd-edition/blob/master/ch14/ch14_part1.ipynb), [`ch14_part2.ipynb`](https://github.com/rickiepark/python-machine-learning-book-3rd-edition/blob/master/ch14/ch14_part2.ipynb), [`ch14_part3.ipynb`](https://github.com/rickiepark/python-machine-learning-book-3rd-edition/blob/master/ch14/ch14_part3.ipynb)을 클릭해 노트북 파일을 볼 수 있습니다.)**.

코드 예제 외에도 주피터 노트북에는 책의 내용에 맞는 섹션 제목을 함께 실었습니다. 또한 주피터 노트북에 원본 이미지와 그림을 포함시켰기 때문에 책을 읽으면서 코드를 쉽게 따라할 수 있으면 좋겠습니다.

![](../ch02/images/jupyter-example-2.png)