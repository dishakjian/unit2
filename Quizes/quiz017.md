# Code
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

# Proof Code Works
![image](https://github.com/user-attachments/assets/07afc98b-5dc1-4eb6-8a75-5fd1c483d2a2)
