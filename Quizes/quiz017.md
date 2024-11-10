# Code
```.py
def truth_table(n:int):
    for i in range(n):
        print(f"bit{i}", end=" | ")
    print()
    for i in range(2 ** n):
        binary_string = f"{i:0{n}b}"
        for bit in binary_string:
            print(bit, end="   | ")
        print("\n")

truth_table(3)
```
# Proof Code Works
![image](https://github.com/user-attachments/assets/07afc98b-5dc1-4eb6-8a75-5fd1c483d2a2)

# Truth table and circuit for Light = S1S2+(S2+S3(notS1))S1
![photo_2024-11-11_00-42-32](https://github.com/user-attachments/assets/916a8564-b0b7-4c10-8337-32c2d04c65e2)
![photo_2024-11-11_00-42-31](https://github.com/user-attachments/assets/417a784d-6dec-4cd2-a485-3a400c5e0287)
