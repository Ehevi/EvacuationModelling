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
- [ ] ? (rozwiązanie komercyjne) [STEPS](https://www.steps.mottmac.com/free-trial) - brak odpowiedzi w kwestii wersji próbnej
- [ ] [Pathfinder](https://www.thunderheadeng.com/pathfinder) - spełnia wszystkie wymagania
- [ ] [AnyLogic](https://www.anylogic.com/) - w teorii spełnia wymagania, trudny w obsłudze

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


