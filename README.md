# Wspólczesne tworzenie gier na przykladzie Unity i Unreal Engine.

## Slowa kluczowe

"gry konsolowe", "silnik gier", "Unity", "Unreal", "animacja", "fizyka", "skrypty", "interfejs użytkownika", "scena", "obiekt", "platforma", "gry mobilne", "optymalizacja", "particle", "audio", "3D", "2D", "architektura", "oswietlenie", "komponent", "drag and drop"

## Spis tresci

1. "Wstep"
2. "Krótka historia silników do tworzenia gier"
3. "Czym jest GDD?"
3. "Przedstawienie Unity i Unreal Engine"
4. "Podstawa tworzenia gier - Unity" (dodatek: video)
5. "Podstawa tworzenia gier - Unreal" (dodatek: video)
6. "Prosta gra krok po kroku - Unity"
7. "Prosta gra krok po kroku - Unreal"
8. "Bugi - jak ich unikac, testy gier" (lista "przykazan")
9. "Podsumowanie procesu tworzenia dla obu silnikow"
10. "Unity i Unreal, a przyszlosc"
11. "Zakonczenie"

### Wstep (to moze bardziej pasowac pdo histore silnikow, zastanawiam sie jeszcze)

Historia gier siega roku 1942, kiedy to dwoje amerykanów Thomasa A. Goldsmith Jr. oraz Estle Ray, tworzy prototyp gry komputerowej :
symulator pocisku rakietowego. Kolejne lata przynosza nowe technolgie. Rok 1952 - pierwsza gra korzystajaca z prototypu monitora. 1958 - pierwsze kontrolery. 1961 - pierwsza gra z wektorowa grafika.

Jednak to dopiero rok 1972 mozna uznac za poczatek nowej branzy, kiedy powstaje Pong - pierwsza gra odnoszaca komercyjny sukces. Udowadnia ona ze na grach mozna zarobic pieniadze, popyt okazal sie ogromny, zas rynek wyjatkowo maly.

Nie mozna zapominac, ze byly to czasy gdy jezyki programowania znane nam dzisiaj nie byly tak rozpowszechnione, byly to poczatkwoe lata jezyka C, a najpopularniejszy powszechnie jezyk do tworzenia silnikow gier - C++ - nie istnial wogole. Wiekszosc gier byla tworzona od podstaw: budowano odpowiednie maszyny. Tak popularne w tamych czasach automaty nie byly niczym wiecej niz ladnie obudowanymi gotowymi urzadzeniami, tworzonymi pod konkretna gre - z zamknieta architektura i bez mozliwosci wprowadzania zmian. 

Dopiero rozwoj komputerow osobistych pozwolil na wieksza swobode oraz pisanie wielu programow pod jedno urzadzenie. Nie zmienialo to faktu, ze ze wzgledu na roznorodna architekture kod napisany raz pod konkretna gre, po jej wydaniu stawal sie bezuzyteczny. Dodatkowo, wczesny sprzet komputerowy cechowal sie niewielka wydajnoscia, totez aby uzyskac jak najlepsza wydajnosc, pisano kod bezposrednio pod dany sprzet.

// pierwszy kod lata 90, Quake engine etc.

