머신 러닝 교과서


##  2장: 간단한 분류 알고리즘 훈련

### 목차

- 인공 뉴런: 초기 머신 러닝의 간단한 역사
    - 인공 뉴런의 수학적 정의
    - 퍼셉트론 학습 규칙
- 파이썬으로 퍼셉트론 학습 알고리즘 구현
    - 객체 지향 퍼셉트론 API
    - 붓꽃 데이터셋에서 퍼셉트론 훈련
- 적응형 선형 뉴런과 학습의 수렴
    - 경사 하강법으로 비용 함수 최소화
    - 파이썬으로 아달린 구현
    - 특성 스케일을 조정하여 경사 하강법 결과 향상
    - 대규모 머신 러닝과 확률적 경사 하강법
- 요약

### A note on using the code examples

The recommended way to interact with the code examples in this book is via Jupyter Notebook (the `.ipynb` files). Using Jupyter Notebook, you will be able to execute the code step by step and have all the resulting outputs (including plots and images) all in one convenient document.

![](images/jupyter-example-1.png)



Setting up Jupyter Notebook is really easy: if you are using the Anaconda Python distribution, all you need to install jupyter notebook is to execute the following command in your terminal:

    conda install jupyter notebook

Then you can launch jupyter notebook by executing

    jupyter notebook

A window will open up in your browser, which you can then use to navigate to the target directory that contains the `.ipynb` file you wish to open.

**More installation and setup instructions can be found in the [README.md file of Chapter 1](../ch01/README.md)**.

**(Even if you decide not to install Jupyter Notebook, note that you can also view the notebook files on GitHub by simply clicking on them: [`ch02.ipynb`](ch02.ipynb))**

In addition to the code examples, I added a table of contents to each Jupyter notebook as well as section headers that are consistent with the content of the book. Also, I included the original images and figures in hope that these make it easier to navigate and work with the code interactively as you are reading the book.

![](images/jupyter-example-2.png)


When I was creating these notebooks, I was hoping to make your reading (and coding) experience as convenient as possible! However, if you don't wish to use Jupyter Notebooks, I also converted these notebooks to regular Python script files (`.py` files) that can be viewed and edited in any plaintext editor. 