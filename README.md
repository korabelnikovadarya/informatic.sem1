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

@startuml
object customer_1 {
  name = "Маша"
  email = "masha@example.com"
  phone = "+7123456789"
  address = "г. Москва, ул. Красная, д.1"
}

object customer_2 {
  name = "Катя"
  email = "katya@example.com"
  phone = "+7987654321"
  address = "г. Москва, ул. Ленина, д.10"
}

object SuperShmot {
  company = "СуперШмот"
  inn = "1234567890"
  email = "sales@super.shmot"
  phone = "+79999999999"
  address = "г. Москва, ул. Проспект, д.1"
}

object jacket {
  name = "jacket"
  category = "ladieswear"
  provider = SuperShmot
  price = 3.00
}

object slacks {
  name = "slacks"
  category = "ladieswear"
  provider = SuperShmot
  price = 5.00
}

object pantsuit {
  name = "pantsuit"
  category = "ladieswear"
  provider = SuperShmot
  elements = [jacket, slacks]
  price = 7.00
}

object Order_1 {
  number = 12345
  timestamp = date(2023, 20, 7)
  customer = customer_1
  products = [(jacket, 1), (slacks,1)]
}

object Order_2 {
  number = 6790
  timestamp = date(2023, 30, 7)
  customer = customer_2
  products = [(pantsuit,3)]
}

jacket --> SuperShmot
slacks --> SuperShmot
pantsuit --> SuperShmot
pantsuit "1" *--> "1" jacket
pantsuit "1" *--> "1" slacks
Order_1 --> customer_1
Order_2 --> customer_2
Order_2 "1" o-> "3" pantsuit
Order_1 "1" o--> "1" slacks
Order_1 "1" o--> "1" jacket
@enduml
