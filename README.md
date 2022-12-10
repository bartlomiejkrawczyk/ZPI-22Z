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
Wykonawcy czynności:
- osoba zmieniająca imię lub nazwisko
    - chce zmienić imię lub nazwisko
    - kto może:
        - pełnoletni obywatel polski
        - pełnoletni cudzoziemiec niemający obywatelstwa żadnego państwa, jeżeli ma w Polsce miejsce zamieszkania
        - pełnoletni cudzoziemiec, który uzyskał w Polsce status uchodźcy
        - osoba małoletnia, której rodzice zmienili nazwisko
        - osoba niepełnoletnia, która ukończyła 13 rok życia na wniosek jednego z rodzica
- rodzic
    - składa wniosek o zmianę nazwiska albo imienia osoby niepełnoletniej
    - wyraża zgodę na wniosek drugiego rodzica, jeżeli niepełnoletni ukończył 13 rok życia
- kierownik urzędu stanu cywilnego
    - odbiera wniosek o zmianę imienia lub nazwiska
    - akceptuje bądź odrzuca wniosek
    - przekazuje informacje do innych kierowników urzędów stanu cywilnego w celu nasienia zmiany do aktu urodzenia  i aktu małżeństwa
    - wprowadza zmiany w aktach stanu cywilnego osób

### 2. Narodziny
<!-- Bartłomiej Krawczyk -->

Wykonawcy czynności:
- nowo narodzone dziecko
    - rodzi się
- rodzic / pełnomocnik
    - może to być:
        - matka lub ojciec dziecka, którzy mają ukończone 16 lat i nie zostali pozbawieni zdolności do czynności prawnych,
        - w pozostałych sytuacjach, na przykład jeśli matka dziecka ma mniej niż 16 lat lub została pozbawiona zdolności do czynności prawnych – dla przedstawiciela ustawowego (na przykład rodzica) lub opiekuna matki dziecka.
        - Urodzenie dziecka można zgłosić samodzielnie lub może zrobić to pełnomocnik.
    - należy przygotować:
        - dokument tożsamości
        - pełnomocnictwo (w przypadku skorzystania z pełnomocnika)
    - ma 21 dni na rejestrację dziecka w urzędzie
- osoba, która odebrała poród
    - lekarz lub położna
    - wystawia kartę urodzenia
    - ma 3 dni na przekazanie jej do urzędu stanu cywilnego
- kierownik urzędu stanu cywilnego
    - rejestruje urodzenie dziecka
    - przygotowuje protokół, który zawiera dane rodziców
    - rejestruje urodzenie dziecka, deklaruje zameldowanie oraz przydziela numer PESEL

### 3. Ślub cywilny
<!-- Gabriela Topczewska -->

Wykonawcy czynności:
- narzeczeni
    - osoby planujące zawarcie związku małżeńskiego
    - dokonują opłaty skarbowej
    - przygotowują wymagane dokumenty:
        - dokumenty tożsamości
        - jeśli jest potrzebne – zezwolenie sądu na zawarcie małżeństwa,
        - dowód opłaty skarbowej
        - zezwolenie sądu na zawarcie małżeństwa - jeśli wymagane
        - pełnomocnictwo - w przypadku korzystania z pełnomocnika
        - akta stanu cywilnego
    - udają się do urzędu dopełnić formalności na co najmniej miesiąc przed planowaną datą ślubu
    - ustalają datę ślubu
    - składają pisemne zapewnienie o nieistnieniu okoliczności wykluczających zawarcie małżeństwa
    - pobierają się
- urzędnik USC
    - sprawdza poprawność i prawdziwość danych na dokumentach zaręczonych
    - przygotowuje wymagane dokumenty i formularze do wypełnienia przez zaręczonych
    - sprawdza dostępność dat ślubu
    - rejestruje wybraną datę ślubu
- organ sądowy
    - udziela zgody sądu na zawarcie małżeństwa, kiedy prawdziwy jest którykolwiek z poniższych przypadków:
        - kobieta jest niepełnoletnia, ale ukończyła 16 lat,
        - osoby są ze sobą spowinowacone,
        - osoba jest dotknięta chorobą psychiczną albo niedorozwojem umysłowym
- tłumacz
    - w przypadku obcojęzyczności któregoś z przyszłych małżonków obowiązkowo udziela tłumacznia w urzędzie
    - w przypadku dokumentó osobistych obcojęzycznych
- urzędnik udzielający ślubu
    - udziela ślubu zaręczonym po wcześniejszym spełnieniu wszystkich wymogów formalnych przez małżonków

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

```mermaid
stateDiagram
    [*] --> z1 : osoba pełnoletnia
    state "Osoba zmieniająca imię lub nazwisko" as zmieniający{
        direction LR
        state "Złożenie wniosku" as z1
        state "Wskazanie miejsca sporządzenia aktu urodzenia" as z2
        state "Wskazanie miejsca sporządzenia aktu małżeństwa" as z3
        state if_mmalzenstwa <<choice>>
        state if_pol <<choice>>
        state "Złożenie wniosku o przeniesienie zagranicznych dokumentów stanu cywilnego" as z4
    }

    [*] --> p1 : osoba niepełnoletnia
    p1 --> z2
    z1 --> z2
    z2 --> if_mmalzenstwa
    if_mmalzenstwa --> z3 : posiadanie aktu małżeństwa
    if_mmalzenstwa --> if_pol : brak aktu małżeństwa
    if_pol --> z4 : brak polskiego obywatelstwa
    if_pol --> k1 : obywatel polski
    z4 --> k1
    z3 --> if_pol

    state "Pierwszy przedstawiciel ustawowy" as przedstawiciel1{
        direction LR
        state "Złożenie wniosku dotyczącego małoletniego dziecka" as p1
    }

    state "Kierownik urzędu realizujący zmianę imienia/nazwiska" as kierownik1{
        direction LR
        state "Sprawdzenie poprawności dokumentów" as k1
        state if_akcept <<choice>>
        state "Wydanie zgody" as k2
        state "Przekazanie informacji o zmianie do pozostałych kierowników urzędu" as k3
    }

    k1 --> if_akcept
    if_akcept --> k2 : zaakceptowanie wniosku
    if_akcept --> [*] : odrzucenie wniosku
    k2 --> k3
    k3 --> k11

    state "Kierownik urzędu zarządzający aktami" as kierownik2{
        direction LR
        state "Wprowadzenie zmian w akcie urodzenia" as k11
        state if_malzenstwo <<choice>>
        state "Wprowadzenie zmian w akcie akcie małżeństwa" as k12
    }

    k11 --> if_malzenstwo
    if_malzenstwo --> k12 : posiadanie aktu małżeństwa
    if_malzenstwo --> [*] : brak aktu małżeństwa

    k12 --> [*]
    k11 --> [*]
```

### 2. Narodziny
<!-- Bartłomiej Krawczyk -->

```mermaid
stateDiagram
    [*] --> r1
    state Dziecko {
        direction LR
        state "Rodzi się" as r1
    }
    state Lekarz {
        direction LR
        state "Odbiór porodu" as l1
        state "Przygotowanie karty urodzenia" as l2
        state "Przesłanie karty urodzenia do urzędu stanu cywilnego" as l3

        l1 --> l2
        l2 --> l3
    }

    r1 --> l1

    state Bliscy {
        state "Wizyta w urzędzie" as b1
        state "Odbiór dokumentów" as b2
    }
    state "Kierownik urzędu" as kierownik {
        state "Przygotowanie protokołu" as k1
        state "<<\system>>" as k1
        state "Zarejestrowanie urodzenia dziecka" as k2
        state "<<\system>>" as k2
        state "Zameldowanie dziecka" as k3
        state "<<\system>>" as k3
        state "Nadanie numeru PESEL" as k4
        state "<<\system>>" as k4
        state "Przygotowanie aktu urodzenia" as k5
        state "<<\system>>" as k5
        state "Przekazanie dokumentów rodzicom" as k6

        k1 --> k2
        k2 --> k3
        k3 --> k4
        k4 --> k5
        k5 --> k6
    }

    state fork_state <<fork>>
      l3 --> fork_state
      fork_state --> b1

      state join_state <<join>>
      b1 --> join_state: 21 Dni
      join_state --> k1
      fork_state --> join_state: 3 Dni

    k6 --> b2: Skrócony akt urodzenia, numer PESEL, potwierdzenie zameldowania
    b2 --> [*]: Rejestracja dziecka
```

### 3. Ślub cywilny
<!-- Gabriela Topczewska -->

```mermaid
stateDiagram
    [*] --> a
    state Narzeczeni {
        direction LR;
        state "Pobranie akt stanu cywilnego" as a
        state "<<\system>>" as a
        state if_sad_state <<choice>>
        state "Złożenie wniosku o uzyskanie pozwolenia sądu" as wsa
        state "Uzyskanie decyzji sądu" as sa
        state if_zgoda <<choice>>
        state if_pol_state <<choice>>
        state "Złożenie dokumentów do przetłumaczenia" as p1
        state "Odebranie przetłumaczonych dokumentów" as p2
        state "Dokonanie opłaty skarbowej" as o
        state "<<\system>>" as o
        state "Złożenie dokumentów w urzędzie" as u
        state "Zaproponowanie daty ślubu" as zd
        state if_data_state <<choice>>
        state "Potwierdzenie daty ślubu" as pd
        state "Złożenie pisemnego oświadczenia o braku czynności wyłączających zawarcie małżeństwa" as osw
        state "Zawarcie małżeństwa" as m
        state "Odwołanie ślubu" as odw

        a --> if_sad_state
        if_sad_state --> if_pol_state : Czy zgoda sądu wymagana? - Nie
        if_sad_state --> wsa : Czy zgoda sądu wymagana? - Tak
        sa --> if_zgoda
        if_zgoda --> if_pol_state : Czy zgoda wydana? - Tak
        if_zgoda --> odw : Czy zgoda wydana? - Nie
        if_pol_state --> o : Czy obie osoby polskojęzyczne? - Tak
        if_pol_state --> p1 : Czy obie osoby polskojęzyczne? - Nie
        p2 --> o
        o --> u
        if_data_state --> pd : Czy data pasuje? - Tak
        if_data_state --> zd : Czy data pasuje? - Nie
        pd --> osw
        odw --> [*]
    }

    state Urzędnik {
        direction LR
        state "Sprawdzenie poprawności dokumentów narzeczonych" as pdok
        state "<<\system>>" as pdok
        state if_popr <<choice>>
        state "Sprawdzenie dostępności daty" as d
        state "<<\system>>" as d
        state "Poinformowanie o dostępności daty" as dd
        state "Zarejestrowanie daty ślubu" as zdat
        state "<<\system>>" as zdat
        state "Przydzielenie urzędnika do zawarcia ślubu" as um
        state "<<\system>>" as um

        pdok --> if_popr
        d --> dd
        zdat --> um
    }
    state Organ_sądowy {
        direction LR
        state "Otrzymanie wniosku o wydanie zgody sądu na zawarcie małżeństwa" as wzg
        state "Wydanie decyzji sądu" as dec
        wzg --> dec

    }
    state Tłumacz {
        direction LR
        state "Otrzymanie dokumentów do przetłumaczenia" as odok
        state "Tłumaczenie i odesłanie przetłumaczonych dokumentów" as tdok

        odok --> tdok

    }
    state Urzędnik_udzielający_ślubu {
        direction LR
        state "Otrzymanie przydziału do udzielenia ślubu" as op
        state "<<\system>>" as op
        state "Udzielenie ślubu" as slub
        state "Zarejestrowanie nowego małżeństwa" as rej
        state "<<\system>>" as rej

        slub --> rej
    }

    state join_state <<join>>

    wsa --> wzg
    dec --> sa
    p1 --> odok
    tdok --> p2
    u --> pdok
    if_popr --> u : Czy dokumenty poprawne? - Nie
    if_popr --> zd : Czy dokumenty poprawne? - Tak
    zd --> d
    dd --> if_data_state
    pd --> zdat
    um --> op
    op --> join_state
    osw --> join_state
    join_state --> slub
    slub --> m
    m --> [*]
```

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
        state "Wprowadzenie zgonu do systemu" as k2
        state "<<\system>>" as k2
        state "Przygotowanie aktu zgonu" as k3
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

# Modelowanie przypadków użycia

## Cel
Rozdział dokumentu powinien opisywać specyfikację interakcji (dialogu) użytkowników z projektowanym systemem informatycznym, umożliwiając zaprojektowanie jego interfejsu i sporządzenie makiety tego systemu.

## Wyniki prac

### Lista aktorów systemowych
lista użytkowników i systemów informatycznych `podejmujących interakcję` z projektowanym systemem.

<!-- Do opisania -->
Lista aktorów systemu informatycznego:
- rodzice nowo narodzonego dziecka
- personel szpitala - lekarze / położne
- osoby zakochane
- osoby bliskie zmarłego
- urzędnicy

### Diagramy przypadków użycia systemu
sporządzone zgodnie z notacją UML diagramy ilustrujące przypadki użycia systemu i ich związki z odpowiednimi aktorami, oraz zależności pomiędzy przypadkami użycia (**\<\<include\>\>**,**\<\<extend\>\>**, generalizacja/specjalizacja).

1. Zgłoszenie narodzin dziecka przez personel medyczny
2. Zgłoszenie narodzin dziecka przez rodziców dziecka
3. Złożenie wniosku o wzięcie ślubu cywilnego
4. Generowany harmonogram ślubów cywilnych
5. Rejestracja zgonu przez urzędnika

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
