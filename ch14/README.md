머신 러닝 교과서 2판


## 14장 - 텐서플로의 구조 자세히 알아보기


### 목차

- The key features of TensorFlow
  - TensorFlow's computation graphs: migrating to TensorFlow v2
     - Understanding computation graphs
     - Creating a graph in TensorFlow v1.x
     - Migrating a graph to TensorFlow v2
     - Loading input data into a model: TensorFlow v1.x style
     - Loading input data into a model: TensorFlow v2 style
  - Improving computational performance with function decorators
  - TensorFlow Variable objects for storing and updating model parameters
  - Computing gradients via automatic differentiation and GradientTape
     - Computing the gradients of the loss with respect to trainable variables
     - Computing gradients with respect to nontrainable tensors
     - Keeping resources for multiple gradient computations
- Simplifying implementations of common architectures via the Keras API
  - Solving an XOR classification problem
  - Making model building more flexible with Keras' functional API
  - Implementing models based on Keras' Model class
  - Writing custom Keras layers
- TensorFlow Estimators
  - Working with feature columns
  - Machine learning with pre-made Estimators
  - Using Estimators for MNIST handwritten digit classification
  - Creating a custom Estimator from an existing Keras model
- Summary

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