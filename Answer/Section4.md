# Section 4

## 1 f683

```py
from math import pi
n = int(input())
print(str(pi)[n+1])
```

## 2 f683

```py
s = input()
print(s[0] + 'o' + s[2:])
```

## 3 e945

``` py
s = input()
if len(s) % 2 == 0:
    mid = len(s) // 2
    if s[:mid] == s[-1:mid-1:-1]: # s[:mid] == s[mid:][::-1]
        print('Yes')
        print(s[:mid])
    else:
        print('No')
else:
    print('No')
```

## 4 c557

```py
import re
s = input()
t1, t2 = re.findall(r'(\d{2}):(\d{2})', s)
t1 = int(t1[0]) * 60 + int(t1[1])
t2 = int(t2[0]) * 60 + int(t2[1])
print(t2 - t1 + 1440 * (t1 > t2))
```

```py
s = input()
t1 = int(s[0:2]) * 60 + int(s[3:5])
t2 = int(s[6:8]) * 60 + int(s[9:11])
print(t2 - t1 + 1440 * (t1 > t2))
```

## 5 c558

```py
# ord('A') = 65 ord('B') = 66 ord('C') = 67 ...
score = sum(ord(i) - 64 for i in input().upper())
print(score)
```

## 6 c559 (same as c558)

```py
# ord('A') = 65 ord('B') = 66 ord('C') = 67 ...
score = sum(ord(i) - 64 for i in input().upper())
print(score)
```

## 7 a020

```py
order = '          ABCDEFGHJKLMNPQRSTUVXYWZIO'
id_ = input()
char = str(order.index(id_[0]))
result = int(char[0]) + int(char[1]) * 9
for i in range(8, 1-1, -1):
    result += int(id_[1:][8-i]) * i
result += int(id_[-1])
if result % 10 == 0:
    print('real')
else:
    print('fake')
```

## 8 e936

```py
s = input()
result = ''
for i in range(len(s)):
    if i % 2 == 0:
        result += s[i]
    else:
        result += '*'
print(result)
```

## 9 f380

```py
n1 = input()
n2 = input()
for i in n1:
    for j in n2:
        print(i + j)
```

## 10 f697

```py
s = input()
s = ''.join(chr(ord(i) + 7) for i in s)
print(s)
```

## 11 e106

```py
order = '''GHIJABCOPQRSTUDEFVWXYZKLMNghijklabpqrstcdefmnxyzouvw ,(:)'".-!?[]{}#%&*0123456789'''
s = input()
print(''.join(order[(order.index(i) + 7) % len(order)] for i in s))
```

```py
order = '''GHIJABCOPQRSTUDEFVWXYZKLMNghijklabpqrstcdefmnxyzouvw ,(:)'".-!?[]{}#%&*0123456789'''
s = input()
print(''.join(order[(order.find(i) + 7) % len(order)] for i in s))
```

## 12 e192

```py
order = '''GHIJABCOPQRSTUDEFVWXYZKLMNghijklabpqrstcdefmnxyzouvw ,(:)'".-!?[]{}#%&*0123456789'''
s = input()
shift = order.index(s[-1])
print(''.join(order[(order.index(i) + shift) % len(order)] for i in s))
```

## 13 f110

```py
try:
    while True:
        s1 = input().replace(' ', '')
        s2 = input().replace(' ', '')
        for i in set(s1): # set: 集合
            if s1.count(i) != s2.count(i):
                print('No')
                break
        else:
            print('Yes')
except EOFError:
    pass
```
