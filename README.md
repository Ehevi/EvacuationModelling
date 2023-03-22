# EvacuationModelling
# Etap 1. Analiza problemu i dziedziny
08.03.2023
## Problem
Zbadanie możliwości modelowania procesu ewakuacji budynku D17

**Proces ewakuacji** - proces, który pozwala osobom znajdującym się w zagrożonej przestrzeni dotrzeć do miejsca bezpieczeństwa, składającego się z procesu przed
przemieszczaniem się i procesu przemieszczania się (standard ISO/TR 13387-8)
### Cele
- [ ] opracowanie przygotowania rzeczywistych danych - zbiór danych, o którym mowa w rozdziale 5.2. pracy (strona 40), rozrysowane tabelki
- [ ] zbadanie gotowych rozwiązań, wybór modeli
- [ ] symulacje na modelach - zebranie danych
- [ ] porównanie wyników symulacji ze sobą nawzajem i z rzeczywistymi danymi - walidacja badanych modeli
### Jakich danych potrzebujemy
- [ ] plany budynków - mapowanie budynków do postaci BIM (Building Information Modelling),
  do ustalenia: stopień dokładności, dostępne są plany budynków i ewakuacji - na każdym piętrze są umieszczone schematy
- [ ] stan początkowy - rozmieszczenie osób w budynkach
- [ ] czas, jaki upłynął do momentu opuszczenia posczególnych pomieszczeń
- [ ] prędkość poruszających się osób: v = 0,91m/s (wg dostarczonej pracy)
### Przegląd gotowych rozwiązań
- [ ] [Cromosim](http://www.cromosim.fr/example_micro.html#social-force-model)
- [ ] [JuPedSim](https://www.jupedsim.org/jpscore_introduction.html)
- [ ] [jCrowdSimulator](https://github.com/FraunhoferIVI/jCrowdSimulator)
- [ ] [STEPS](https://www.steps.mottmac.com/free-trial) - brak odpowiedzi w kwestii wersji próbnej
- [ ] [Pathfinder](https://www.thunderheadeng.com/pathfinder) - spełnia wszystkie wymagania, można stworzyć plan budynku na podstawie zdjęcia, obsługuje schody, animacje 3d
- [ ] [AnyLogic](https://www.anylogic.com/) - w teorii spełnia wymagania i robi to co Pathfinder, ale trudny w obsłudze

## Dziedzina
### Metryki
- krzywa ewakuacyjna - zależność liczby osób pozostających w budynku od czasu,
- liczba ludzi, którzy wyszli poszczególnymi wyjsciami ewakuacyjnymi,
- sekwencje ewakuacji - analiza rozmieszczenia ludzi w danych momentach ewakuacji,
- identyfikacja punktów zatłoczenia
### Dyskusja
- reprezentacja pięter budynku `Teleportation cell`
- *proces przed przemieszczaniem się* - czynniki psychospołeczne, zazwyczaj doliczenie dodatkowego czasu
- różne modele dynamiki pieszych oferują różne opisy liczbowe do pomiaru ruchu pieszych (przepływ, zagęszczenie)
### Klasyfikacja modeli
#### mikroskopowe / makroskopowe
#### ciągłe / dyskretne
#### deterministyczne / stochastyczne
#### oparte o reguły / oparte o siły
#### wysokiej prawdziwości / niskiej prawdziwości

# Etap 2. Analiza wymagań i przegląd dostępnych rozwiązań pod ich kątem
22.03.2023
## Kryteria wyboru rozwiązania (lista wymagań):
- [ ] darmowy dostęp do oprogramowania i jego kodu źródłowego
- [ ] open source lub licencja studencka
- [ ] brak wygórowanych wymagań technicznych do uruchomienia symulacji
- [ ] łatwość instalacji i obsługi narzędzia
- [ ] obecność tutoriali i wsparcia
- [ ] popularność rozwiązania (np. wykorzystanie przez firmy zajmujące się problematyką)
- [ ] łatwość procesu dostosowania danych do formatu akceptowanego przez program
- [ ] prosta interpretacja wyników działania programu
- [ ] funkcjonalności

## Przegląd symulatorów
| Symulator | [Pathfinder](https://www.thunderheadeng.com/pathfinder) | STEPS |
|--------:|----------------------------|--------------|
| dostęp | możliwość pobrania | możliwość pobrania |
| licencja | licencja studencka | licencja studencka (?) / free trial |
| wymagania techniczne | dostępne tutoriale i forum | tutoriale, forum |
| instalacja i obsługa | bez problemu | brak odpowiedzi |
| wsparcie | dokumentacja, tutoriale, forum | brak odpowiedzi |
| popularność | dobre opinie | dobre opinie |
| wyniki | automatyczna analiza wyników | mapy, wizualizacje, csv, xlsx |
| funckjonalności| windy, kolejki, customowa populacja | ruch pieszych |

## Ogólne informacje
- do każego sprawdzonego rozwiązania musimy dopasować dane wejściowe do przyjmowanego formatu
- "przyjemność obsługi"
- rozwiązania komercyjne: Pathfinder - dostaliśmy licencję studencką, STEPS - brak odpowiedzi
- spora część rozwiązań z listy jest niedostępna
