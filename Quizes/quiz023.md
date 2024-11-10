# Paper Solution
![photo_2024-11-11_01-11-46](https://github.com/user-attachments/assets/c205271d-ce33-49fd-856a-311f3e4a0983)
# Code
```.py
import random
from matplotlib import pyplot as plt
import matplotlib
import numpy as np
h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]
x = []

for i in range(32):
    x.append(i)

plt.style.use('ggplot')
plt.scatter(x, h, label='Humidity')

m, b = np.polyfit(x, h, 1)
def model (x,m,b):
    H_model = m*x+b
    return H_model
x_model = [min(x), max(x)]
y_model = [model(min(x),m,b), model(max(x),m,b)]

print(f"h = {m:.02f}, b = {b:02f}")
# Plot the linear model
plt.plot(x_model, y_model)
plt.xlabel('Time (10-minute intervals)')
plt.ylabel('Relative Humidity (%)')
plt.title("Relative Humidity Over Time with Linear Model")

plt.show()
```
# Proof Code Works
![image](https://github.com/user-attachments/assets/5c80f5bb-8d24-467d-af6e-c7b6370b8e76)
