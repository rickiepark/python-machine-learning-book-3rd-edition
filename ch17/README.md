머신 러닝 교과서 2판


## 17장 - 새로운 데이터 합성을 위한 생성적 적대 신경망


### 목차

- 생성적 적대 신경망 소개
    - 오토인코더
    - 새로운 데이터 합성을 위한 생성 모델
    - GAN으로 새로운 샘플 생성하기
    - GAN의 생성자와 판별자 손실 함수 이해하기
- 밑바닥부터 GAN 모델 구현하기
    - 구글 코랩에서 GAN 모델 훈련하기
    - 생성자와 판별자 신경망 구현하기
    - 훈련 데이터셋 정의하기
    - GAN 모델 훈련하기
- 합성곱 GAN과 와서스테인 GAN을 사용하여 합성 이미지의 품질 높이기
    - 전치 합성곱
    - 배치 정규화
    - 생성자와 판별자 구현하기
    - 두 분포 사이의 거리 측정하기
    - GAN에 EM 거리 사용하기
    - 그래디언트 페널티
    - WGAN-GP로 DCGAN 모델 훈련하기
    - 모드 붕괴
- 다른 GAN 애플리케이션
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

**(주피터 노트북을 설치하지 않았더라도 깃허브에서 [`ch17_part1.ipynb`](https://github.com/rickiepark/python-machine-learning-book-3rd-edition/blob/master/ch17/ch17_part1.ipynb)과 [`ch17_part2.ipynb`](https://github.com/rickiepark/python-machine-learning-book-3rd-edition/blob/master/ch17/ch17_part2.ipynb)을 클릭해 노트북 파일을 볼 수 있습니다.)**.

코드 예제 외에도 주피터 노트북에는 책의 내용에 맞는 섹션 제목을 함께 실었습니다. 또한 주피터 노트북에 원본 이미지와 그림을 포함시켰기 때문에 책을 읽으면서 코드를 쉽게 따라할 수 있으면 좋겠습니다.

![](../ch02/images/jupyter-example-2.png)