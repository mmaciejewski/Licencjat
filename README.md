## Tworzenie gier w Unity i Unreal Engine

#### Agnieszka Czerwińska, Michał Maciejewski i Mariusz Miszczykowski

### Slowa kluczowe

gry konsolowe, silnik gier, Unity, Unreal Engine, animacja, fizyka, skrypty, interfejs użytkownika, scena, obiekt, platforma, optymalizacja, particle, audio, 3D, architektura, oswietlenie, komponent, drag and drop

### Spis treści

1. Wstęp
1. Krótka historia silników do tworzenia gier
1. Czym jest Game Design Document?
1. Przedstawienie Unity i Unreal Engine
1. Podstawy tworzenia gier:
   1.  Unity (dodatek: video)
   1. Unreal Engine (dodatek: video)
1. Prosta gra krok po kroku -- Unity
1. Prosta gra krok po kroku -- Unreal Engine
1. Testowanie gier
1. Podsumowanie procesu tworzenia gier dla obu silników
1. Zakończenie

### Streszczenie

W pracy opisano współczesne podejście do programowania gier z wykorzystaniem silników gier.
Porównano dwa silniki o otwartym kodzie: Unreal Engine udostępnianym przez firmę Epic Games, oraz Unity 3D –- Unity Technologies. 
W części praktycznej pracy stworzono dwie wersje jednej gry - po jednej w każdym z silników. Zostały one oparte na jednym Game Design Document (patrz, rozdział 3 –- „Czym jest Game Design Document”).
Pozwoliło to na stworzenie gier o podobnych cechach, jednak dzięki specyfice samego dokumentu, także nie ograniczających możliwości żadnego z silników. Cały przebieg procesu tworzenia owych gier został opisany w oddzielnych rozdziałach.

### Wstęp (DO KOREKTY)

Jeszcze 20 lat temu tworzenie gier było nie lada wyzwaniem, wymagało ogromnej cierpliwości, sporej wiedzy z zakresu fizyki, informatyki i matematyki. Dzisiaj grę stworzyć może nawet przeciętny nastolatek. Dlatego liczba gier wychodzących na rynek jest tak duża, że nie sposób śledzić pomniejsze tytuły.

Gry komputerowe towarzyszyły nam od dzieciństwa. Były naszym hobby i poświęcaliśmy im mnóstwo czasu. Od zawsze marzyliśmy, by zacząć tworzyć swoje własne gry. 
Wiedza, którą zdobyliśmy w trakcie studiów pozwoliło nam nie tylko na realizację tego marzenia, ale dała nam również możliwość analizy różnych sposobów tworzenia oprogramowania. W tej pracy chcemy przedstawić różnice wynikające z oparcia jednej gry na dwóch silnikach do tworzenia gier - Unity i Unreal Engine. W tej pracy zawarliśmy podstawowe różnice między nimi, ich głowne zalety, jak i ograniczenia obu silników. Wierzymy, że pozwoli to początkującym twórcom gier, jak i tym bardziej doświadczonym, znaleźć właściwe narzędzie do wykonania zadania.

Silniki gier to zaawansowane oprogramowanie tworzone przez firmy, specjalnie na potrzeby nowych gier. Powołanie nowej gry do życia wymaga ogromnych nakładów czasowych i finansowych. "Jak będziemy generować grafikę? Czy w naszej grze będzie realistyczna fizyka? A dynamiczne światło? Co z dzwiękiem? Jaki język programowania wybrać? A i trzeba jeszcze tę grę zoptymalizować pod konkretną platformę!". Na te i wiele innych pytań trzeba odpowiedzieć za każdym razem tworząc nową grę. Doświadczeni twórcy wiedzą jednak, że to własnie odpowiedzi na te pytania generują największe koszty. Aby uniknąć odkrywania koła na nowo, firmy często tworzą własne silniki, bądź wykupują licencje na inne. Współcześnie, większość nowych tytułów robiona jest na już gotowych silnikach. Tylko mały procent doczeka się własnego, wartego niejednokrotnie więcej niż sama gra. 
Na nasze szczęście dzisiaj każdy z nas może skorzystać z możliwości takiego silnika. O ile kiedyś były one zarezerwowane tylko dla wąskiej grupy twórców, szybko odkryto, że na sprzedaży i udostępnianiu silników gier można także zarobić spore pieniądze. Koszty licencji popularnych płatnych silników takich jak Frostbite 3 lub Cry Engine 3 mogą sięgać milionowych kwot.

Mimo, że na rynku istnieje wiele innych darmowych silnikow, w tej pracy skupimy sie na dwóch obecnie najpopularniejszych darmowych silnikach:
Unreal Engine udostępniane przez firmę Epic Games, oraz Unity 3D udostępniane przez firmę Unity Technologies. 

Przyjrzymy się krótkiej historii silników gier oraz porównamy oba oprogramowania. Dowiemy sie czym jest GDD, następnie przyjrzymy się ich cechom i opiszemy proces tworzenia gier w każdym z nich. Odkryjemy najczęstsze bugi w grach i jak z nimi walczyć, a w podsumowaniu opiszemy krótko: stopień trudnosci w użytkowaniu, czas potrzebny do stworzenia gry i zastanowimy sie nad przyszłością obu silników.


### Krótka historia silników do tworzenia gier

Silnik gier jest to specjalne oprogramowanie zaprojektowane z myślą o tworzeniu i rozbudowywaniu gier wideo. Jego typową funkcjonalnością jest obsługa generowania grafiki (zarówno 2D i 3D), fizyki, kolizji, dźwięku, sieci, animacji, procesora, pamięci itp. Większość silników opiera się na tzw. skryptach – krótkich programach pisanych wewnątrz aplikacji, pozwalających na stosunkowo nieskrępowaną modyfikację i ciągłe rozszerzanie możliwości danego silnika. Idzie to w parze z głównym założeniem jakim jest możliwość jego wielokrotnego wykorzystania do tworzenia kompletnie odmiennych tytułów.  

Teoretycznie prawie każda gra, która kiedykolwiek powstała, opiera się na jakimś silniku. Jednak dopiero lata 90' uznajemy za początek ich historii. Jest to związane z faktem, że pierwsze gry były tzw. „hardkodowane”. Oznacza to, że wszelkie dane były bezpośrednio wpisywane w kod źródłowy, a ich wartości dostosowane bezpośrednio do urządzenia na które były tworzone. Ze względu na niską wydajność i limity pamięci ówczesnych maszyn było to rozwiązanie konieczne. Uniemożliwiały jednak modyfikację kodu. Oznaczało to, że silnik wykorzystywany był tylko raz, pod konkretną grę, co stoi w konflikcie z wcześniej podaną definicją silnika gier.

Poniżej została zamieszczona tabelka z datami, autorami i szczególnymi cechami silników gier, poczynając od „Hovertank 3D”. Nie był to pierwszy silnik w historii, jednak jako pierwszy był rozwijany i użyty w wielu produkcjach. Był to także jeden z tytułów 3D z gatunku FPS ( ang. first-person-shooter ). Rozwój tego gatunku szedł w parze z powstaniem terminu „silnika gier”. Trzeba zaznaczyć, że ze względu na ogromną ilość różnych silników, poniższa lista nie jest kompletna i zawiera tylko te najpopularniejsze i/lub najbardziej zasłużone. 

| Nazwa        | Rok powstania | Autor/właściciel  | Szczegóły |
| -------------|----| --------- | ---------------- | :---------: |
| Hovertank 3D | 1991 | John Carmack (id Software) | Silnik powstał w 6 tygodni, wielokrotnie rozwijany, napisany w językach C i x86 Assembly |
| Wolfenstein 3D | 1992 | John Carmack (id Software) | Usprawniona wersja Hovertank 3D, dodano raycasty, i fizykę gracza, zwiększono wydajność |
| ID Tech 1 | 1993 | John Carmack (id Software) | Pierwszy z serii silników id Tech, dodano opcje konfiguracji grafiki, otwarte przestrzenie, pełne oteksturowanie gry |
| Build | 1996 | Ken Silverman (3D Realms) | Dodano woksele, podział na sektory, destrukcja otoczenia |
| Quake Engine | 1996 | John Carmack (id Software) | Dodano statyczne oświetlenie, zwiększono wydajność, możliwość gry sieciowej, lightmapy |
| Unreal Engine | 1998 | Epic Games | Używany i rozwijany do dziś silnik gier, korzysta z własnego języka skryptowego UnrealScript, modularna budowa silnika, łatwy do modowania, napisany w C++, jeden z najpopularniejszych silników w historii |
| Id Tech 3 | 1999 | id Software | Powstał w odpowiedz na UnrealEngine, wymaga Open GL, dodanie shaderów,  dodano format MD3 do modeli 3D |
| Infernal Engine | 2000 | Terminal Reality | Napisany w C++, język skryptowy Dante, niewymagający kompilacji przy zmianach, rozbudowany system zarządzania zasobami |
| Cry Engine | 2004 | Crytek | Powstało wstępnie jako demo technologiczne karty graficznej GeForce 3, obsługa Shader Model 3.0, efekt HDR,  język programowania Lua i C# |
| Source Engine | 2004 | Valve Corporation | Napisany w C++, Source SDK udostępniany dla każdego użytkownika posiadającego grę na platformie Steam, wsparcie wieloprocesowości |
| Unity Engine | 2005 | Unity Technologies | Napisany w C, C++ i C#, pozwala robić gry na większość istniejących platform, łatwy w użytkowaniu |
| Frostbite | 2008 | Digital Illusions CE | HDR Audio, system destrukcji otoczenia |


###Czym jest Game Design Document?

Game Design Document (w skrócie GDD) jest dokumentem tworzonym jeszcze przed przystąpieniem do tworzenia gry. Najważniejszym celem dokumentu jest utrzymanie konsystencji oraz jednoznaczne wytyczenie celów związanych z projektem. GDD jest tak zwanym „żywym” dokumentem. Oznacza to, że może on być rozwijany i zmieniany podczas pracy nad grą. Jeśli pojawią się przeszkody uniemożliwiające wykonanie wcześniejszych założeń, lub powodujące znaczne opóźnienie w pracach nad grą dozwolone jest zmienianie danych części dokumentu. Zaleca się jednak w miarę możliwości, aby nie odchodzić za daleko od wyjściowych założeń, gdyż stoi to w konflikcie z założeniami owego dokumentu. 

Struktura dokumentu nie jest jednoznacznie zdefiniowana. W zależności od wielkości zespołu oraz docelowych odbiorców może on przybierać różnorakie formy – od czysto formalnych mocno technicznych aspektów, do ogólnej wizji artystycznej świata i rodzaju rozgrywki. Dokument może składać się z czystego tekstu, ale również screenów, zdjęć, szkiców koncepcyjnych, diagramów. Każda forma jak najlepiej oddająca założenia gry jest akceptowalna. 

Zdarza się, że GDD często zaczyna się tylko podstawowymi założeniami gry, a kończy jako rozbudowany wielostronicowy dokument opisujący każdy możliwy aspekt gry. Przy jego pisaniu nie można zapomnieć, że   będzie on czytany przez każdego członka zespołu tworzącego grę, nie tylko przez programistów, ale także artystów czy managerów. Dlatego pomimo ogólnej swobody przy jego pisaniu zaleca się zachowywać ogólnie pojętą strukturę, co pozwala na oddzielenie zagadnień typowo technicznych, od tych związanych z marketingiem czy kreacją świata. 

Wiele firm wymaga od twórców gier aby dostarczali GDD. Jako, że nie ma określonego standardu dla tego typu dokumentu, autorzy muszą go tak zaprojektować, aby grę nie tylko przedstawić, ale także „sprzedać”. Sprawia to, że GDD potrafią się od siebie znacząco różnić. 

Swoboda w tworzenia GDD daje wiele możliwości, ale potrafi także być sporym wyzwaniem. Osoby posiadające już doświadczenie przy robieniu gier zdecydowanie lepiej radzą sobie przy pisaniu takiego dokumentu, gdyż znają już wszystkie etapy produkcji, oraz problemy z nią związane. Korzystając z ich doświadczenia można nakreślić pewne prawidłowości przy jego pisaniu.

Jak napisać dobre GDD.

Jeśli GDD pisze kilka osób, wyznacz jedną osobę odpowiedzialną za funkcjonowanie dokumentu. 
Zbyt duża swoboda  w dostępie do dokumentu wprowadza niepotrzebny chaos. Każdy pomysł przed wpisaniem powinien zostać najpierw rozpatrzony, aby nie wpuszczać do projektu nadmiarowych pomysłów.

Nie pisz całego dokumentu na „raz”.
Pamiętaj, że GDD tak samo jak projekt będzie ciągle ewoluować. Może się okazać, że wraz z rozwojem projektu, wiele pomysłów zostanie odrzuconych, a niektóre założenia ulegną zmianie. Jeśli nie pozostanie wystarczająco miejsca na zmiany, lub projekt zacznie przechodzić znaczące zmiany, może to zaważyć na czytelności dokumentu.

Używaj różnych form przekazu.
Obraz przy opisie lokacji, bądź referencja przy animacji powiedzą czytelnikowi więcej niż długi skomplikowany tekst. 

Podziel dokument na sekcje.
Stwórz dział „Użyte technologie” i „Świat gry”. W tym momencie każdy będzie wiedział, gdzie i jakiego typu informacje znajdują się w tekście.

Wyznacz realistyczne cele.
Zanim dokument zostanie ostatecznie zatwierdzony, powinien najpierw zostać rozpatrzony pod kątem potencjalnych kosztów czasowych i finansowych. Stworzenie wielkiego tytułu, może być zbyt ambitne dla małego zespołu. Głównym celem powinno być ukończenie gry w odpowiednim czasie. Trzeba wziąć pod uwagę ewentualne problemy i pamiętać, że każdy nowy pomysł generuje dodatkowe koszty.



Przykładowa budowa GDD:

Index

1.	Założenia gry
1. Ogólny opis (gatunek, format, założenia)
2. Interakcja
2. Przebieg rozgrywki
3. Cel rozgrywki
2.	Założenia techniczne
1. Docelowe platformy
2. Użyte technologie
1.	silnik gry
2.	pozostałe technologie (np. systemy kontroli wersji, frameworki)
	3. Wyświetlanie/Obraz (np. orientacja na urządzeniu mobilnym)
	4. Sterowanie
	5. Mechanika gry
	6. Inne

       3.    Świat gry
1.	Świat gry
1.	Obiekty
1.	statyczne
2.	interaktywne
2.	Środowisko
1.	motywy 
2.	otoczenie
3.	Wyzwania
4.	Przeciwnicy
	
2.	Poruszanie po świecie
4.	Grafika
1.  Style
2. Assety
	5.    Dżwięk
1.	Style
2.	Potrzebne dźwięki
3.	Potrzebna muzyka
		
	6. Ramy czasowe projektu
	7. Dodatkowe pomysły

