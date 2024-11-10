# Paper Solution
![photo_2024-11-11_01-16-37](https://github.com/user-attachments/assets/0ee848df-cf49-42e7-8d47-7d140960de60)

# Code
```.py
from matplotlib import pyplot as plt
plt.style.use('ggplot')
start = -10
step = 0.01
x,y = [], []
for i in range(int(20/step)): #20 = -10 to 10
    n = start + step * i
    x.append(n)
    if n >= 0:
        y.append(n)
    else:
        y.append(n*-1)

plt.plot(x,y)
plt.xlabel("x")
plt.ylabel("$y=|x|$")
plt.title("Graph for $y=|x|$")
plt.show()
```

# Proof Code Works
![image](https://github.com/user-attachments/assets/200989d7-d260-4503-948d-4b29d3b178a0)
