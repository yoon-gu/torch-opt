.. torch-opt documentation master file, created by
   sphinx-quickstart on Sat Sep 17 20:24:21 2022.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to torch-opt's documentation!
=====================================
안녕하세요. 깃헙으로도 스핑크스가 지원이 되는군요.


.. toctree::
   :numbered:
   :maxdepth: 1
   :caption: 목차:

   linear_regression
   linear_logis


이런저런 예제들
==================

#. abc
#. def
#. gdf

* :math:`a+b=c` 이나 :math:`\sum` 이런게 되려나?
* `aligned` 은?

.. math::

   (a + b)^2  &=  (a + b)(a + b) \\
              &=  a^2 + 2ab + b^2

..  code-block:: python
   :caption: 신경망 모델
   :linenos:

   import torch
   import torch.nn as nn
   import torch.nn.functional as F

   class QNetwork(nn.Module):
       def __init__(self, state_size, action_size, seed,
                    fc1_units=256, fc2_units=128, fc3_units=64):
           super(QNetwork, self).__init__()
           self.seed = torch.manual_seed(seed)
           self.fc1 = nn.Linear(state_size, fc1_units)
           self.fc2 = nn.Linear(fc1_units, fc2_units)
           self.fc3 = nn.Linear(fc2_units, fc3_units)
           self.fc4 = nn.Linear(fc3_units, action_size)

       def forward(self, state):
           x = F.relu(self.fc1(state))
           x = F.relu(self.fc2(x))
           x = F.relu(self.fc3(x))
           return self.fc4(x)


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
