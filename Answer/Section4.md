# Section 4

## 1 f683

```py
from math import pi
n = int(input())
print(str(pi)[n+1])
```

## 2 f683

```py
2 c554
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
