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

### Wstep 

XXI wiek. Gry komputerowe wyrastaja na kolejne medium we wspolczesnym swiecie. Nikogo nie dziwia godziny spedzone na czystej rozrywce przy komputerze. Rynek gier siega 91 miliardow dolarow. Miliony graczy zagrywa sie przy niezliczonej ilosci gier. Jeszcze niespelna 20 lat temu moglismy liczyc na zaledwie kilkaset tytulow, a wiekszosc gier byla robiona przez pojedynczych utalentowanych pasjonatow. Tworzenie gier bylo nie lada wyzwaniem, wymagalo ogromnej cierpliwosci, sporej wiedzy z zakresu fizyki, informatyki i matematyki.

Dzisiaj gre stworzyc moze nawet przecietny ciekawski nastolatek. Ilosc gier wychodzacych na rynek jest tak duza, ze nie sposob sledzic pomniejsze tytuly. Serwisy z malymi grami pekaja w szwach, duze gry nie sa juz tylko domena duzych firm. Niejednokrotnie mali zawodnicy potrafia zawojowac rynek gra, ktora pod wzgledem skomplikowania bije wielkie tytuly lat 90 - robione przez ogromne zespoly.
Jak to mozliwe?

Odopowiedzia sa silniki gier - zaawansowane oprogramowanie tworzone przez firmy specjalnie na potrzeby nowych gier. Powolanie nowej gry do zycia wymaga ogromnych nakladow czasowych i finansowych. "Jak bedziemy generowac grafike? Czy w naszej grze bedzie realistyczna fizyka? A dynamiczne swiatlo? Co z dzwiekiem? Jaki jezyk programowania wybrac? A i trzeba jeszcze te gre zoptymalizowac pod konkretna platforme!". Na te i wiele innych pytan trzeba odpowiedziec kazdorazowo tworzac nowa gre. Doswiadczeni tworcy wiedza jednak, ze to wlasnie te pytania generuja najwieksze koszty. Aby uniknac odkrywania kola na nowo, firmy czesto tworza wlasne silniki, badz wykupuja licencje na inne. Wspolczesnie, wiekszosc nowych tytulow robiona jest na juz gotowych silnikach, a tylko maly procent z nich doczekuje sie wlasnego, wartego niejednokrotnie wiecej niz sama gra. 

Na nasze szczescie dzisiaj kazdy z nas moze skorzystac z mozliwosci takiego silnika. O ile kiedys zaawansowane silniki byly zarezerwowane tylko dla waskiej grupy tworcow, szybko odkryto, ze na sprzedazy i udostepnianiu silnikow gier mozna takze zarobic spore pieniadze. Rynek gier jest nieprzewidywalny i nawet najlepsza gra moze okazac sie finansowa klapa, natomiast silnik na ktorym ta gra powstala nie traci przy tym na wartosci. Koszty licencji popularnych platnych silników takich jak Frostbite 3 lub Cry Engine 3, moga siegac milionowych kwot.

Mimo ze istnieje wiele innych darmowych silnikow, to w tej pracy skupimy sie na dwoch obecnie najpopularniejszych darmowych silnikach:
Unreal Engine udostepniane przez firme Epic Games, oraz Unity 3D udostepniane przez firme Unity Technologies. 

Przyjrzymy sie krótkiej historii silników gier oraz porównamy oba oprogramowania. Dowiemy sie czym jest GDD, nastepnie przyjrzymy sie ich cechom i opiszemy proces tworzenia gier w kazdym z nich. Odkryjemy najczestsze bugi w grach i jak z nimi walczyc, a w podsumowaniu opiszemy krotko: stopien trudnosci w uzytkowaniu, czas potrzebny do stworzenia gry i zastanowimy sie nad przyszloscia obu silnikow.



### Krótka historia silników do tworzenia gier

Historia gier siega roku 1942, kiedy to dwoje amerykanów Thomasa A. Goldsmith Jr. oraz Estle Ray, tworzy prototyp gry komputerowej :
symulator pocisku rakietowego. Kolejne lata przynosza nowe technolgie. Rok 1952 - pierwsza gra korzystajaca z prototypu monitora. 1958 - pierwsze kontrolery. 1961 - pierwsza gra z wektorowa grafika.

Jednak to dopiero rok 1972 mozna uznac za poczatek nowej branzy, kiedy powstaje Pong - pierwsza gra odnoszaca komercyjny sukces. Udowadnia ona ze na grach mozna zarobic pieniadze, popyt okazal sie ogromny, zas rynek wyjatkowo maly.

Nie mozna zapominac, ze byly to czasy gdy jezyki programowania znane nam dzisiaj nie byly tak rozpowszechnione, byly to poczatkwoe lata jezyka C, a najpopularniejszy powszechnie jezyk do tworzenia silnikow gier - C++ - nie istnial wogole. Wiekszosc gier byla tworzona od podstaw: budowano odpowiednie maszyny. Tak popularne w tamych czasach automaty nie byly niczym wiecej niz ladnie obudowanymi gotowymi urzadzeniami, tworzonymi pod konkretna gre - z zamknieta architektura i bez mozliwosci wprowadzania zmian. 

Dopiero rozwoj komputerow osobistych pozwolil na wieksza swobode oraz pisanie wielu programow pod jedno urzadzenie. Nie zmienialo to faktu, ze ze wzgledu na roznorodna architekture kod napisany raz pod konkretna gre, po jej wydaniu stawal sie bezuzyteczny. Dodatkowo, wczesny sprzet komputerowy cechowal sie niewielka wydajnoscia, totez aby uzyskac jak najlepsza wydajnosc, pisano kod bezposrednio pod dany sprzet.

// pierwszy kod lata 90, Quake engine etc.

