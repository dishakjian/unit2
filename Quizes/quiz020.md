# Paper solution
![photo_2024-11-11_01-11-43](https://github.com/user-attachments/assets/229a6a8e-a3a4-42f1-aeb8-1dfd43232f09)

# Code
```.py
import random

from matplotlib import pyplot as plt
import matplotlib

random.seed(1234)
def produce(n=5,m=3,s=2):
    x,y = [],[]
    for _ in range(n):
        r = random.randint(0,100)
        x.append(r)
        e = r ** (0.5 * (m/s) ** 2)
        y.append(e)
    return x,y

ax, ay = produce(n=10)
plt.plot(ax,ay,'or')
plt.show()
```
# Proof Code Works
![image](https://github.com/user-attachments/assets/d12f9d59-f957-494a-b4b8-ae30c950ffe2)
