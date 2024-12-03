# Paper Solution
![photo_2024-12-04_01-12-03](https://github.com/user-attachments/assets/82541d96-5fae-4a07-b449-86385912bc14)

# Code

```.py
def count_letters(lexicon, msg):
    msg = msg.lower()
    for char in msg:
        if char in lexicon:
            lexicon[char] += 1
    return lexicon

test1_lexicon = {'w': 0, 'l': 0, 'c': 0}
test1_msg = "hello world"

test2_lexicon = {'a': 0, 'e': 0, 'i': 0, 'o': 0, 'u': 0}
test2_msg = "Why did I choose CS?"

case1 = count_letters(test1_lexicon, test1_msg)
case2 = count_letters(test2_lexicon, test2_msg)
print(case1)
print(case2)
```
# Proof Code Works
![image](https://github.com/user-attachments/assets/c42f90d3-c21f-4d5b-bed3-c2fbdb8e5123)
