# Zarządzanie projektami informatycznymi

Przedmiot: **ZPI**

Semestr: **Zima 2022**

Temat: **System wspomagający działanie urzędu stanu cywilnego**

Zespół:
```
Brzozowski Mateusz
Krawczyk Bartłomiej
Topczewska Gabriela
```

## Czym się zajmuje?

- rejestracja: urodzeń, małżeństw, zgonów

- dokonywanie zmian w księgach na podstawie

- przyjmowanie oświadczeń o zawarciu związku małżeńskiego


- rejestracja

## Założenia

Dokumentacja analityczna powstająca w ramach projektu informatycznego stanowi środek komunikacji i efekt porozumienia pomiędzy przyszłym użytkownikiem tego systemu a zespołem informatycznym: projektantami i programistami.

Dokumentacja powinna zostać przygotowana w taki sposób, aby:
1. Użytkownicy posiadający wiedzę specyficzną dla dziedziny zastosowań byli w stanie potwierdzić, że dokumentacja ta prawidłowo opisuje procesy, których realizację będzie wspomagał system informatyczny oraz właściwie określa funkcje tego systemu.
2. Projektanci i programiści byli w stanie, jedynie na podstawie tej dokumentacji, zaproponować zgodną z oczekiwaniami użytkownika implementację opisanych w dokumentacji analitycznej funkcji systemu.

# Modelowanie procesów biznesowych

## Cel

Rozdział dokumentu powinien opisywać kluczowe procesy biznesowe zachodzące w przedsiębiorstwie.

Przedsiębiorstwo lub organizacja pełnią rolę środowiska, w którym działał będzie projektowany system informatyczny.

Należy uwzględnić tylko te procesy, które na jakimś etapie (jedna lub więcej czynności w ramach procesu) będą wspierane przez system informatyczny. Można ograniczyć liczbę procesów do 3–5 (nietrywialnych).

## Wyniki prac

### Lista wykonawców czynności
lista wszystkich `wykonawców czynności` w ramach procesów biznesowych wraz z ich zwięzłym i precyzyjnym opisem.


### 1. Zmiana imienia/nazwiska
<!-- Mateusz Brzozowski -->

### 2. Narodziny
<!-- Bartłomiej Krawczyk -->

### 3. Ślub cywilny
<!-- Gabriela Topczewska -->

### 4. Zgon
<!-- Bartłomiej Krawczyk -->

Wykonawcy czynności:
- zmarły
    - umiera :o
- lekarz
    - lekarz może stwierdzić zgon na podstawie osobiście wykonanych badań i ustaleń, zaś w uzasadnionych przypadkach lekarz (z wyłączeniem lekarza dentysty) może uzależnić wystawienie karty zgonu od przeprowadzenia sekcji zwłok
    - wystawia kartę zgonu
- osoby związane ze zmarłą osobą
    - może to być:
        - współmałżonek osoby, która zmarła,
        - pozostała rodzina zmarłej osoby, na przykład dzieci, wnuki, prawnuki, rodzice, dziadkowie, brat, siostra, siostrzenica, bratanek, teściowie,
        - pełnomocnik jednej z powyższych osób.
    - zgłaszają śmierć osoby zmarłej do urzędu stanu cywilnego
    - we wniosku powinni zawrzeć:
        - kartę zgonu - od lekarza, który stwierdził zgon
        - dowód osobisty zmarłej osoby,
        - własny dokument tożsamości do okazania (potwierdzenie pełnomocnictwa)
- kierownik urzędu stanu cywilnego
    - rejestruje zgon - sporządzi akt zgonu - w dniu zgłoszenia
    - po rejestracji dostarcza bezpłatny odpis aktu zgonu
    - wnioski należy składać we właściwym urzędzie dla miejsca zgonu
    - po zgłoszeniu zgonu unieważniany jest dowód osobisty oraz następuje automatyczne wymeldowanie zmarłej osoby z miejsca pobytu stałego lub czasowego
- administracja cmentarza
    - na podstawie aktu zgonu decyduje o pochowaniu zmarłego

### Specyfikacje procesów biznesowych
zwięzły opis poszczególnych procesów biznesowych oraz specyfikacje czynności wykonywanych w ramach poszczególnych procesów zapisane jako diagramy aktywności (ang.activity diagram) w notacji UML. Na diagramach należy podać wykonawców czynności, korzystając z torów (ang. swimlanes) lub boksów. Ponadto, należy w szczególny sposób oznaczyć czynności (węzły diagramów), które wspierać będzie projektowany system informatyczny, np. opatrując je stereotypem **\<\<system\>\>**.

https://mermaid-js.github.io/mermaid/#/stateDiagram

### 1. Zmiana imienia/nazwiska
<!-- Mateusz Brzozowski -->

### 2. Narodziny
<!-- Bartłomiej Krawczyk -->

### 3. Ślub cywilny
<!-- Gabriela Topczewska -->

### 4. Zgon
<!-- Bartłomiej Krawczyk -->


```mermaid
stateDiagram
    [*] --> s
    state Zmarły {
        direction LR
        state "śmierć" as s
    }
    state Lekarz {
        direction LR
        state "Badania" as b
        state "Sekcja zwłok" as sz
        state "Wystawienie karty zgonu" as kz
        state "Decyzja o powodzie śmierci" as d
        b --> sz
        sz --> kz
        kz --> d: Karta zgonu

        state if_state <<choice>>
        d --> if_state
        if_state --> Nie: Zmarł na skutek choroby zakaźnej
        if_state --> Tak: Zmarł na skutek choroby zakaźnej
    }
    state Bliscy {
        state "Dostarczenie karty zgonu oraz dokumentów do urzędu stanu cywilnego" as w
        state "Odbiór odpisu od aktu zgonu" as b2
        state "Przekazanie aktu zgonu do administracji cmentarza" as b3

        b2 --> b3
    }
    state "Kierownik urzędu" as kierownik {
        state "Zarejestrowanie zgonu" as k1
        state "Przygotowanie aktu zgonu" as k2
        state "<<\system>>" as k2
        state "Wprowadzenie zgonu do systemu" as k3
        state "<<\system>>" as k3
        state "Automatyczne wymeldowanie oraz unieważnienie dokumentów" as k4
        state "<<\system>>" as k4
        state "Przygotowanie odpisu do Aktu zgonu" as k5

        k1 --> k2
        k2 --> k3
        k3 --> k4
        k4 --> k5
    }
    state "Administracja cmentarza" as administracja {
        state "Wypełnienie formalności oraz zajęcie się zmarłym" as c1
    }
    s --> b

    Nie --> w : 3 Dni
    Tak --> w : 24h

    w --> k1: Karta zgonu, Dowód zmarłego, Własny dowód tożsamości

    k5 --> b2: Odpis aktu zgonu
    b3 --> c1: Odpis aktu zgonu

    c1 --> [*]: Pogrzeb
```


Zanim pochowasz osobę, która zmarła, musisz zgłosić jej zgon w urzędzie stanu cywilnego (USC). Masz na to 3 dni od dnia wystawienia karty zgonu. Jeśli osoba ta zmarła na skutek choroby zakaźnej – tylko 24 godziny od momentu zgonu. Sprawdź, jak możesz to zrobić.

## Kto może zgłosić śmierć:
- współmałżonek osoby, która zmarła,
- pozostała rodzina zmarłej osoby, na przykład dzieci, wnuki, prawnuki, rodzice, dziadkowie, brat, siostra, siostrzenica, bratanek, teściowie,
- pełnomocnik jednej z powyższych osób.

## Co musisz przygotować
- kartę zgonu – dostaniesz ją od lekarza, który stwierdził zgon,
- dowód osobisty zmarłej osoby,
- swój dokument tożsamości do okazania (np. dowód osobisty lub paszport).

## Gdzie zgłaszasz

W USC właściwym dla miejsca zgonu. Przykład: jeśli osoba zmarła w Sopocie – zgłoś zgon w urzędzie stanu cywilnego w Sopocie.

## Ile będziesz czekać

Kierownik USC zarejestruje zgon (czyli sporządzi akt zgonu) w dniu jego zgłoszenia.

Po zarejestrowaniu zgonu kierownik USC wyda ci jeden bezpłatny odpis skrócony aktu zgonu.

Jeśli z przyczyn technicznych rejestracja zgonu nie będzie możliwa w dniu zgłoszenia, kierownik USC zamieści w karcie zgonu adnotację o zgłoszeniu zgonu. Z tym dokumentem możesz pójść do administracji cmentarza, żeby pochować osobę zmarłą. Kierownik USC zarejestruje zgon w najbliższym możliwym terminie. Następnie dostaniesz dwa odpisy aktu zgonu. Ustal z urzędnikiem sposób ich odbioru. Możesz je dostać podczas kolejnej wizyty w urzędzie albo listownie. Jeden odpis jest dla ciebie, drugi przekaż administracji cmentarza.

## Informacje dodatkowe
Gdy zgłosisz zgon, osoba zmarła zostanie automatycznie wymeldowana z miejsca pobytu stałego lub czasowego, a jej dowód osobisty zostanie unieważniony.



# Modelowanie przypadków użycia

## Cel 
Rozdział dokumentu powinien opisywać specyfikację interakcji (dialogu) użytkowników z projektowanym systemem informatycznym, umożliwiając zaprojektowanie jego interfejsu i sporządzenie makiety tego systemu.

## Wyniki prac

### Lista aktorów systemowych 
lista użytkowników i systemów informatycznych `podejmujących interakcję` z projektowanym systemem.

### Diagramy przypadków użycia systemu
sporządzone zgodnie z notacją UML diagramy ilustrujące przypadki użycia systemu i ich związki z odpowiednimi aktorami, oraz zależności pomiędzy przypadkami użycia (**\<\<include\>\>**,**\<\<extend\>\>**, generalizacja/specjalizacja).

### Specyfikacje przypadków użycia systemu
specyfikacje przebiegu interakcji w obrębie poszczególnych przypadków użycia w postaci opisu scenariusza głównego (podstawowego), scenariuszy alternatywnych i punktów rozszerzeń.

### Projekty ekranów
graficzny szkic lub zrzut z ekranu komputera, ekranu/formularza służącego do wprowadzania danych lub wybierania opcji przez użytkownika w ramach danego przypadku użycia.

<!-- Mateusz Brzozowski -->

**Uwaga:** Dla każdego przypadku użycia na diagramie należy opracować jego specyfikację oraz projekt ekranu (jeśli z przypadkiem użycia wiąże się wprowadzanie danych, wybieranie opcji).

# Modelowanie pojęć systemu

## Cel
Rozdział dokumentu powinien opisywać specyfikację pojęć związanych z projektowanym systemem.

## Wyniki prac

### Diagram klas
diagram klas przedstawiający pojęcia dotyczące projektowanego systemu informatycznego, sporządzony zgodnie z notacją UML. Specyfikacje klas (pojęć) powinny obejmować specyfikacje atrybutów,dla których należy wyspecyfikować odpowiedni typ niezwiązany jednak z określoną platformą implementacji, np. LiczbaCałkowita, LiczbaRzeczywista, Data, Napis itp. Należy wyspecyfikować związki pomiędzy klasami: związek asocjacji (i ew. jej szczególne przypadki - agregację i kompozycję) wraz z licznością końców, oraz związek generalizacji/specjalizacji. 

### Specyfikacja klas
zwięzły opis znaczenia poszczególnych klas i ich atrybutów.

**Uwaga:** Nie podajemy operacji dla klas. Każda asocjacja musi być nazwana.
