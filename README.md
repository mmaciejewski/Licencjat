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

### Streszczenie

W pracy opisano współczesne podejście do programowania gier z wykorzystaniem silników gier.
Porównano dwa silniki o otwartym kodzie: Unreal Engine udostępnianym przez firmę Epic Games, oraz Unity 3D – Unity Technologies. 

? W tej pracy termin „silniki” zawsze będzie odnosił się do ww. wymienionych oprogramowań, za wyjątkiem rozdziału drugiego - „Krótka historia silników gier”. 

W części praktycznej pracy stworzone dwie wersje jednej gry - po jednej w każdym z silników. Zostały one oparte na jednym GDD (patrz, rozdział 3 – „czym jest gdd”). 
Pozwoliło to na stworzenie gier o podobnych cechach, jednak dzięki specyfice samego dokumentu, także nie ograniczających możliwości żadnego z silników. Cały przebieg procesu tworzenia owych gier został opisany w oddzielnych rozdziałach. Obejmują one wszystkie kroki niezbędne do stworzenia grywalnego produktu, zarówno od strony programistycznej, jak i projektowej. Poprzedza je rozdział zawierający niezbędne informacje potrzebne do zrozumienia podstawowych zagadnień oraz obsługi silników - w formie krótkich filmów wideo. Część teoretyczna skupia się przede wszystkich na przedstawieniu samego zagadnienia silników gier w ogólności, mającego pokrótce wprowadzić odbiorcę w temat tego typu oprogramowania - objaśnić ich cel i genezę. Porusza także tematy ściśle powiązane z samym programowaniem, którymi są zarówno planowanie jak i testowanie aplikacji. 
Biorąc pod uwagę szerokie spektrum zagadnień powiązanych z całym procesem tworzenia gry, natomiast wychodzących poza zakres samego programowania konieczne było odpowiednie podzielenie pracy. Dlatego też część praktyczna skupia się na pracy w samych silnikach i ich funkcjonalności, a część teoretyczna na temacie tworzenia gier ogółem.


### Wstęp 

Jeszcze 20 lat temu tworzenie gier było nie lada wyzwaniem, wymagało ogromnej cierpliwości, sporej wiedzy z zakresu fizyki, informatyki i matematyki. Dzisiaj grę stworzyć może nawet przeciętny nastolatek. Dlatego liczba gier wychodzących na rynek jest tak duża, że nie sposób śledzić pomniejsze tytuły. Dlaczego podjęliśmy ten temat :+1:

Głównym powodem są silniki gier - zaawansowane oprogramowanie tworzone przez firmy specjalnie na potrzeby nowych gier. Powołanie nowej gry do życia wymaga ogromnych nakładów czasowych i finansowych. "Jak będziemy generować grafikę? Czy w naszej grze będzie realistyczna fizyka? A dynamiczne światło? Co z dzwiękiem? Jaki język programowania wybrać? A i trzeba jeszcze tę grę zoptymalizować pod konkretną platformę!". Na te i wiele innych pytań trzeba odpowiedzieć za każdym razem tworząc nową grę. Doświadczeni twórcy wiedzą jednak, że to własnie odpowiedzi na te pytania generują największe koszty. Aby uniknąć odkrywania koła na nowo, firmy często tworzą własne silniki, bądź wykupują licencje na inne. Współcześnie, większość nowych tytułów robiona jest na już gotowych silnikach. Tylko mały procent doczeka się własnego, wartego niejednokrotnie więcej niż sama gra. 
Na nasze szczęście dzisiaj każdy z nas może skorzystać z możliwości takiego silnika. O ile kiedyś były one zarezerwowane tylko dla wąskiej grupy twórców, szybko odkryto, że na sprzedaży i udostępnianiu silników gier można także zarobić spore pieniądze. Koszty licencji popularnych płatnych silników takich jak Frostbite 3 lub Cry Engine 3 mogą sięgać milionowych kwot.

Mimo, że na rynku istnieje wiele innych darmowych silnikow, w tej pracy skupimy sie na dwóch obecnie najpopularniejszych darmowych silnikach:
Unreal Engine udostępniane przez firmę Epic Games, oraz Unity 3D udostępniane przez firmę Unity Technologies. 

Przyjrzymy się krótkiej historii silników gier oraz porównamy oba oprogramowania. Dowiemy sie czym jest GDD, następnie przyjrzymy się ich cechom i opiszemy proces tworzenia gier w każdym z nich. Odkryjemy najczęstsze bugi w grach i jak z nimi walczyć, a w podsumowaniu opiszemy krótko: stopień trudnosci w użytkowaniu, czas potrzebny do stworzenia gry i zastanowimy sie nad przyszłością obu silników.


### Krótka historia silników do tworzenia gier

Pierwsze silniki do tworzenia gier nie były zbyt powszechne. Były prostymi platformami do tworzenie gier 2D. Rozpowszechniły się dopiero w latach 90-tych, wraz z rosnącą popularnością grafiki trójwymiarowej.

// pierwszy kod lata 90, Quake engine etc.

