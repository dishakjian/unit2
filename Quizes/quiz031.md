# Code
```.py
import numpy as np
import matplotlib.pyplot as plt
import requests

step = 4 / 100
x = np.arange(-4, 4 + step, step)
y = np.arange(-4, 4 + step, step)


plt.figure(figsize=(8, 8))

plt.plot(x,x**2, color="blue")
plt.plot(x,-x**2, color="red")
plt.plot(y**2, y, color="green")
plt.plot(-y**2, y, color="purple")


plt.xlim(-4, 4)
plt.ylim(-4, 4)
plt.grid()
plt.title("Four Parabolas aligned with axes")
plt.show()
```
# Proof Code Works
![image](https://github.com/user-attachments/assets/b6580ad3-9e89-43f2-bb34-6c529d746b5f)
