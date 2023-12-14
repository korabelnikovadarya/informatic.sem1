<h3 align="center">Hi there, I'm <a href="https://dashashat.ru/" target="_blank">Dasha</a> again
<h3 align="center">You need to see registration of information</h3>

#### Plotting: 

```
import matplotlib.pyplot as plt
import numpy as np
x = np.linspace(-100, 100, 100)
y = np.sin(x) * x**3
plt.plot(x, y)
plt.grid()
plt.show()
```

#### Palindrome
```
import re
s = str(input())
s = s.lower()
s = re.sub(r'[^\w\s]', '', s)
s = s.replace(' ', '')
s2 = s[::-1]
print(s)
print(s2)
print(s == s2)
```


