# Paper Solution
![photo_2024-12-04_01-19-18](https://github.com/user-attachments/assets/662e6c81-665c-42d4-bf30-ed50827164bc)
# Code
```.py
def sort_dict(in_dict):
    sorted_dict = dict(sorted(in_dict.items(), key=lambda item: str(item[1])))
    return sorted_dict

test1 = {'apple': 5, 'banana': 2, 'orange': 8, 'grape': 1}
test2 = {'python': 3, 'java': 8, 'c++': 5, 'javascript': 2}
test3 = {'apple': 'red', 'banana': 2, 'orange': 'orange', 'grape': 1, 'kiwi': 'brown', 'pear': 8}

print(sort_dict(test1))
print(sort_dict(test2))
print(sort_dict(test3))
```
# Proof Code Works
![image](https://github.com/user-attachments/assets/283c02a1-cdd8-4f5f-ba2e-c57a37b1e1da)
