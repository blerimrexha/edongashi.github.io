# Gjuhë Programuese - Java 2

---

## Përsëritje

1. Çka është programi?
2. Çka është gjuha programuese?

--

1. Programi - varg urdhërash që ekzekutohen nga kompjuteri.
2. Gjuha programuese - sintaksa dhe rregullat për shkruarjen e programeve.

---

Çka është **main**?

--

**main** është pika hyrëse e programit.

```cpp
int main() {
  return 0;
}
```

---

Çka quajmë **bllok të kodit** dhe si shënohet?

--

**Bllok të kodit** e quajmë vargun e urdhërave të mbështjellur me kllapa gjarpërore.

```cpp
{
  urdher;
  urdher;
  urdher;
}
```

---

Të shpjegohet ky program:

```cpp
#include <iostream>
using namespace std;

int main() {
  cout << "Pershendetje" << endl;
  return 0;
}
```

---

Të krijohet një projekt i ri dhe të shkruhet programi i cili shfaq tekstin "**Pershendetje**" në ekran.

---

## Tipet dhe Variablat

---

**Rikujtim:** Kompjuteri të dhënat i ruan në formë binare - vargje të njësheve dhe zerove.

- Biti (bit) - shifra 0 ose 1.
- Bajti (byte) - vargu i 8 bitave.

--

**Shembull:** Numri $25$ në formë binare shkruhet:

$$
25_{10}=00011001_2
$$

---

Kemi disa lloje të të dhënave:

1. Tipet numerike
2. Tipi i vërtetësisë - boolean
3. Tipet tekstuale - karakteret dhe stringjet
4. Tipet komplekse

---

## Tipet numerike

Ndahen në dy kategori kryesore:

1. Numrat e plotë - **integer**
2. Numrat me presje - **floating-point**

---

<!-- .slide: style="font-size: 0.6em" -->

Numrat e plotë (integer) **me** shenjë:

Tipi|Madhësia|Vlerat
---|---|---:
`char`|1 bajt|`-128` deri `127`
`short int`|2 bajt|`-32768` deri `32767`
`int`|4 bajt|`-2147483648` deri `2147483647`
`long int`|4 bajt|`-2147483648` deri `2147483647`
`long long int`|8 bajt|`-9223372036854775808` deri `9223372036854775807`

---

<!-- .slide: style="font-size: 0.6em" -->

Numrat e plotë (integer) **pa** shenjë:

Tipi|Madhësia|Vlerat
---|---|---:
`unsigned char`|1 bajt|`0` deri `255`
`unsigned short int`|2 bajt|`0` deri `65535`
`unsigned int`|4 bajt|`0` deri `4294967295`
`unsigned long int`|4 bajt|`0` deri `4294967295`
`unsigned long long int`|8 bajt|`0` deri `18446744073709551615`

---

Numrat me presje - floating-point

Tipi|Madhësia|Preciziteti
---|---|---:
`float`|4 bajt|7 shifra
`double`|8 bajt|15-16 shifra
`long double`|16 bajt|28-29 shifra

---

Shpesh përdorën këto terme:

- Single-precision - për **float**.
- Double-precision - për **double**.

---

## Tipi i vërtetësisë

Ka vetëm dy vlera - **saktë**/**pasaktë**, **po**/**jo**, **1**/**0**.

Tipi|Madhësia|Vlerat
---|---|---
bool|1 bajt|`true` ose `false`

---

## Tipet tekstuale

Emri|Madhësia
---|---
char|1 bajt
char16_t|2 bajt
char32_t|4 bajt
string|Pacaktuar

---

**String** paraqet vargun e karaktereve deri te karakteri terminues `\0`

0  |1  |2  |3  |4
:-:|:-:|:-:|:-:|:-:
`'D'`|`'i'`|`'t'`|`'a'`|`'\0'`

---

## Tipet komplekse

1. Strukturat dhe klasat e librarisë standarde.
2. Tipet që i definojmë vet (në të ardhmen).

---

Prej gjithë këtyre tipeve, më së shpeshti do të përdorim:

- **int** - kur na nevojitet numër i plotë.
- **double** - kur na nevojitet numër me presje.
- **bool** - kur duhet ta ruajmë ndonjë fakt.

---

## Variablat

Përmes variablave "mbajmë në mend".

Variabla ka **tipin** dhe **emrin**.

```cpp
<tipi> <emri> [= <vlera fillestare>];
```

---

Variablat i kemi të njohura nga shkencat tjera:

$$
F = ma
$$

$$
v = \frac{s}{t}
$$

$$
y = 2x + 3
$$

---

Deklarimi i variablave:

```cpp
int variabla;
```

Nëse dëshirojmë ta inicializojmë me vlerë fillestare:

```cpp
int variabla = 42;
```

---

**Shembull**

**`nr_studenteve`** është numër i plotë (**`int`**), dhe paraqet numrin e studentëve prezent në sallë.

```cpp
int nr_studenteve = 14;

cout << nr_studenteve; // Çka na shfaqet?
```

---

Variablave ia lëmë emrin sipas dëshirës, me kushtin që nuk është fjalë kyçe e gjuhës programuese, psh. `int`, `float`, etj.

---

Kur kemi disa variabla, mund t'i deklarojmë në një urdhër të vetëm:

```cpp
int a, b, c;
double x, y;
```

---

Variablat mund t'i lexojmë nga tastiera:

```cpp
int a, b;

cout << "Shtypni vleren a: ";
cin  >> a; // Lexojmë nga standard input.
cout << "Shtypni vleren b: ";
cin  >> b; // Lexojmë nga standard input.
cout << "Keni shtypur a=" << a << " dhe b=" << b << endl;
```

Programi "mban në mend" numrat $a$ dhe $b$.

---

## Shprehjet

Gjithçka që ka vlerë dhe tip quhet **shprehje**.

```cpp
15      // Shprehje e tipit int.
x + 1.5 // Shprehje e tipit double.
"Tung"  // Shprehje e tipit char[] (string).
true    // Shprehje e tipit bool.
```

Ky definicion na duhet në vazhdim.

---

## Operatorët

Përmes operatorëve kryejmë llogaritje të ndryshme.

---

**Operatori i shoqërimit (assignment)**

Llogarit shprehjen nga ana **e djathtë** dhe e vendos në shprehjen e anës **së majtë**.

```cpp
int a, b;
a = 25; // Vendos 25 (ana e djathtë) në a (ana e majtë)
b = a;  // Vendos a (ana e djathtë) në b (ana e majtë)
```

Shënohet me simbolin **`=`** (baraz)

---

Shprehja e anës së majtë dhe e anës së djathtë duhet ta kenë tipin e njejtë.

```cpp
int a;
a = 25;     // Ok.
a = "Tung"; // Nuk ka kuptim.
```

---

Analizojeni kodin në vijim:

```cpp
int a;
a = 3;
cout << a << endl;
a = a + 1;
cout << a << endl;
```

Na shfaqet:

```text
3
4
```

---

$$
\underbrace{a}_{\text{Ana e majtë}} = \underbrace{a + 1}_{\text{Ana e djathtë}}
$$

Llogaritet shprehja e djathtë:

$$
\begin{array}{rl}
a &= 3 + 1 \\
a &= 4
\end{array}
$$