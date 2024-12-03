# Paper Solution
![photo_2024-12-04_01-12-02](https://github.com/user-attachments/assets/39e5fa04-e4da-4995-b2bc-3d214f1fb30f)
# Code
```.py
def flip(in_dict):
    out_dict = {}
    for key, value in in_dict.items():
        if value in out_dict:
            if isinstance(out_dict[value], list):
                out_dict[value].append(key)
            else:
                out_dict[value] = [out_dict[value], key]
        else:
            out_dict[value] = key
    return out_dict

test1 = {'a': 1, 'b': 2, 'c': 3}
test2 = {'bob': 26, 'alice': 30, 'carl': 40}
test3 = {'q1': True, 'q2': False, 'q3': True}

print(flip(test1))
print(flip(test2))
print(flip(test3))
```
# Proof Code Works
![image](https://github.com/user-attachments/assets/7f9b1be7-9cd9-4cd1-8bd5-af8a390f54a9)
