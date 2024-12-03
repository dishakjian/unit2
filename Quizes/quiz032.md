# Paper Solution
![photo_2024-12-04_01-12-00](https://github.com/user-attachments/assets/daed0707-c144-436b-b99a-b0ed09e1a920)

# Code
```.py
def mystery(a :list, b :list):
    x = []
    for i in a:
        for j in b:
            if i == j:
                x.append(i)
    return x

c = [3,6,9,12,15,18]
d = [2,4,6,8,10,12,14,16,18,20]

print(mystery(c,d))
```
# Proof Code Works
![image](https://github.com/user-attachments/assets/a37fad63-eab9-47f2-b56e-711f176f0912)
