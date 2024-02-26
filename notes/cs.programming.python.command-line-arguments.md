---
id: peybhew3nxmkervzvl5cehj
title: Command Line Arguments
desc: ''
updated: 1708696027165
created: 1708695133138
---

```py
import sys

print(len(sys.argv))
for x in sys.argv:
    print(x)
```


![](/assets/images/2024-02-23-19-09-40.png)

### Ex-2

```py
import sys

arg = sys.argv[1]

if arg == "himanshu":
    print("Login allowed")
else:
    print("Who are you ?")

```
