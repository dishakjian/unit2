# Paper solution(code and truth table/circuit)
![photo_2024-11-11_00-42-29](https://github.com/user-attachments/assets/5185ad37-76b4-4ec2-a855-c0b6ab114b89)
![photo_2024-11-11_00-42-28](https://github.com/user-attachments/assets/9dddfc15-f609-4492-80b5-32873833c421)

# Code
```.py
def truth_table():
    print(f"{'A':<2} {'B':<2} {'C':<2} | {'AB + not B + not CB':<19}")
    print("-" * 30)
    for A in [0, 1]:
        for B in [0, 1]:
            for C in [0, 1]:
                result = (A and B) or (not B) or (not (C and B))
                print(f"{A:<2} {B:<2} {C:<2} | {int(result):<19}")
truth_table()
```

# Proof Code Works
![image](https://github.com/user-attachments/assets/86751be6-4dcc-43d4-89d7-917031e4bcdf)
