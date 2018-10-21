# Ushtrime - Java 2

---

Të krijohet një projekt i ri dhe të shkruhet programi i cili shfaq këtë tekst në ekran:

```text
Përshëndetje!

Po mësojmë gjuhën programuese "C++".
```

--

```cpp
#include <iostream>
using namespace std;

int main() {
  cout << "P\x89rsh\x89ndetje!" 
       << endl
       << endl
       << "Po m\x89sojm\x89 gjuh\x89n programuese \"C++\".";
  return 0;
}
```

---

**Detyrë:** Të shkruhet programi i cili lexon 3 numra të plotë dhe pastaj i shfaq ata.

```text
Jepni vleren a: 15
Jepni vleren b: -2
Jepni vleren c: 3

Keni shtypur vlerat:
a = 15
b = -2
c = 3
```

--

```cpp
#include <iostream>
using namespace std;

int main() {
  int a, b, c;

  cout << "Jepni vleren a: ";
  cin  >> a;
  cout << "Jepni vleren b: ";
  cin  >> b;
  cout << "Jepni vleren c: ";
  cin  >> c;

  cout << endl << "Keni shtypur vlerat:" << endl;
  
  cout << "a = " << a << endl
       << "b = " << b << endl
       << "c = " << c << endl;

  return 0;
}
```

---

**Detyrë:** Të shkruhet programi i cili lexon 3 numra me presje dhe llogaritë mesatarën e tyre.

```text
Jepni vleren a: 3.2
Jepni vleren b: 6
Jepni vleren c: 1.3

Vlera mesatare: 3.5
```

--

```cpp
#include <iostream>
using namespace std;

int main() {
  double a, b, c, m;

  cout << "Jepni vleren a: ";
  cin  >> a;
  cout << "Jepni vleren b: ";
  cin  >> b;
  cout << "Jepni vleren c: ";
  cin  >> c;
  cout << endl;
  
  m = (a + b + c) / 3.0;
  cout << "Vlera mesatare: " << m << endl;

  return 0;
}
```

---

**Detyrë:** Të lexohen nga tastiera brinjët e drejtkëndëshit, pastaj të llogariten perimetri dhe sipërfaqja (në variabla), dhe të shfaqen në ekran.

```text
Jepni brinjen a: 5
Jepni brinjen b: 3
Perimetri i drejtkendeshit: 16
Siperfaqja e drejtkendeshit: 15
```

**Kujtesë:** $\;S=ab,\; P=2(a+b)$

--

```cpp
#include <iostream>
using namespace std;

int main() {
  int a, b, S, P;
  
  cout << "Jepni brinjen a: ";
  cin  >> a;
  cout << "Jepni brinjen b: ";
  cin  >> b;

  P = 2 * (a + b);
  S = a * b;
  
  cout << "Perimetri i drejtkendeshit: " << P << endl;
  cout << "Siperfaqja e drejtkendeshit: " << S << endl;

  return 0;
}
```

---

**Detyrë:** Janë dhënë vlerat reale $a=2.0,\;b=3.5,\;c=1.2$.

Të llogariten shprehjet:

$$
\begin{array}{rlcr}
1) & a + 2c - \frac{7}{9}b & \Rightarrow & 1.67 \\
2) & a + 2(1.1 + b) - c & \Rightarrow & 10 \\
3) & b^a - 2c & \Rightarrow & 9.85  \\
4) & \sqrt{\frac{a^2 + b^2}{c + 1}} & \Rightarrow & 2.71 \\
\end{array}
$$

--

```cpp
#include <iostream>
#include <math.h>
using namespace std;

int main() {
  double a = 2.0;
  double b = 3.5;
  double c = 1.2;

  cout << a + 2 * c - 7.0 / 9.0 * b << endl;
  cout << a + 2 * (1.1 + b) - c << endl;
  cout << pow(b, a) - 2 * c << endl;
  cout << sqrt((pow(a, 2) + pow(b, 2)) / (c + 1)) << endl;

  return 0;
}
```

---

**Detyrë:** Të gjendet sipërfaqja dhe perimetri i rrethit, nëse rrezja $r$ jepet nga tastiera. Vlera e PI ($\pi$) të deklarohet si konstante.

```text
Jepni vleren e rrezes: 3
Perimetri i rrethit: 18.84
Siperfaqja e rrethit: 28.26
```

**Kujtesë:** $\;P=2\pi r,\; S=\pi r^2,\;\pi\approx 3.14$

--

```cpp
#include <iostream>
#include <math.h>
using namespace std;

int main() {
  const double pi = 3.14;
  double r, P, S;

  cout << "Jepni vleren e rrezes: ";
  cin >> r;

  P = 2 * pi * r;
  S = pi * pow(r, 2);

  cout << "Perimetri i rrethit: " << P << endl;
  cout << "Siperfaqja e rrethit: " << S << endl;

  return 0;
}
```

---

**Detyrë:** Të deklarohet variabla $shuma=0$, dhe të lexohen pesë numrat e ardhshëm nga tastiera. Secili numër i lexuar t'i shtohet shumës.

```text
Jepni numer: 3
Jepni numer: 1
Jepni numer: 2
Jepni numer: 7
Jepni numer: 4
Totali: 17
```

--

```cpp
#include <iostream>
using namespace std;

int main() {
  int shuma = 0;
  int numri;

  cout << "Jepni numer: ";
  cin >> numri;
  shuma += numri;

  cout << "Jepni numer: ";
  cin >> numri;
  shuma += numri;

  cout << "Jepni numer: ";
  cin >> numri;
  shuma += numri;

  cout << "Jepni numer: ";
  cin >> numri;
  shuma += numri;

  cout << "Jepni numer: ";
  cin >> numri;
  shuma += numri;

  cout << "Totali: " << shuma << endl;

  return 0;
}
```

---

**Detyrë:** Të lexohen numrat e plotë $a$ dhe $b$ nga tastiera, dhe pastaj t'iu ndërrohen vlerat mes veti.

```text
Shtypni a: 10
Shtypni b: 3
Para nderrimit:
a = 10, b = 3
Pas nderrimit:
a = 3, b = 10
```

--

```cpp
#include <iostream>
using namespace std;

int main() {
  int a, b, temp;

  cout << "Shtypni a: ";
  cin  >> a;
  cout << "Shtypni b: ";
  cin  >> b;

  cout << "Para nderrimit:"
       << "a = " << a 
       << ", b = " << b << endl;

  temp = a;
  a = b;
  b = temp;

  cout << "Pas nderrimit:"
       << "a = " << a 
       << ", b = " << b << endl;

  return 0;
}
```

---

**Detyrë:** Të llogaritet hipotenuza e trekëndëshit nëse katetet $a$ dhe $b$ jepen nga tastiera.

```text
Shtypni a: 4
Shtypni b: 3
Hipotenuza e trekendeshit me katetet a=4 dhe b=3 eshte c=5.
```

**Kujtesë:** $\;c=\sqrt{a^2+b^2}$

--

```cpp
#include <iostream>
#include <math.h>
using namespace std;

int main() {
  double a, b, c;

  cout << "Shtypni a: ";
  cin  >> a;
  cout << "Shtypni b: ";
  cin  >> b;

  c = sqrt(pow(a, 2) + pow(b, 2));

  cout << "Hipotenuza e trekendeshit me katetet a="
       << a << " dhe b=" << b << " eshte c=" << c << endl;

  return 0;
}
```
