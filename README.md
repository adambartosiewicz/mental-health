# Mental Health

Długoterminowy system osobistej obserwacji psychologicznej. Celem jest **wykrywanie wzorców w skali miesięcy i lat** w służbie **zmiany zachowania** — nie terapia, nie pisanie dziennika dla samego pisania, nie śledzenie objawów.

Obszary: ADHD, lęk, samoocena, relacje, satysfakcja z życia, eksperymenty behawioralne.

Repozytorium jest zoptymalizowane do współpracy z asystentami AI w długim okresie.

---

## Pojedyncze źródło prawdy

W tym repozytorium jest dokładnie jeden autorytatywny dokument o mnie:

**`psychological-map.md`** (w katalogu głównym).

Wszystko inne istnieje, żeby ten plik wspierać, aktualizować lub dostarczać mu dowodów. Mapa powinna być czytelna sama z siebie, bez przeglądania reszty repo. Jeśli informacje zaczynają żyć gdzie indziej i nigdy nie docierają do mapy — system zawiódł.

Docelowy rozmiar mapy: **3–10 stron.** Jeśli urośnie ponad to — przytnij albo zarchiwizuj.

---

## Przepływ informacji

```
journal/  ──┐
            ├──►  patterns/  ──►  psychological-map.md
sessions/ ──┘                              ▲
                                           │
experiments/  ─── wyniki ──────────────────┘

references/   (wejście z zewnątrz — nigdy automatycznie nie wlewane do mapy)
archive/      (materiał wycofany — przenoszony tu, nie usuwany)
```

Reguły:

1. **Surowa obserwacja → `journal/`.** Pojedyncze zdarzenia, wyładowania, fragmenty. Bez presji promocji.
2. **Ustrukturyzowana rozmowa → `sessions/`.** Podsumowania znaczących rozmów z AI. Tymczasowe dokumenty robocze.
3. **Powtarzalność → `patterns/`.** Gdy ta sama obserwacja pojawi się w ≥3 różnych dniach, ląduje w odpowiednim pliku `patterns/<domena>.md`. Wzorce to **artefakty analityczne**, nie źródła prawdy. Wspierają mapę; nie zastępują jej.
4. **Mocne dowody → `psychological-map.md`.** Tylko dobrze udokumentowane, trwałe ustalenia trafiają do mapy. Mapa aktualizowana jest przez komendę `update-map` po świadomym przeglądzie.
5. **Hipotezy → `experiments/`.** Gdy coś w mapie wymaga sprawdzenia — albo zanim awansujesz interpretację — zaprojektuj eksperyment behawioralny.
6. **Materiał zewnętrzny → `references/`.** Artykuły, materiały o ADHD, pojęcia z terapii, frameworki. **Nigdy automatycznie nie wlewane do mapy.**
7. **Materiał wycofany → `archive/`.** Gdy coś w mapie się dezaktualizuje, stara wersja trafia tu z datą; nowy wpis linkuje wstecz. Nic nie jest usuwane.

---

## Cykl życia mapy

`psychological-map.md` ewoluuje wolno i świadomie.

- **Dodawaj** wpis tylko wtedy, gdy istnieją co najmniej 3 odrębne obserwacje wspierające go z różnych dni.
- **Aktualizuj** wpis tylko przez komendę `update-map`, która najpierw produkuje propozycję zmian.
- **Zastępuj** zamiast nadpisywać: przenieś starą wersję do `archive/psychological-map-<data>.md`, napisz zastępczą, podlinkuj wstecz.
- **Degraduj** zamiast usuwać: gdy wzorzec słabnie, oznacz `pewność: obniżona, obserwuj`. Usunięcie następuje tylko po dłuższej nieobecności.
- **Cytuj dowody** w każdym nietrywialnym wpisie: linkuj do `patterns/`, `sessions/` lub `experiments/`.
- **Oddzielaj obserwację od interpretacji.** Każdy wpis ma jedno i drugie, wyraźnie rozdzielone, plus poziom pewności.

---

## Rola eksperymentów

System preferuje **eksperymenty nad spekulacją**.

Gdy w mapie znajduje się interpretacja, która stała się nośna, albo otwarte pytanie, które codzienne życie mogłoby przetestować — zaprojektuj eksperyment pod `experiments/`. Eksperymenty mają ramy czasowe, z góry określone kryteria sukcesu i porażki, oraz pisemne podsumowanie zamknięcia — w tym te negatywne i porzucone.

> „Co mogę przetestować?" wygrywa z „Dlaczego taki jestem?"

---

## Rola asystentów AI

Asystenci AI są **współpracownikami przy utrzymaniu** tego repozytorium, nie rozmówcami, którzy uspokajają.

### Zasady dla AI przy przetwarzaniu nowych informacji

1. **Zapisuj obserwacje w `journal/`**, gdy są surowe i datowane.
2. **Wykrywaj powracające tematy w `patterns/`** — promuj dopiero po powtórzeniu.
3. **Aktualizuj `psychological-map.md` tylko wtedy, gdy dowody są mocne.** Nigdy na podstawie jednej rozmowy.
4. **Oddzielaj obserwacje od interpretacji** w każdym output. Oznaczaj hipotezy jako hipotezy.
5. **Unikaj workflowów szukających uspokojenia.** Żadnego „świetnie ci idzie". Żadnych pętli uspokajających wokół konkretnej treści lękowej.
6. **Preferuj eksperymenty nad spekulacją.** Gdy interpretacja staje się lepka, zaproponuj eksperyment zamiast się z nią zgadzać.

### Czego AI ma odmawiać

- Diagnozowania.
- Generowania uspokojenia bez konkretnego oparcia.
- Wytwarzania list „rzeczy, które mógłbyś spróbować", gdy użytkownik się wyżala (najpierw zapytaj, czy chce opcji, czy towarzyszenia).
- Traktowania jednego złego dnia jako trendu.
- Pozwalania, by materiał z `references/` przepłynął do mapy bez wyraźnej zgody człowieka.

Pełny kontekst dla AI żyje w `.ai/context.md`. Wielokrotnego użytku workflow żyją w `.ai/commands/`.

---

## Mapa katalogów

```
mental-health/
├── README.md                      ten plik
├── psychological-map.md           pojedyncze źródło prawdy
├── .ai/                           warstwa współpracy z AI
│   ├── context.md                   jak AI ma podejść do tego repo
│   ├── decisions.md                 trwałe decyzje o samym systemie
│   ├── session-log.md               chronologiczny indeks sesji
│   └── commands/                    wielokrotnego użytku workflow AI
├── journal/                       surowe, datowane obserwacje (tylko dopisuj)
├── sessions/                      ustrukturyzowane podsumowania rozmów
├── patterns/                      artefakty analityczne (anxiety, adhd, …)
├── experiments/                   eksperymenty behawioralne (aktywne i zamknięte)
├── references/                    materiał zewnętrzny — nigdy automatycznie nie wlewany
└── archive/                       wycofane wpisy mapy i wzorców
```

---

## Język

Domyślnym językiem tego repozytorium jest **polski**. Cała zawartość plików (mapa, wzorce, sesje, journal, eksperymenty, materiały) ma być po polsku. Nazwy plików i katalogów oraz komendy w `.ai/commands/` zostają po angielsku ze względów technicznych, ale **wyniki generowane przez komendy mają być po polsku**.

---

## Metryka sukcesu

To repozytorium istnieje, żeby wspierać:

- **większe życie**
- **mniej unikania**
- **większą elastyczność psychologiczną**
- **większe zaangażowanie w to, co ważne**
- **lepsze rozumienie siebie**

Repozytorium **NIE istnieje wyłącznie po to, żeby zmniejszać lęk.** Spadek lęku nie jest celem. Lęk może spaść, bo życie się skurczyło — to porażka. Lęk może wzrosnąć, gdy życie się powiększa — to może być sukces.

Jeśli mapa staje się uczciwsza, eksperymenty się dzieją, unikanie jest nazywane, a zaangażowanie rośnie — system działa.
