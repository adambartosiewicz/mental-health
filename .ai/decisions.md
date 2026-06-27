# Decyzje systemowe

Trwałe decyzje o tym, **jak działa to repozytorium** — nie o użytkowniku. Gdy reguła workflow, konwencja nazewnictwa czy wybór strukturalny zostanie ustalony, zapisuj tu, żeby przyszłe sesje nie litygowały tego od nowa.

## Reguły aktualizacji

- Nowe decyzje dopisuj na dole z datą.
- Nigdy nie edytuj decyzji w miejscu. Jeśli decyzja zostanie odwrócona, dodaj nowy wpis, który ją zastępuje, i podlinkuj wstecz.
- Zapisy krótkie: reguła, powód, i (jeśli odwrócona) co zastąpiło.

## Format

```
## RRRR-MM-DD — <krótki tytuł>

**Decyzja:** <co ustalono>
**Dlaczego:** <powód — zwykle problem, którego uniknęliśmy>
**Status:** aktywna | zastąpiona przez <data>
```

---

## 2026-06-14 — Sesje używają nazw data-temat

**Decyzja:** Pliki sesji nazywane są `RRRR-MM-DD-krótki-temat.md` (kebab-case temat). Jedna sesja na plik.
**Dlaczego:** Sortują się chronologicznie, łatwo grepować po temacie, brak kolizji.
**Status:** aktywna

## 2026-06-14 — Aktualizacje mapy wymagają ≥3 obserwacji

**Decyzja:** Nic nie trafia do `psychological-map.md` przy mniej niż trzech odrębnych obserwacjach z różnych dni.
**Dlaczego:** Wnioski z pojedynczych zdarzeń to droga do tego, żeby ten system stał się salą luster.
**Status:** aktywna

## 2026-06-14 — Archiwizuj zamiast usuwać

**Decyzja:** Zdezaktualizowana treść z `psychological-map.md` przenoszona jest do `archive/psychological-map-RRRR-MM-DD.md`, nie usuwana. Zastępczy wpis linkuje do archiwum.
**Dlaczego:** Wykrywanie trendów wymaga historii. Trzeba móc zapytać „co kiedyś myślałem o X?"
**Status:** aktywna

## 2026-06-14 — Pojedyncze źródło prawdy w katalogu głównym

**Decyzja:** `psychological-map.md` żyje w katalogu głównym repozytorium i jest jedynym autorytatywnym dokumentem o użytkowniku. Katalog `core/` został usunięty; jego zawartość (values, strengths, open-questions) została scalona do mapy jako sekcje.
**Dlaczego:** Repozytorium fragmentowało model na wielu „core" plikach, podkopując zasadę pojedynczego źródła prawdy. Mapa powinna być czytelna sama z siebie.
**Status:** aktywna

## 2026-06-14 — `references/` nigdy nie wlewa się automatycznie

**Decyzja:** Materiał zewnętrzny w `references/` (artykuły, materiały o ADHD, pojęcia z terapii, frameworki) jest wejściem, nie częścią modelu. Materiał referencyjny nie wpływa do `psychological-map.md` automatycznie — obowiązuje ten sam próg dowodów co dla każdego specyficznego dla użytkownika wzorca.
**Dlaczego:** Atrakcyjny framework to nie dowód. Bez tej reguły mapa wypełniłaby się cudzymi modelami.
**Status:** aktywna

## 2026-06-14 — Sukces to nie „mniej lęku"

**Decyzja:** Metryką sukcesu tego repozytorium jest: większe życie, mniej unikania, większa elastyczność psychologiczna, większe zaangażowanie, lepsze rozumienie siebie. Redukcja lęku **nie** jest metryką sukcesu.
**Dlaczego:** Lęk może spaść, bo życie się skurczyło. To porażka udająca sukces. Zapisane, żeby AI nie optymalizował dla złego celu.
**Status:** aktywna

## 2026-06-15 — Język repozytorium: polski

**Decyzja:** Domyślnym językiem zawartości plików (mapa, wzorce, sesje, journal, eksperymenty, materiały, README, decyzje) jest polski. Komendy w `.ai/commands/` zostają w angielskim, ale ich wyniki — pliki sesji, eksperymenty, propozycje aktualizacji mapy, raporty cotygodniowe — generowane są po polsku. Nazwy plików i katalogów (np. `psychological-map.md`, `patterns/`, `journal/`) zostają w angielskim ze względów technicznych.
**Dlaczego:** Użytkownik myśli i czuje po polsku. Self-modeling po angielsku tworzy warstwę tłumaczenia, która gubi niuanse. Komendy zostają po angielsku, bo to instrukcje techniczne dla AI, nie treść dla użytkownika.
**Status:** aktywna

## 2026-06-16 — `journal/` partycjonowany na rok/miesiąc

**Decyzja:** Wpisy dziennika żyją pod `journal/RRRR/MM/RRRR-MM-DD.md`. Pełna data zostaje w nazwie pliku — żeby cytaty (`journal/2017/07/2017-07-22.md`) były czytelne także w izolacji od ścieżki. `journal/README.md` zostaje na poziomie głównym katalogu jako konwencja. Komendy (`analyze-pattern`, `update-map`, `weekly-review`) operujące na journal mają schodzić rekurencyjnie po podkatalogach.
**Dlaczego:** Po imporcie z lifelogu w czerwcu 2026 katalog `journal/` urósł do 269 plików w jednym poziomie, co utrudnia nawigację w edytorze i robi ścianę przy listowaniu. Podział po rok/miesiąc daje fizyczne klastry zgodne z naturalnymi oknami analitycznymi (rok jako kontekst życiowy, miesiąc jako jednostka przeglądu).
**Status:** aktywna

## 2026-06-16 — Sesję najpierw się otwiera, potem ewentualnie zapisuje

**Decyzja:** Dodano komendę `.ai/commands/open-session.md`, która ładuje kontekst do prowadzenia rozmowy psychologicznej bez tworzenia pliku sesji. Plik sesji powstaje dopiero później przez `log-session`, jeśli rozmowa wytworzyła materiał wart zachowania.
**Dlaczego:** `log-session` jest komendą zamykającą rozmowę, a brakowało symetrycznego kroku wejściowego. Bez niego AI może odpowiedzieć merytorycznie bez załadowania mapy, ostatnich sesji i właściwych wzorców.
**Status:** aktywna

## 2026-06-16 — Bearable trzyma dane strukturalne, journal opis jakościowy

**Decyzja:** Dane ilościowe i strukturalne dotyczące stanu fizycznego i codziennych moderatorów (sen, jakość snu, energia, leki, kofeina, nawodnienie, tętno/ciśnienie, symptomy fizyczne, ogólny rating lęku) mogą być prowadzone w Bearable. `journal/` nie powinien wymagać przepisywania pełnej tabeli przy każdym wpisie. Journal służy do krótkiego opisu jakościowego epizodów, zwłaszcza gdy lęk osiąga ≥5/10, występuje panika, sprawdzanie/OCD, lęk wolnopłynący albo reakcja jest nietypowo silna względem bodźca.
**Dlaczego:** Pełna tabela w każdym wpisie dziennika zwiększa tarcie i grozi porzuceniem trackingu. Bearable rozkłada wpisywanie w czasie i przypomina o nim powiadomieniami, a journal lepiej przechowuje kontekst, przebieg i znaczenie epizodu.
**Status:** aktywna

## 2026-06-27 — `journal/` jako bieżący dziennik życia, ze znacznikami tematów

**Decyzja:** Od teraz użytkownik pisze wpisy dziennika bezpośrednio w `journal/` (dotychczasowe wpisy pochodzą z importu z Diaro). Wpisy są pełne i pisane „dla siebie" — mogą obejmować zwykłe dni bez treści psychologicznej. Żeby zachować możliwość filtrowania sygnału, każdy wpis dostaje znaczniki w **YAML frontmatter** jako właściwość `tags` (kompatybilne z Obsidianem i łatwe do parsowania), np. `tags: [lęk, relacje]`; zwykły dzień bez treści psychologicznej → `tags: []`. Paleta tagów oparta na domenach mapy: `lęk, zobojętnienie, relacje, małżeństwo, ADHD, praca, ruch, sen, ludzie` (otwarta — nowy powracający tag jest sygnałem, że domena dojrzewa do `patterns/`). Dzień z epizodem lękowym zachowuje istniejącą konwencję: nagłówek `## HH:MM — epizod lęku` + blok „Minimum do zapisu" (patrz decyzja 2026-06-16 o Bearable). Komendy operujące na journal (`analyze-pattern`, `update-map`, `weekly-review`) mają przy liczeniu częstotliwości filtrować po `tags`, nie po liczbie plików.

**Dlaczego:** Jedno miejsce o niskim tarciu zwiększa szansę na regularność. Dyscyplina promocji (`journal/` → `patterns/` ≥3 dni → mapa) chroni mapę przed szumem niezależnie od liczby wpisów. Znaczniki rozwiązują jedyne realne ryzyko: rozcieńczenie sygnału psychologicznego w pełnym strumieniu życia oraz utrzymanie sensowności heurystyk częstotliwości.

**Uwaga (konfund do rozliczenia w mapie):** Korpus z Diaro był pisany nieregularnie i często jako „wentyl bezpieczeństwa w kryzysie", więc częstotliwość wpisów jest skonfundowana wzorcem pisania, nie tylko stanem. To podważa pewność dwóch wpisów mapy opartych na liczeniu wpisów: „Satysfakcja z życia / Rok 2019" (kontrast 1 vs 19 vs 22 epizody) oraz otwarte pytanie „Co się stało 2022–2023?". Do obniżenia pewności przez `update-map` w osobnym kroku.

**Status:** aktywna
