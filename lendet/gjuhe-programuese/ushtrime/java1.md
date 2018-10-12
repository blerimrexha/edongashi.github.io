## Instalimi i Visual Studio

1. Vizitojmë faqen [visualstudio.microsoft.com](https://visualstudio.microsoft.com/).
2. Te `Visual Studio IDE`, e zgjedhim `Community 2017`.
3. Klikojmë butonin dhe presim deri të shkarkohet.
4. Ndjekim hapat e instalimit, dhe sigurohemi që kemi zgjedhur opsionin `Desktop Development with C++` gjatë instalimit.

---

<!-- .slide: style="font-size:0.6em;" -->

## Krijimi i projektit

1. Hapim Visual Studio.
2. Shkojmë te `File > New > Project`.
3. Te lista e gjuhëve, kërkojmë gjuhën `Visual C++`.
4. Te lloji i projektit, e kërkojmë njërën nga këto:
   - Për Visual Studio 2017, e zgjedhim `Windows Desktop Wizard`.
   - Për versione më të vjetra, e zgjedhim `Win32 Project`.
5. Te shtegu i projektit, e zgjedhim dosjen ku dëshirojmë ta ruajmë projektin. Këtë e bëjmë duke shtypur butonin `Browse`.
6. E vendosim emrin e projektit, psh. `Ushtrimi1`.
7. E shtypim `OK`.
8. Na shfaqet dritarja për të konfiguruar projektin.
    - E zgjedhim opsionin `Empty Project`
    - Tek `Application Type` e zgjedhim `Console Application`
9. Shtypim `OK`.

---

## Krijimi i fajllit burimor

<!-- .slide: style="font-size:0.6em;" -->

1. Pasi ta kemi hapur projektin, në anën e djathtë e shohim `Solution Explorer`.
    - Nëse nuk e shohim, shkojmë te `View > Solution Explorer` për ta shfaqur.
2. Te projekti ynë, i shohim katër dosje. Dosjen `Source Files` e hapim me tastin e djathtë, dhe shkojmë te `Add > New Item`
3. Na hapet menyja për krijimin e fajllave. E zgjedhim `C++ File (.cpp)`, dhe ia lëmë emrin sipas dëshirës, psh `programi.cpp`. E shtypim `OK`.
4. Te dosja `Source Files` na shfaqet fajlli i sapo-krijuar. E klikojmë dy herë dhe na shfaqet editori.

---

## Programi fillestar

Në editor, shkruajmë këtë kod:

```cpp
#include <iostream>
using namespace std;

int main() {
  cout << "Pershendetje!" << endl;
  return 0;
}
```

Pas ekzekutimit shfaqet:

```text
Pershendetje
Press any key to continue...
```

---

<!-- .slide: style="font-size:0.6em;" -->

## Ekzekutimi i programit

1. Shkojmë te `Debug > Start Without Debugging`.
    - Këtë veprim mund ta bëjmë edhe duke shtypur `Ctrl+F5`.
2. Nëse kodi është në rregull, programi kompajllohet dhe shfaqet dritarja e aplikacionit.
3. Nëse kemi gabime, na del një njoftim që programi nuk ka mundur të kompajllohet. E shtypim `No` për t'u kthyer te editori.
4. Rikthehemi te editori dhe korigjojmë gabimet.
    - Dritarja `Error List` na ndihmon në gjetjen e gabimeve. Gabimet mund t'i klikojmë dy herë me tastin e majtë për të na dërguar te rreshti i kodit tek i cili gjendet problemi.
5. Pasi t'i kemi korigjuar gabimet, kthehemi te hapi 1.

---

## Mbyllja e projektit

1. Shkojmë te `File > Close Solution`.
    - Nëse kemi ndryshime të paruajtura, na pyet nëse dëshirojmë t'i ruajmë para se ta mbyllim projektin.

---

## Rihapja e projektit

1. Shkojmë te `File > Open > Project/Solution`.
2. E kërkojmë shtegun e projektit tonë.
3. Brenda dosjes së projektit, e zgjedhim `.sln` fajllin i cili mban emrin e projektit.
4. Shtypim `Open` dhe na hapet projekti. 