# Code
```.py
from matplotlib import pyplot as plt
import numpy as np
data =  {
'x': [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19],
'y': [24, 1, 2, 25, 26, 21, 23, 34, 49, 2, 19, 32, 7, 17, 36, 7, 45, 28, 40, 46]
}

x,y = [], []
for i in range(len(data["x"])):
    x.append(data["x"][i])
    y.append(data["y"][i])

plt.title("quiz data science")

plt.plot(x,y,"o-")
plt.show()
```
# Proof Code Works
![image](https://github.com/user-attachments/assets/633402a7-6ee6-4b89-b33a-c321a73595f0)
