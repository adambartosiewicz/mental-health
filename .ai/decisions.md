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
