# Gjuhë Programuese - Java 6

---

## Përsëritje

---

**Detyrë:** Çka do të shtypet kur ekzekutohet ky kod?

```cpp
#include <iostream>
using namespace std;

int main() {
  for (int i = 0; i < 10; i += 2) {
    cout << 2 * i << endl;

    if (i == 6) {
      break;
    }
  }
}
```

--

```text
0
4
8
12
```

---

## Vargjet (vektorët)

Vargu është seri e vlerave të ndonjë tipi.

---

**Shembull:** Ruajtja e vargut të notave

```cpp
int notat[4] = { 9, 10, 8, 7 };
```

`notat` është varg i gjatësisë $4$ dhe është inicializuar me vlerat $\lbrace 9, 10, 8, 7 \rbrace$

---

Leximi nga vargu:

```cpp
int notat[4] = { 9, 10, 8, 7 };
int nota1 = notat[0]; // 9
int nota2 = notat[1]; // 10
int nota3 = notat[2]; // 8
int nota4 = notat[3]; // 7
```

![](/lendet/gjuhe-programuese/java6/notat.png) <!-- .element: style="max-height:400px;border:none;" -->

---

Shkruarja në varg:

```cpp
int notat[4];
notat[0] = 9;  // nota 1
notat[1] = 10; // nota 2
notat[2] = 8;  // nota 3
notat[3] = 7;  // nota 4
```

---

Numërimi i vargut me gjatësi $n$ fillon me $0$ dhe mbaron me $n-1$.

Duhet pasur kujdes mos t'i tejkalojmë kufijtë e vargut.

---

**Shembull:** Vizitimi i secilit element të vargut

```cpp
const int n = 5;
int vargu[n] = { 5, -2, 4, 7, 3 };

for (int i = 0; i < n; i++) {
  cout << vargu[i] << endl;
}
```

Unaza merr vlerat $i = \lbrace 0 \dots n-1 \rbrace$

---

**Përmbledhje**

- Vargu ka gjatësi konstante $n$.
- Elementeve iu qasemi përmes indeksimit `v[i]`
- Elementi i parë gjendet në indeksin $0$.
- Elementi i fundit gjendet në indeksin $n-1$.

---

**Detyrë:** Të inicializohet vargu $\lbrace 7,2,5,6,1,10,3 \rbrace$

1. Të shfaqen të gjithë elementet e këtij vargu.
2. Të gjendet shuma e elementeve të vargut.
3. Të tregohet sa elemente janë $\geq 5$.
4. Të gjendet shuma e numrave tek dhe çift.
5. Të gjendet shuma e elementit të parë dhe të fundit.

--

1. Të shfaqen të gjithë elementet e këtij vargu.

```cpp
#include <iostream>
using namespace std;

int main() {
  const int n = 7;
  int v[n] = { 7, 2, 5, 6, 1, 10, 3 };

  for (int i = 0; i < n; i++) {
    cout << v[i] << endl;
  }

  return 0;
}
```

--

2. Të gjendet shuma e elementeve të vargut.

```cpp
#include <iostream>
using namespace std;

int main() {
  const int n = 7;
  int v[n] = { 7, 2, 5, 6, 1, 10, 3 };

  int S = 0;

  for (int i = 0; i < n; i++) {
    S += v[i];
  }

  cout << "S=" << S << endl;
  return 0;
}
```

--

3. Të tregohet sa elemente janë $\geq 5$.

```cpp
#include <iostream>
using namespace std;

int main() {
  const int n = 7;
  int v[n] = { 7, 2, 5, 6, 1, 10, 3 };

  int nr = 0;

  for (int i = 0; i < n; i++) {
    if (v[i] >= 5) {
      nr++;
    }
  }

  cout << "nr=" << nr << endl;
  return 0;
}
```

--

4. Të gjendet shuma e numrave tek dhe çift.

```cpp
#include <iostream>
using namespace std;

int main() {
  const int n = 7;
  int v[n] = { 7, 2, 5, 6, 1, 10, 3 };

  int shuma_cift = 0;
  int shuma_tek = 0;

  for (int i = 0; i < n; i++) {
    if (v[i] % 2 == 0) {
      shuma_cift += v[i];
    } else {
      shuma_tek += v[i];
    }
  }

  cout << "nr=" << nr << endl;
  return 0;
}
```

--

5. Të gjendet shuma e elementit të parë dhe të fundit.

```cpp
#include <iostream>
using namespace std;

int main() {
  const int n = 7;
  int v[n] = { 7, 2, 5, 6, 1, 10, 3 };

  cout << "Shuma e elementit te pare dhe te fundit: "
       << v[0] + v[n - 1] << endl;
  return 0;
}
```

---

**Detyrë:** Të krijohet një varg me gjatësi 5. Të lexohen 5 numra nga tastiera dhe të ruhen në këtë varg.

1. Të gjendet elementi më i madh në këtë varg.
2. Të gjendet elementi më i vogël në këtë varg.
3. Të shfaqen elementet në indeksa tek.
4. Të kthehet vargu mbrapsht dhe të shfaqen vlerat.

--

1. Të gjendet elementi më i madh në këtë varg.

```cpp
#include <iostream>
using namespace std;

int main() {
  const int n = 5;
  int v[n];

  for (int i = 0; i < n; i++) {
    cin >> v[i];
  }
  
  int max = v[0];
  for (int i = 1; i < n; i++) {
    if (v[i] > max) {
      max = v[i];
    }
  }

  cout << "Maksimumi: " << max << endl;
  return 0;
}
```

--

2. Të gjendet elementi më i vogël në këtë varg.

```cpp
#include <iostream>
using namespace std;

int main() {
  const int n = 5;
  int v[n];

  for (int i = 0; i < n; i++) {
    cin >> v[i];
  }
  
  int min = v[0];
  for (int i = 1; i < n; i++) {
    if (v[i] < min) {
      min = v[i];
    }
  }

  cout << "Minimumi: " << min << endl;
  return 0;
}
```

--

3. Të shfaqen elementet në indeksa tek.

```cpp
#include <iostream>
using namespace std;

int main() {
  const int n = 5;
  int v[n];

  for (int i = 0; i < n; i++) {
    cin >> v[i];
  }
  
  for (int i = 1; i < n; i += 2) {
    cout << v[i] << endl;
  }

  return 0;
}
```

--

4. Të kthehet vargu mbrapsht dhe të shfaqen vlerat.

```cpp
#include <iostream>
using namespace std;

int main() {
  const int n = 5;
  int v[n];

  for (int i = 0; i < n; i++) {
    cin >> v[i];
  }
  
  for (int i = 0; i < n / 2; i++) {
    int temp = v[n - 1 - i];
    v[n - 1 - i] = v[i];
    v[i] = temp;
  }

  cout << "Pas nderrimit:" << endl;
  for (int i = 0; i < n; i++) {
    cout << v[i] << endl;
  }

  return 0;
}
```

---

**Detyrë:** Të krijohet vargu $\lbrace 2.5,1.7,3.2,7.5,11.3 \rbrace$.

1. Të llogaritet mesatarja e vargut.
2. Të kopjohet vargu në një varg tjetër.
3. Në vargun e ri elementet ta kenë shenjën e kundërt.

--

1. Të llogaritet mesatarja e vargut.

```cpp
#include <iostream>
using namespace std;

int main() {
  const int n = 5;
  double v[n] = { 2.5, 1.7, 3.2, 7.5, 11.3 };
  double S = 0;

  for (int i = 0; i < n; i++) {
    S += v[i];
  }

  cout << "Mesatarja: " << S / n << endl;
  return 0;
}
```

--

2. Të kopjohet vargu në një varg tjetër.

```cpp
#include <iostream>
using namespace std;

int main() {
  const int n = 5;
  double v[n] = { 2.5, 1.7, 3.2, 7.5, 11.3 };
  double v2[n];
  
  for (int i = 0; i < n; i++) {
    v2[i] = v[i];
  }

  return 0;
}
```

--

3. Në vargun e ri elementet ta kenë shenjën e kundërt.

```cpp
#include <iostream>
using namespace std;

int main() {
  const int n = 5;
  double v[n] = { 2.5, 1.7, 3.2, 7.5, 11.3 };
  double v2[n];
  
  for (int i = 0; i < n; i++) {
    v2[i] = -v[i];
  }

  return 0;
}
```

---

## Matricat

Matrica është varg dy-dimenzional - me rreshta dhe kolona.

---

Nga matematika, matricat janë struktura të formës:

$$
A_{m,n} = 
\begin{pmatrix}
a_{1,1} & a_{1,2} & \cdots & a_{1,n} \\
a_{2,1} & a_{2,2} & \cdots & a_{2,n} \\
\vdots  & \vdots  & \ddots & \vdots  \\
a_{m,1} & a_{m,2} & \cdots & a_{m,n} 
\end{pmatrix}
$$

---

Në C++, rreshtat dhe kolonat fillojnë me indeksin $0$:

$$
A_{m,n} = 
\begin{pmatrix}
a_{0,0} & a_{0,1} & \cdots & a_{0,n-1} \\
a_{1,0} & a_{1,1} & \cdots & a_{1,n-1} \\
\vdots  & \vdots  & \ddots & \vdots  \\
a_{m-1,0} & a_{m-1,1} & \cdots & a_{m-1,n-1} 
\end{pmatrix}
$$

---

**Shembull:** Deklarimi i matricës

$$
A_{3,4} =
\begin{pmatrix}
2 & 4 & 7 & 1 \\
5 & -1 & 3 & 5 \\
3 & 2 & 1 & 14
\end{pmatrix}
$$

```cpp
int A[3][4] = {
  { 2,  4,  7,  1 },
  { 5, -1,  3,  5 },
  { 3,  2,  1, 14 }
};
```

---

Leximi dhe shkrimi i anëtarëve:

```cpp
int A[3][4] = {
  { 2,  4,  7,  1 },
  { 5, -1,  3,  5 },
  { 3,  2,  1, 14 }
};

int vlera = A[1][3]; // vlera = 5
A[2][0] = 13;
```

---

**Detyrë:** Të inicializohet matrica

$$
A_{2,3} =
\begin{pmatrix}
1 & 2 & 6 \\
5 & 7 & 4
\end{pmatrix}
$$

1. Të shfaqen të gjithë anëtarët e matricës.
2. Të llogaritet shuma e anëtarëve.
3. Të gjendet anëtari më i madh dhe më i vogël.

--

1. Të shfaqen të gjithë anëtarët e matricës.

```cpp
#include <iostream>
using namespace std;

int main() {
  const int m = 2;
  const int n = 3;
  int A[2][3] = {
    { 1, 2, 6 },
    { 5, 7, 4 }
  };

  for (int i = 0; i < m; i++) {
    for (int j = 0; j < n; j++) {
      cout << A[i][j] << " ";
    }

    cout << endl;
  }

  return 0;
}
```

--

2. Të llogaritet shuma e anëtarëve.

```cpp
#include <iostream>
using namespace std;

int main() {
  const int m = 2;
  const int n = 3;
  int A[2][3] = {
    { 1, 2, 6 },
    { 5, 7, 4 }
  };

  int S = 0;

  for (int i = 0; i < m; i++) {
    for (int j = 0; j < n; j++) {
      S += A[i][j];
    }
  }

  cout << "S=" << S << endl;
  return 0;
}
```

--

3. Të gjendet anëtari më i madh dhe më i vogël.

```cpp
#include <iostream>
using namespace std;

int main() {
  const int m = 2;
  const int n = 3;
  int A[2][3] = {
    { 1, 2, 6 },
    { 5, 7, 4 }
  };

  int max = A[0][0];
  int min = A[0][0];

  for (int i = 0; i < m; i++) {
    for (int j = 0; j < n; j++) {
      if (A[i][j] > max) {
        max = A[i][j];
      }

      if (A[i][j] < min) {
        min = A[i][j];
      }
    }
  }

  cout << "Maksimumi: " << max << endl
       << "Minimumi: " << min << endl;
  return 0;
}
```
