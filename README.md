# 🚑 Przewodnik Procedur Medycznych (EMS Field Manual)
**System Medyczny: `xr-ambulancejob`**

Ten dokument jest oficjalną instrukcją operacyjną dla ratowników medycznych i lekarzy. Zawiera szczegółowy opis diagnozowania obrażeń, obsługi aparatury, farmakologii oraz **dokładną kolejność kroków leczenia** wymaganą przez system medyczny.

---

## ⚠️ Złota Zasada Systemu Medycznego

W systemie `xr-ambulancejob` każde obrażenie wymaga podania określonych przedmiotów w **ścisłej, niezmiennej kolejności krok po kroku**.

> **WAŻNE:**
> Próba użycia przedmiotu z pominięciem poprzedniego etapu (np. nałożenie bandaża przed zeszyciem rany) zostanie **odrzucona przez system** komunikatem:
> `❌ Niewłaściwy przedmiot dla tej strefy lub błędny krok procedury.`
> 
> **Pełne wybudzenie z BW (Revive):**
> Pacjent zostanie automatycznie wybudzony dopiero wtedy, gdy:
> 1. Wszystkie rany we wszystkich strefach ciała zostaną **wyleczone do zera**.
> 2. Pacjent posiada **wyczuwalny puls** (jeśli doszło do zatrzymania krążenia, należy użyć defibrylatora po zaopatrzeniu ran).

---

## 📋 Tabela Obrażeń i Sekwencja Leczenia (Krok po Kroku)

Poniższa tabela przedstawia wszystkie obrażenia występujące w systemie wraz z ich lokalizacją, stopniem zagrożenia i **dokładnym algorytmem użycia przedmiotów**:

| Typ Obrażenia | Strefy Ciała | Poziom | Krwawienie | Kolejność użycia przedmiotów (Sekwencja) |
| :--- | :--- | :---: | :---: | :--- |
| **Rana postrzałowa (Styczna)** | Wszystkie | 🟠 Średni | 1 | `1. Gaza` ➔ `2. Zestaw do szycia` ➔ `3. Bandaż` |
| **Rana postrzałowa (Na wylot)** | Wszystkie | 🔴 Ciężki | 2 | `1. Gaza` ➔ `2. Bandaż elastyczny` |
| **Rana postrzałowa (Ślepa - pocisk)** | Wszystkie | 🔴 Ciężki | 2 | `1. Gaza` ➔ `2. Zestaw do szycia` ➔ `3. Bandaż` |
| **Odma opłucnowa** | **Tors** | 🔴 Ciężki | 3 | `1. Opatrunek wentylowy (Chest Seal)` |
| **Rana kłuta (Dźgnięcie)** | Wszystkie | 🔴 Ciężki | 2 | `1. Gaza` ➔ `2. Zestaw do szycia` ➔ `3. Bandaż` |
| **Rana cięta** | Wszystkie | 🟠 Średni | 1 | `1. Zestaw do szycia` ➔ `2. Bandaż` |
| **Złamanie zamknięte** | Kończyny / Tors / Głowa | 🟠 Średni | 0 | `1. Szyna Kramera` ➔ `2. Bandaż elastyczny` |
| **Złamanie otwarte** | Kończyny (Ręce / Nogi) | 🔴 Ciężki | 2 | `1. Staza taktyczna` ➔ `2. Gaza` ➔ `3. Zestaw do szycia` ➔ `4. Szyna Kramera` ➔ `5. Bandaż elastyczny` |
| **Krwotok wewnętrzny** | Tors / Głowa | 🔴 Ciężki | 2 | `1. Worek z krwią (Blood Bag)` |
| **Oparzenie I stopnia** | Wszystkie | 🟢 Lekki | 0 | `1. Maść na oparzenia` |
| **Oparzenie II stopnia** | Wszystkie | 🟠 Średni | 0 | `1. Opatrunek hydrożelowy` ➔ `2. Bandaż` |
| **Siniak / Stłuczenie** | Wszystkie | 🟢 Lekki | 0 | `1. Bandaż elastyczny` |
| **Otarcia naskórka** | Wszystkie | 🟢 Lekki | 0 | `1. Środek odkażający` ➔ `2. Bandaż` |

---

## 🔍 Diagnostyka i Objawy Kliniczne

System generuje realistyczne objawy, które pomagają rozpoznać uraz przed otwarciem poszczególnych partii ciała:

### 1. Odma opłucnowa (`pneumothorax`) — *Priorytet 1 na torsie*
* **Co widać:** Krwawa piana z ust, sinica warg i opuszków palców, niesymetryczne ruchy klatki piersiowej.
* **Badanie miejscowe:** Świszczący dźwięk przy oddechu (zasysanie powietrza przez ranę), brak szmerów oddechowych.
* **Pulsoksymetr:** Spadek saturacji SpO2 do **75–88%**, tachykardia **110–135 BPM**.
* **Działanie:** Natychmiastowe założenie **Opatrunku wentylowego (`chest_seal`)** na Tors!

### 2. Złamanie otwarte (`fracture_open`) — *Priorytet 1 na kończynach*
* **Co widać:** Kość przebijająca skórę, masywny krwotok przez odzież, nienaturalne wygięcie kończyny.
* **Pacjent odczuwa:** Rozdzierający ból, drżenie ciała (wstrząs urazowy), utrata czucia poniżej rany.
* **Działanie:** 
  1. Załóż **Stazę taktyczną (`tourniquet`)** powyżej miejsca złamania, by odciąć krwotok.
  2. Oczyść i osłoń ranę **Gazą (`gauze`)**.
  3. Zbliż tkanki miękkie **Zestawem do szycia (`suture_kit`)**.
  4. Unieruchom kość **Szyną Kramera (`splint`)**.
  5. Całość zabezpiecz **Bandażem elastycznym (`elastic_bandage`)**.

### 3. Krwotok wewnętrzny (`internal_bleeding`)
* **Co widać:** Skrajna bladość twarzy, zimny i lepki pot, przyspieszony płytki oddech, dezorientacja.
* **Badanie miejscowe:** Objaw Cullena / Grey Turnera (zasinienie powłok brzusznych bez rany zewnętrznej), deskowaty, twardy brzuch.
* **Pulsoksymetr:** SpO2 **92–95%**, wysokie tętno **110–140 BPM** (wstrząs hipowolemiczny).
* **Działanie:** Podanie **Worka z krwią (`blood_bag`)** w celu uzupełnienia utraconej objętości krwi.

---

## 🛠️ Sprzęt i Narzędzia Medyczne

### 1. Pulsoksymetr (`pulse_oximeter`)
* **Działanie:** Podpinany na palec pacjenta z poziomu panelu diagnostycznego NUI.
* **Wskazania aparatury:**
  * **SpO2 97–100% / Tętno 70–80 BPM:** Parametry prawidłowe (pacjent stabilny).
  * **SpO2 75–88% / Tętno 110–135 BPM:** Podejrzenie **odmy opłucnowej** (niedotlenienie i duszność).
  * **SpO2 92–95% / Tętno 110–140 BPM:** Podejrzenie **krwotoku wewnętrznego** lub **masywnej rany postrzałowej**.
  * **Tętno 90–105 BPM:** Reakcja stresowa / silny ból (złamanie zamknięte, oparzenie II stopnia).
  * **SpO2 0% / Tętno 0 BPM:** **Brak pulsu / Nagłe Zatrzymanie Krążenia (NZK)** — wymagany defibrylator!

### 2. Defibrylator (`defibrillator`)
* **Zastosowanie:** Używany przy **stwierdzonym braku pulsu** (`hasPulse == false`).
* **Zasady użycia:**
  * Jeśli pacjent **ma puls**, defibrylator zgłosi błąd: *"Pacjent ma już puls, defibrylacja nie jest wymagana"*.
  * Procedura trwa 5 sekund (animacja RKO / masażu serca).
  * Skuteczność pojedynczego impulsu wynosi 50%. W razie niepowodzenia należy ponowić próbę.
  * Pomyślny impuls przywraca akcję serca i oddech. Po wyczyszczeniu wszystkich ran pacjent zostaje wybudzony.

### 3. Pozycja bezpieczna (`turn_on_back` - Interakcja ox_target)
* **Zastosowanie:** Jeśli pacjent leży twarzą w dół (na brzuchu), medyk przez celownik `ox_target` wybiera opcję **"Ustaw w pozycję bezpieczną"**.
* Odwraca to poszkodowanego na plecy, umożliwiając prawidłowy dostęp do dróg oddechowych, torsu i badania aparaturą.

### 4. Rękawiczki lateksowe (`latex_gloves`)
* Środek ochrony indywidualnej ratownika przed skażeniem biologicznym krwią i płynami ustrojowymi.

---

## 💊 Farmakologia (Leki i Płyny Infuzyjne)

Leki posiadają zintegrowane efekty wizualne i fizjologiczne po stronie pacjenta:

| Lek | Wskazania do podania | Działanie w systemie | Efekt wizualny pacjenta |
| :--- | :--- | :--- | :--- |
| **Adrenalina (`epinephrine`)** | Wstrząs, zapaść, bradykardia, po udanej defibrylacji. | Zwiększa rzut serca, pobudza krążenie. | PostFX Rampage (czerwona poświata, zastrzyk energii). |
| **Morfina (`morphine`)** | Skrajny, rozdzierający ból (złamania otwarte, postrzały). | Całkowicie znosi odczuwanie bólu przez poszkodowanego. | Zmiękczenie obrazu (drug_flying_base), uspokojenie. |
| **Nalokson (`naloxone`)** | Przedawkowanie morfiny / opioidów, depresja oddechowa. | Błyskawiczne odwrócenie działania morfiny i narkotyków. | Efekt rozjaśnienia ekranu (SuccessMichaelFade). |
| **Środek usypiający (`sedative`)** | Panika, wstrząs pourazowy, agresja, przygotowanie do operacji. | Uspokojenie i wyciszenie układu nerwowego. | Efekt przyciemnienia i uśpienia (deathfail). |
| **Sól fizjologiczna (`saline`)** | Utrata płynów, odwodnienie, wstrząs hipowolemiczny. | Uzupełnienie łożyska naczyniowego, stabilizacja ciśnienia. | Subtelny filtr stabilizacyjny (chop_cam). |
| **Worek z krwią (`blood_bag`)** | **Krwotok wewnętrzny**, ciężka anemia pokrwotoczna. | Wymagany element leczenia krwotoków wewnętrznych. | Regeneracja sił witalnych i dotlenienie tkanek. |
| **Krople żołądkowe (`stomach_drops`)** | Nudności, wymioty, podrażnienia żołądkowe. | Neutralizacja mdłości i odruchów wymiotnych. | Łagodny filtr wyciszający żołądek. |

---

## 🧑‍⚕️ Standardowy Algorytm Działań Ratowniczych (Procedura Krok po Kroku)

Podczas przyjazdu na miejsce wezwania zaleca się stosowanie poniższego schematu:

```
[1. Zabezpieczenie & BHP] 
   └── Założenie rękawiczek lateksowych. Podejście do pacjenta.

[2. Pozycja & Dostęp]
   └── Jeśli leży na brzuchu ➔ Użyj ox_target: "Ustaw w pozycję bezpieczną".

[3. Otwarcie Panelu Medycznego]
   └── ox_target na poszkodowanym ➔ "Pomoc medyczna". Kamera zbliża się na pacjenta.

[4. Wstępna Diagnostyka (ABC)]
   └── Sprawdź pulsoksymetrem (Pulse Oximeter) tętno i SpO2:
       ├── Tętno = 0 / SpO2 = 0 ➔ Brak pulsu! Przygotuj defibrylator.
       ├── SpO2 < 90% ➔ Szukaj natychmiast odmy na Torsie!
       └── Tętno > 120 ➔ Szukaj krwotoków wewnętrznych lub otwartych ran.

[5. Zaopatrzenie Urazów Zagrażających Życiu]
   ├── Odma opłucnowa (Tors) ➔ Nałóż Opatrunek Wentylowy (Chest Seal).
   ├── Złamanie otwarte ➔ Krok 1: Staza Taktyczna (Tourniquet) na krwawiącą kończynę!
   └── Krwotok wewnętrzny ➔ Podaj Worek z krwią (Blood Bag).

[6. Zaopatrzenie Pozostałych Ran (Sekwencyjnie)]
   └── Otwieraj kolejne strefy ciała i aplikuj przedmioty zgodnie z tabelą:
       • Postrzały: Gaza ➔ Zestaw do szycia ➔ Bandaż
       • Złamania zamknięte: Szyna Kramera ➔ Bandaż elastyczny
       • Oparzenia II st.: Opatrunek hydrożelowy ➔ Bandaż
       • Otarcia: Środek odkażający ➔ Bandaż

[7. RKO i Wskrzeszenie (Gdy rany są zaopatrzone)]
   ├── Jeśli pacjent nie miał pulsu ➔ Użyj Defibrylatora (`defibrillator`).
   └── Gdy wszystkie rany zostaną wyzerowane i powróci puls ➔ Pacjent zostaje automatycznie ożywiony!
```

---

*Dokument sporządzony na potrzeby frakcji medycznej serwera. Wersja zgodna z rdzeniem skryptu `xr-ambulancejob`.*
