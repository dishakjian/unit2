# Paper solution
![photo_2024-11-11_01-11-44](https://github.com/user-attachments/assets/90d2d85c-a266-4cae-bff8-28da645c83f6)

# Code
```.py
from matplotlib import pyplot as plt
import matplotlib

plt.style.use('ggplot')

start = -10
step = 0.01
x,y = [], []

for i in range(int(20/step)): #20 = -10 to 10
    x.append(start + step*i)
    y.append(2*(x[-1]+5)**2)

line_x = [-5, -5]
line_y = [0, 2*((15)**2)]

plt.plot(line_x, line_y, linestyle = "dashed", linewidth = 2, color = "#0a55a6")

plt.plot(x, y, linewidth = 2, color = "#abcdef")
plt.xlabel("x")
plt.ylabel("$y=2(x+5)^2$")
plt.title("Graph for the parabola $y=2(x+5)^2$")
plt.show()
```
# Proof Code Works
![image](https://github.com/user-attachments/assets/3f31969c-8633-4f8d-b287-d11e10c73d1c)
