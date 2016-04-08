## Wspólczesne tworzenie gier na przykladzie silników Unity i Unreal Engine

### Slowa kluczowe

gry konsolowe, "silnik gier", "Unity", "Unreal", "animacja", "fizyka", "skrypty", "interfejs użytkownika", "scena", "obiekt", "platforma", "gry mobilne", "optymalizacja", "particle", "audio", "3D", "2D", "architektura", "oswietlenie", "komponent", "drag and drop"

### Spis tresci

1. Wstep
2. Krótka historia silników do tworzenia gier
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

Jeszcze 20 lat temu tworzenie gier było nie lada wyzwaniem, wymagało ogromnej cierpliwości, sporej wiedzy z zakresu fizyki, informatyki i matematyki. Dzisiaj grę stworzyć może nawet przeciętny nastolatek. Ilość gier wychodzących na rynek jest tak duża, że nie sposób śledzic pomniejsze tytuly. Serwisy z małymi grami pękają w szwach. Duże gry nie są już tylko domeną dużych firm. Niejednokrotnie mali zawodnicy potrafią zawojowac rynek grą, która pod względem skomplikowania bije wielkie tytuły lat 90 - robione przez ogromne zespoly.
Jak to możliwe?
Odopowiedzią są silniki gier - zaawansowane oprogramowanie tworzone przez firmy specjalnie na potrzeby nowych gier. Powołanie nowej gry do zycia wymaga ogromnych nakładow czasowych i finansowych. "Jak bedziemy generować grafikę? Czy w naszej grze będzie realistyczna fizyka? A dynamiczne światło? Co z dzwiękiem? Jaki język programowania wybrać? A i trzeba jeszcze tę grę zoptymalizować pod konkretną platformę!". Na te i wiele innych pytań trzeba odpowiedzieć za każdym razem tworząc nową grę. Doświadczeni twórcy wiedzą jednak, że to własnie odpowiedzi na te pytania generują największe koszty. Aby uniknąć odkrywania koła na nowo, firmy często tworzą własne silniki, bądź wykupują licencje na inne. Współcześnie, większość nowych tytułów robiona jest na już gotowych silnikach. Tylko mały procent doczeka się własnego, wartego niejednokrotnie więcej niż sama gra. 

Na nasze szczęście dzisiaj każdy z nas może skorzystać z możliwości takiego silnika. O ile kiedyś były one zarezerwowane tylko dla wąskiej grupy twórców, szybko odkryto, że na sprzedaży i udostępnianiu silników gier można także zarobić spore pieniądze. Rynek gier jest nieprzewidywalny i nawet najlepsza gra może okazać sie finansową klapą. Jednak silnik na którym ta gra powstała nie traci przy tym na wartości. Koszty licencji popularnych płatnych silników takich jak Frostbite 3 lub Cry Engine 3 mogą sięgać milionowych kwot.

Mimo, że istnieje wiele innych darmowych silnikow, to w tej pracy skupimy sie na dwóch obecnie najpopularniejszych darmowych silnikach:
Unreal Engine udostępniane przez firmę Epic Games, oraz Unity 3D udostępniane przez firmę Unity Technologies. 

Przyjrzymy się krótkiej historii silników gier oraz porównamy oba oprogramowania. Dowiemy sie czym jest GDD, następnie przyjrzymy się ich cechom i opiszemy proces tworzenia gier w każdym z nich. Odkryjemy najczęstsze bugi w grach i jak z nimi walczyć, a w podsumowaniu opiszemy krótko: stopień trudnosci w użytkowaniu, czas potrzebny do stworzenia gry i zastanowimy sie nad przyszłością obu silników.


### Krótka historia silników do tworzenia gier

Historia gier sięga roku 1942, kiedy to dwoje amerykanów Thomasa A. Goldsmith Jr. oraz Estle Ray, tworzy prototyp gry komputerowej :
Symulator pocisku rakietowego. Kolejne lata przynoszą nowe technologie. Rok 1952 - pierwsza gra korzystająca z prototypu monitora. 1958 - pierwsze kontrolery. 1961 - pierwsza gra z wektorową grafiką.

Jednak to dopiero rok 1972 można uznać za początek nowej branży, kiedy powstaje Pong - pierwsza gra odnosząca komercyjny sukces. Udowadnia ona, że na grach można zarobić pieniądze. Popyt okazał się ogromny, zaś rynek wyjątkowo mały.

Nie można zapominać, że były to czasy gdy języki programowania znane nam dzisiaj nie istniały. Były to pierwsze lata języka C.  Najpopularniejszy powszechnie język do tworzenia silników gier - C++ - nie istniał wogóle. Większość gier była tworzona od podstaw: budowano odpowiednie maszyny. Tak popularne w tamych czasach automaty nie byly niczym wiecej niz ladnie obudowanymi gotowymi urzadzeniami. Każdy był tworzony pod konkretną grę - z zamkniętą architekturą i bez możliwości wprowadzania zmian. 

Dopiero rozwój komputerów osobistych pozwolił na większą swobodę oraz pisanie wielu programów pod jedno urządzenie. Nie zmieniało to faktu, że ze względu na różnorodną architekturę, kod napisany raz pod konkretna gre, po jej wydaniu stawal sie bezuzyteczny. Dodatkowo, wczesny sprzet komputerowy cechowal sie niewielka wydajnoscia, totez aby uzyskac jak najlepsza wydajnosc, pisano kod bezposrednio pod dany sprzet.

// pierwszy kod lata 90, Quake engine etc.

