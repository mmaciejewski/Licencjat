## Tworzenie gier w Unity i Unreal Engine

#### Agnieszka Czerwińska, Michał Maciejewski i Mariusz Miszczykowski

### Slowa kluczowe

gry konsolowe, silnik gier, Unity, Unreal Engine, animacja, fizyka, skrypty, interfejs użytkownika, scena, obiekt, platforma, optymalizacja, particle, audio, 3D, architektura, oswietlenie, komponent, drag and drop

### Spis treści

1. Wstęp
1. Krótka historia silników do tworzenia gier (tabelka – rok, autor, licencja…) – max. 1 strona
1. Czym jest Game Design Document?
1. Przedstawienie Unity i Unreal Engine
1. Podstawy tworzenia gier:
   1.  Unity (dodatek: video)
   1. Unreal Engine (dodatek: video)
1. Prosta gra krok po kroku - Unity
1. Prosta gra krok po kroku - Unreal Engine
1. Testowanie gier
1. Podsumowanie procesu tworzenia gier dla obu silników
1. Zakończenie

### Streszczenie (USTAWIC GDZIES TO ZDANIE ZE ZNAKIEM ZAPYTANIA)

W pracy opisano współczesne podejście do programowania gier z wykorzystaniem silników gier.
Porównano dwa silniki o otwartym kodzie: Unreal Engine udostępnianym przez firmę Epic Games, oraz Unity 3D – Unity Technologies. 

? W tej pracy termin „silniki” zawsze będzie odnosił się do ww. wymienionych oprogramowań, za wyjątkiem rozdziału drugiego - „Krótka historia silników gier”. 

W części praktycznej pracy stworzono dwie wersje jednej gry - po jednej w każdym z silników. Zostały one oparte na jednym GDD (patrz, rozdział 3 – „czym jest gdd”). 
Pozwoliło to na stworzenie gier o podobnych cechach, jednak dzięki specyfice samego dokumentu, także nie ograniczających możliwości żadnego z silników. Cały przebieg procesu tworzenia owych gier został opisany w oddzielnych rozdziałach. Obejmują one wszystkie kroki niezbędne do stworzenia grywalnego produktu. Zarówno od strony programistycznej, jak i projektowej. Poprzedza je rozdział zawierający niezbędne informacje potrzebne do zrozumienia podstawowych zagadnień oraz obsługi silników - w formie krótkich filmów wideo. Część teoretyczna skupia się przede wszystkich na ogólnym przedstawieniu samego zagadnienia silników gier. Ma on pokrótce wprowadzić odbiorcę w temat tego typu oprogramowania - objaśnić ich cel i genezę. Porusza także tematy ściśle powiązane z samym programowaniem, którymi są zarówno planowanie jak i testowanie aplikacji. 
Biorąc pod uwagę szerokie spektrum zagadnień powiązanych z całym procesem tworzenia gry, wychodzących poza zakres samego programowania konieczne było odpowiednie podzielenie pracy. Dlatego też część praktyczna skupia się na pracy w samych silnikach i ich funkcjonalności, a część teoretyczna na temacie tworzenia gier ogółem.


### Wstęp (DO KOREKTY, DLACZEGO PODJELISMY TEMAT)

Jeszcze 20 lat temu tworzenie gier było nie lada wyzwaniem, wymagało ogromnej cierpliwości, sporej wiedzy z zakresu fizyki, informatyki i matematyki. Dzisiaj grę stworzyć może nawet przeciętny nastolatek. Dlatego liczba gier wychodzących na rynek jest tak duża, że nie sposób śledzić pomniejsze tytuły. Dlaczego podjęliśmy ten temat :+1:

Głównym powodem są silniki gier - zaawansowane oprogramowanie tworzone przez firmy specjalnie na potrzeby nowych gier. Powołanie nowej gry do życia wymaga ogromnych nakładów czasowych i finansowych. "Jak będziemy generować grafikę? Czy w naszej grze będzie realistyczna fizyka? A dynamiczne światło? Co z dzwiękiem? Jaki język programowania wybrać? A i trzeba jeszcze tę grę zoptymalizować pod konkretną platformę!". Na te i wiele innych pytań trzeba odpowiedzieć za każdym razem tworząc nową grę. Doświadczeni twórcy wiedzą jednak, że to własnie odpowiedzi na te pytania generują największe koszty. Aby uniknąć odkrywania koła na nowo, firmy często tworzą własne silniki, bądź wykupują licencje na inne. Współcześnie, większość nowych tytułów robiona jest na już gotowych silnikach. Tylko mały procent doczeka się własnego, wartego niejednokrotnie więcej niż sama gra. 
Na nasze szczęście dzisiaj każdy z nas może skorzystać z możliwości takiego silnika. O ile kiedyś były one zarezerwowane tylko dla wąskiej grupy twórców, szybko odkryto, że na sprzedaży i udostępnianiu silników gier można także zarobić spore pieniądze. Koszty licencji popularnych płatnych silników takich jak Frostbite 3 lub Cry Engine 3 mogą sięgać milionowych kwot.

Mimo, że na rynku istnieje wiele innych darmowych silnikow, w tej pracy skupimy sie na dwóch obecnie najpopularniejszych darmowych silnikach:
Unreal Engine udostępniane przez firmę Epic Games, oraz Unity 3D udostępniane przez firmę Unity Technologies. 

Przyjrzymy się krótkiej historii silników gier oraz porównamy oba oprogramowania. Dowiemy sie czym jest GDD, następnie przyjrzymy się ich cechom i opiszemy proces tworzenia gier w każdym z nich. Odkryjemy najczęstsze bugi w grach i jak z nimi walczyć, a w podsumowaniu opiszemy krótko: stopień trudnosci w użytkowaniu, czas potrzebny do stworzenia gry i zastanowimy sie nad przyszłością obu silników.


### Krótka historia silników do tworzenia gier

Silnik gier jest to specjalne oprogramowanie zaprojektowane z myślą o tworzeniu i rozbudowywaniu gier wideo. Jego typową funkcjonalnością jest obsługa generowania grafiki (zarówno 2D i 3D), fizyki, kolizji, dźwięku, sieci, animacji, procesora oraz pamięci itp. Większość silników opiera się na tzw. skryptach – krótkich programach pisanych wewnątrz aplikacji, pozwalających na stosunkowo nieskrępowaną modyfikację i ciągłe rozszerzanie możliwości danego silnika. Idzie to w parze z głównym założeniem jakim jest możliwość jego wielokrotnego wykorzystania do tworzenia kompletnie odmiennych tytułów.  

Teoretycznie prawie każda gra, która kiedykolwiek powstała, opiera się na jakimś silniku. Jednak dopiero lata 90' uznajemy za początek ich historii. Jest to związane z faktem, że pierwsze gry były tzw „hardkodowane”. Oznacza to, że wszelkie dane były bezpośrednio wpisywane w kod źródłowy, a ich wartości dostosowane bezpośrednio do urządzenia na które były tworzone. Ze względu na słabą wydajność i limity pamięci ówczesnych maszyn było to rozwiązanie konieczne. Uniemożliwiały jednak modyfikację kodu. Oznaczało to, że silnik wykorzystywany był tylko raz, pod konkretną grę, co stoi w konflikcie z wcześniej podaną definicją silnika gier.

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
