## Gjuhë Programuese

Edon Gashi

edon.gashi@uni-pr.edu

edongashi.github.io

---

### Kompjuteri

Pajisje e cila kryen punë të dobishme.

- Procesori - kryen punë
- Memoria - mban në mend
- Hyrja/Dalja - komunikon me botën

---

### Programi

Një varg urdhërash që ekzekutohen (ndjeken) nga kompjuteri.

- Word, Excel, PowerPoint
- Google Chrome, Mozilla Firefox
- Visual Studio
- Me mijëra tjera...

---

Programet shkruhen përmes **gjuhës programuese**.

Gjuha programuese është urë lidhëse mes programerit dhe kompjuterit.

Sikur gjuhët e njerëzve, gjuhët programuese i kanë rregullat dhe karakteristikat e veta.

---

### Kompajlleri

Kompajlleri është program i cili përkthen gjuhën programuese në gjuhë të makinës.

Gjuha e makinës është varg i njësheve dhe zerove.

---

Secili program ka:

1. Pikën e nisjes **main**
2. Hyrjen dhe daljen standarde*

*(standard input / standard output)

---

**main** paraqet pikën nga e cila fillon ekzekutimi i urdhërave.

Programi përfundon kur ekzekutohen të gjithë urdhërat që gjenden në **main**.

---

Kur përfundon ekzekutimi i **main**, programi kthen një numër për ta treguar statusin e gabimit - error code

- Vlera **0** tregon që nuk ka pasur gabim
- Vlerat **tjera** tregojnë që ka pasur gabim

Shumicën e rasteve do ta vendosni statusin **0**.

---

Si duket main në gjuhën programuese C++?

```cpp
int main() {
  return 0;
}
```

Ky program nuk bën asgjë. Vetëm ekzekutohet dhe tregon që është ekzekutuar me sukses.

---

Anatomia e programit

$$
\texttt{int main()}\;\lbrace\;\textit{blloku}\;\rbrace
$$

**Bllok** quhet një varg i urdhërave.

---

Në C++ blloku i urdhërave mbështjellet në kllapa gjarpërore.

```cpp
{
  urdhër;
  urdhër;
  urdhër;
  return 0;
}
```

Urdhërat brenda bllokut ndahen me pikëpresje.

Hapësirat dhe rreshtat e rinj nuk kanë rëndësi. Ato përdorën për ta bërë kodin më të lexueshëm.

---

$$
\overbrace{\color{red}{\texttt{int}}}^{\text{tipi i bllokut}}\texttt{ main() { ... }}
$$


**int** - Shkurtesë për **integer** (shqip: numër i plotë)

Tregon që main (programi) kthen një numër të plotë - **error code**.

---

$$
\texttt{int }\overbrace{\color{red}{\texttt{main}}}^{\text{emri i bllokut}}\texttt{() { ... }}
$$

Blloku hyrës gjithmonë duhet ta ketë emrin "main".

Në të ardhmën do të krijojmë edhe blloqe tjera - funksione. Për fillim do të merremi vetëm me **main**.

---

$$
\texttt{int main}\overbrace{\color{red}{\texttt{()}}}^{\text{parametrat}}\texttt{{ ... }}
$$

Në kllapa futen parametrat, por për main nuk na nevojiten. Prandaj lihen të zbrazëta.

Do të shpjegohen më vonë më detajisht.

---

```cpp
int main() {
  return 0;
}
```

Urdhëri $\;\color{red}{\texttt{return 0;}}\;$ ka kuptimin "kthe zero" - programi i ekzekutuar nuk ka gabim.

Me kohën do të mësojmë urdhëra tjerë.

---

**Komenti** na lejon të shkruajmë shpjegime ose shënime tjera në kod.

```cpp
int main() {
  // Rreshti në vijim kthen statusin 0
  return 0;
}
```

Kompajllerit nuk i intereson për komente - ato injorohen.

---

Komentet shkruhen në dy mënyra.

Mënyra e parë është me `//`

```cpp
int main() {
  return 0; // Ky tekst injorohet nga kompajlleri
  // Edhe ky tekst injorohet
}
```

Kur vendoset sekuenca "//", gjithçka pas saj në atë rresht injorohet.

---

Mënyra e dytë për komente

```cpp
int main() {
  /* Ky koment shtrihet
  në disa rreshta. */
  return 0;  
}
```

Komenti vendoset brenda sekuencës `/* ... */`.

Kjo mënyrë e lejon komentin të shtrihet në disa rreshta.

---

### Hyrja dhe dalja standarde

Më herët u cek që programi ka **hyrjen** dhe **daljen** standarde.

**Hyrja** mundëson leximin e informacionit.

**Dalja** mundëson shkruarjen e informacionit.

Anglisht: **standard input** dhe **standard output**.

---

Në C++, hyrja dhe dalja standarde gjenden në librarinë **iostream**.

$$
\overbrace{\texttt{i}}^{\text{input}}
\underbrace{\texttt{o}}_{\text{output}}
\texttt{stream}
$$

**stream** ka kuptimin e rrjedhës - burimi i informacionit ose rrjedha e informacionit.

---

Hyrja standarde është objekti `std::cin`

Dalja standarde është objekti `std::cout`

- std - standard
- cin - character input
- cout - character output

---

Nga `std::cin` lexohet me operatorin `>>`

```
std::cin >> x;
```

Kjo ka kuptimin

$$
\textit{standard input}\xrightarrow{lexo} x
$$

Merr nga standard input dhe vendose në $x$.

---

Në `std::cout` shkruhet me operatorin `<<`

```
std::cout << "Pershendetje";
```

Kjo ka kuptimin

$$
\textit{standard output}\xleftarrow{shkruaj}\text{"Pershendetje"}
$$

Shkruaj tekstin "Pershendetje" në standard output.

---

Shembulli i plotë

```cpp
#include <iostream>

int main() {
  std::cout << "Pershendetje";
  return 0;
}
```

Pas ekzekutimit, në dritare shfaqet

```cpp
Pershendetje
```

---

Rreshti `#include <iostream>` ka kuptimin:

Përfshije librarinë `iostream`, pasi që programi im ka nevojë të shkruajë ose të lexojë nga hyrja/dalja.

```cpp
#include <iostream>

int main() {
  std::cout << "Pershendetje";
  return 0;
}
```

---

```cpp
#include <iostream>

int main() {
  std::cout << "Pershendetje";
  return 0;
}
```

Programi i sipërm mund të shënohet si më poshtë

```cpp
#include <iostream>
using namespace std;

int main() {
  cout << "Pershendetje";
  return 0;
}
```

---

`using namespace std;` e largon nevojën e shkruarjes së parashtesës `std::` çdo herë që dëshirojmë të komunikojmë me `cin` ose `cout`.

---

```cpp
#include <iostream>

int main() {
  std::cout << "Pershendetje!\n";
  std::cout << "Mire se vini.";
  return 0;
}
```

Në ekran shfaqet:

```cpp
Pershendetje!
Mire se vini.
```

---

```cpp
#include <iostream>
using namespace std;

int main() {
  cout << "Pershendetje!\n";
  cout << "Mire se vini.";
  return 0;
}
```

Në ekran shfaqet:

```cpp
Pershendetje!
Mire se vini.
```

---

Teksti në shembujt e kaluar u fut në thonjëza.

```cpp
"Pershendetje"
```

Kjo është e nevojshme për ta dalluar urdhërin nga teksti i zakonshëm.

---

Në tekst që shkruhet në kod, nuk kemi mundësi të vendosim rresht të ri duke shtypur enter.

Për të treguar që në tekst gjendet rreshti i ri, përdoret karakteri special `\n`, ku `n` e ka kuptimin "newline".

```cpp
cout << "Pershendetje!\nMire se vini.";
```

Në ekran shfaqet:

```cpp
Pershendetje!
Mire se vini.
```

---

Ekzistojnë disa karaketere tjera speciale. Karakteret që fillojnë me "\" kanë kuptim të veçantë.

Karakteri|Kuptimi
-|-
`\n`|Rresht i ri
`\t`|Tab
`\'`|Thonjëza e njëfishtë
`\"`|Thonjëza e dyfishtë
`\\`|Vetë karakteri \\

Dhe tjera...

---

Shembull

```cpp
// Importo librarine iostream
#include <iostream>
using namespace std;

// Pika hyrese e programit
int main() {
  cout << "Rreshti i pare" << "\n" << "Rreshti i dyte";
  return 0;
}
```

Rezultati në ekran

```cpp
Rreshti i pare
Rreshti i dyte
```

Siç po shihet më lartë, mund të lidhen operatorët `<<` njëri pas tjetrit.

---

### Tipet e të dhënave

Ekzistojnë disa lloje të të dhënave. Kryesoret:

Emri|Përshkrimi|Shembuj
-|-
int|Numër i plotë|$-2,\,0,\,3,\,15$
float|Numër me presje|$-1.2,\,0.0,\,3.5$
char|Karakter i vetëm|$\texttt{'a'},\,\texttt{'b'},\,\texttt{'\n'}$
string|Varg i karaktereve (tekst)|$\texttt{"Pershendetje"}$
bool|Vlerë e vërtetësisë|$\texttt{true},\,\texttt{false}$
