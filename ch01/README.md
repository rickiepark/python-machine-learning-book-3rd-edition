##  1장: 컴퓨터는 데이터에서 배운다


---

**1장에는 코드 예제가 없습니다.**

---

## 파이썬 패키지 설치

파이썬은 세 개의 주요 운영 체제인 마이크로소프트 윈도(Microsoft Windows), macOS, 리눅스
(Linux)에서 사용할 수 있습니다. 파이썬 공식 웹 사이트(https://www.python.org)에서 문서와
설치 파일을 내려받을 수 있습니다

책은 파이썬 3.7.2 버전과 그 이상에 맞추어져 있습니다. 현재 파이썬 3의 최신 버전을 사용하
는 것이 좋습니다.
일부 코드는 파이썬 2.7과 호환될 수 있지만 파이썬 2.7의 공식 지원이 2019년 말에 끝났기 때문에 상당수의 오픈 소스 라이브러리는 이미 파이썬 2.7에 대한 지원을 중단했습니다(https://python3statement.org/). 따라서 파이썬 3.7 또는 그 이상을 사용하는 것이 매우 권장됩니다.

**노트**

다음 명령으로 현재 파이썬 버전을 확인할 수 있습니다.

    $ python -V

예를 들면 다음과 같이 출력됩니다.

    Python 3.7.1 :: Continuum Analytics, Inc.


#### pip

책에서 사용할 패키지는 pip 설치 프로그램으로 설치할 수 있습니다. 이 프로그램은 파이썬 3.3
버전부터 파이썬 표준 라이브러리에 포함되었습니다. 자세한 pip 설명은 온라인 문서(https://
docs.python.org/3/installing/index.html)를 참고하세요.

파이썬을 설치하고 난 후 터미널(Terminal)에서 pip 명령으로 필요한 파이썬 패키지를 설치할 수
있습니다:

    pip install SomePackage


(`SomePackage`는 numpy, pandas, matplotlib, scikit-learn 등이 될 수 있습니다)

설치한 패키지를 업데이트할 때는 `--upgrade` 옵션을 사용합니다:

    pip install SomePackage --upgrade


#### 아나콘다

과학 컴퓨팅을 위해서는 컨티넘 애널리틱스(Continuum Analytics)의 아나콘다(Anaconda) 파이썬 배포판을 권장합니다. 아나콘다는 상업적 목
적을 포함하여 무료로 사용할 수 있고 기업이 사용하기 충분한 수준의 파이썬 배포판입니다. 데이
터 과학, 수학, 공학용 파이썬 필수 패키지들을 모두 포함하고 있으며 주요 운영 체제를 모두 지원
합니다. 아나콘다 설치 파일은 https://www.anaconda.com/download/에서 내려받을 수 있
습니다. 간단한 아나콘다 안내는 온라인 문서(https://docs.anaconda.com/anaconda/userguide/
getting-started/)를 참고하세요.

아나콘다를 설치한 후 다음 명령으로 필요한 파이썬 패키지를 설치할 수 있습니다:

    conda install SomePackage

설치한 패키지를 업데이트할 때는 다음 명령을 사용합니다:

    conda update SomePackage

책 전반에 걸쳐 데이터를 저장하고 조작하는 데 넘파이 다차원 배열을 주로 사용합니다. 이따금
판다스(Pandas)도 사용합니다. 판다스는 넘파이 위에 구축된 라이브러리고 테이블 형태의 데이터
를 아주 쉽게 다룰 수 있는 고수준 도구를 제공합니다. 종종 정량적인 데이터를 시각화하면
이해하는 데 매우 도움이 됩니다. 이를 위해 많은 옵션을 제공하는 맷플롯립(Matplotlib) 라이
브러리를 사용하겠습니다.

#### 핵심 패키지

책에서 사용하는 주요 파이썬 패키지 버전은 다음과 같습니다. 여러분 컴퓨터에 설치된 패키지와
버전이 동일하거나 더 높은지 확인하세요. 예제 코드를 정상적으로 실행하려면 버전을 맞추는 것
이 좋습니다:

- [NumPy](http://www.numpy.org) >= 1.18.5
- [SciPy](http://www.scipy.org) >= 1.4.1
- [scikit-learn](http://scikit-learn.org/stable/) >= 0.23.2
- [matplotlib](http://matplotlib.org) >= 3.1.1
- [pandas](http://pandas.pydata.org) >= 1.0.4
- [TensorFlow](https://www.tensorflow.org) >= 2.3.0

## 파이썬/주피터 노트북

어떤 독자들은 `.ipynb` 코드 파일에 무엇인지 모를 수 있습니다. 이 파일은 IPython 노트북입니다. 이 책의 코드는 평범한 파이썬 `.py` 스크립트 대신에 IPython 노트북에 담겨 있습니다. IPython 노트북이 데이터 분석 프로젝트에 안성맞춤이기 때문입니다! IPython 노트북을 사용하면 한 곳에서 모든 것을 처리할 수 있습니다. 코드, 코드를 실행한 결과, 그래프, 막다운(markdown)과 LaTeX 문법을을 지원하는 문서까지 가능합니다!

![](./images/ipynb_ex1.png)

**노트:**  "IPython 노트북"은 최근에 "[주피터(Jupyter) 노트북](http://jupyter.org)"으로 바뀌었습니다. 주피터는 파이썬 외에도 줄리아(Julia), R 등의 다른 언어를 지원하는 프로젝트입니다. 파이썬 사용자에게는 달라지는 것이 없습니다. 이름만 바뀌었을 뿐입니다("IPython 노트북" 대신 "주피터 노트북"이라고 부릅니다).

주피터 노트북은 pip를 사용해 설치할 수 있습니다.

    $ pip install jupyter notebook

또는 아나콘다나 미니콘다를 설치했다면 콘다를 사용할 수 있습니다:

    $ conda install jupyter notebook

주피터 노트북을 열려면 먼저 코드가 있는 디렉토리로 이동합니다. 예를 들어:


    $ cd ~/code/python-machine-learning-book

그다음 `jupyter notebook`을 실행합니다.

    $ jupyter notebook

주피터가 기본 브라우저를 실행합니다(일반적으로 [http://localhost:8888/](http://localhost:8888/)에서 실행됩니다). 이제 주피터 메뉴에서 원하는 노트북을 선택해 열 수 있습니다.

![](./images/ipynb_ex2.png)

주피터 노트북에 대한 더 자세한 내용은 [주피터 초보자 가이드](http://jupyter-notebook-beginner-guide.readthedocs.org/en/latest/what_is_jupyter.html)와 [주피터 노트북 기본사항](https://jupyter-notebook.readthedocs.io/en/stable/examples/Notebook/Notebook%20Basics.html)을 참고하세요.

## 주피터 랩

또 다른 주피터 노트북 환경인 주피터 랩(Jupyter Lab)이 2018년에 릴리스되었습니다. 동일한 `.ipynb` 파일을 다룰 수 있지만 브라우저 인터페이스에서 추가적인 기능을 제공합니다. 주피터 노트북과 주피터 랩 중 어느 것을 사용해도 괜찮습니다.

주피터 랩은 다음과 같이 설치할 수 있습니다.

    $ conda install -c conda-forge jupyterlab

주피터 노트북과 비슷하게 실행하려면 다음 명령을 실행합니다.

    $ jupyter lab

이 명령을 커맨드 라인 터미널에서 실행하면 브라우저에서 주피터 랩 세션을 시작합니다. 주피터 랩에 대한 더 자세한 정보는 [공식 문서](https://jupyterlab.readthedocs.io/en/stable/)를 참고하세요.
