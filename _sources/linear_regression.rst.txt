Linear Regression
=================

이번 절에서는 선형 회귀 모델을 학습시키는 최적화 문제를 설정하고 최적화 문제에 포함 된 예측 모델과 손실함수를 설명합니다.
다음은 선형 회귀 모델 학습에 사용될 데이터를 만들어내는 코드입니다. 일반적으로는 주어진 데이터로 해야 하지만, 실습의 단순화를 위해 직접 데이터를 만들었습니다. 먼저 필요한 패키지들을 불러오는 코드를 실행합니다.

기울기가 0.5이고 :math:`y` 절편이 1.0인 직선을 기준으로 값을 계산하고 노이즈를 더해서 데이터를 생성합니다.

.. exec_code::
   :linenos:

   import numpy as np

   np.random.seed(320)
   x_train = np.linspace(-1, 1, 51)
   y_train = 0.5 * x_train + 1.0 + 0.4 * np.random.rand(len(x_train))

   print(f'x_train 앞 10개: {x_train[:5]}')
   print(f'y_train 앞 10개: {y_train[:5]}')