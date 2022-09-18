Classification with Linear model
================================

Binary Classification
---------------------

이번 절에서는 2차원 평면에 주어진 2가지 종류의 좌표 데이터를 학습하는 가장 기본적인 이항 분류 문제를 다룹니다.

.. exec_code::
   :linenos:

   import numpy as np

   xy = np.array([[.2, .4],[.4, .2],[.65,.3],[.8, .5],[.5, .8],[.25, .8]])
   labels = np.array([[0],[0],[0],[1],[1],[1]], dtype=np.int32)
   print(xy)
   print(labels)


Multiclass Classification
-------------------------