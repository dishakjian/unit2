# Paper solution
![photo_2024-11-11_00-42-22](https://github.com/user-attachments/assets/a2ac20d5-1d6c-4114-8879-f2b1b75d8322)
![photo_2024-11-11_00-42-21](https://github.com/user-attachments/assets/dae4cacb-db04-4743-8482-56eccc9188e8)

# Code
```.py
import random
def produce(n, m, s):
    random.seed(1234)
    results = []
    exponent = 0.5 * (m / s) ** 2

    for _ in range(n):
        x = random.randint(0, 100)
        y = round(x ** exponent, 2)
        results.append((x, y))
    return results
sample = produce(n=5, m=3, s=2)
print(sample)
```
# Proof Code Works
![image](https://github.com/user-attachments/assets/1cdc73f8-7b3e-4e07-afc4-f659c5f4b0ee)
