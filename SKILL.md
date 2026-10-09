---
name: naturalne-pisanie
description: Twórz i przerabiaj teksty tak, aby brzmiały naturalnie, konkretnie i nieschematycznie, bez typowych manier generycznego stylu AI. Używaj przy pisaniu od zera i redakcji artykułów, postów, opisów, newsletterów, raportów, komentarzy, odpowiedzi, tekstów na strony, scenariuszy, pism i notatek, zwłaszcza po polsku. Stosuj także jako warstwę stylistyczną do tekstów eksperckich i prawniczych. Domyślnie zwracaj gotowy tekst. Samodzielnie nie pozyskuj faktów ani nie uruchamiaj connectorów; pracuj na materiale z rozmowy lub dostarczonym przez inne aktywne narzędzia/skille.
---

# Naturalne pisanie

## Cel

Twórz tekst, który brzmi jak napisany przez kompetentnego człowieka: konkretnie, adekwatnie do sytuacji i bez powtarzalnych manier generycznych odpowiedzi modeli językowych.

Nie obiecuj niewykrywalności przez detektory AI. Nie optymalizuj tekstu pod detektor i nie traktuj pojedynczego słowa, znaku interpunkcyjnego ani konstrukcji jako dowodu autorstwa AI.

## Zasada nadrzędna: minimalna potrzebna ingerencja

Najpierw wykonaj polecenie użytkownika. Potem poprawiaj tylko to, co rzeczywiście pogarsza tekst.

- Zachowuj trafne, charakterystyczne sformułowania autora.
- Nie wygładzaj tekstu dla samego wygładzenia.
- Nie zmieniaj tonu, stanowiska ani kategoryczności bez potrzeby.
- Jeżeli fragment jest naturalny, precyzyjny i pasuje do gatunku, zostaw go bez zmian.
- Brak zmiany jest prawidłowym wynikiem redakcji.

Przy redakcji najpierw rozpoznaj elementy warte zachowania, dopiero potem problemy do naprawy.

## Hierarchia reguł

### 1. Reguły twarde

Stosuj zawsze:

- zachowaj sens, stanowisko autora i istotne informacje,
- nie wymyślaj faktów, cytatów, źródeł, danych ani doświadczeń autora,
- respektuj wskazany ton, format, odbiorcę i poziom formalności,
- zachowuj właściwą terminologię,
- nie humanizuj tekstu przez celowe błędy, literówki lub przypadkowe kolokwializmy,
- nie zastępuj naturalnego słowa rzadszym synonimem tylko dla pozornej różnorodności.

### 2. Reguły korekcyjne

Stosuj tylko wtedy, gdy rozpoznasz problem, np.:

- niską gęstość informacji lub powtarzanie tej samej myśli,
- generyczne wstępy i puenty,
- monotonną składnię albo identyczny ciężar kolejnych zdań,
- nadmierne „zszywanie” tekstu łącznikami,
- seryjne trójki, paralelizmy lub kontrasty,
- nieadekwatne formatowanie,
- kalki językowe, urzędniczo-korporacyjny rejestr lub pozorne autorytety.

### 3. Sygnały ostrzegawcze

Nie poprawiaj tekstu tylko dlatego, że wystąpił pojedynczy sygnał, np. myślnik, słowo „kluczowy”, lista trzech elementów, „ponadto” albo konstrukcja „nie tylko..., ale także...”.

Reaguj, gdy cecha:

- powtarza się,
- występuje w skupieniu z innymi manierami,
- jest niedopasowana do gatunku albo autora,
- faktycznie pogarsza precyzję, rytm lub czytelność.

W razie wątpliwości preferuj zachowanie poprawnego fragmentu zamiast jego przerabiania.

## Dobór głębokości

Nie ładuj wszystkich referencji automatycznie.

**CORE — bez dodatkowych referencji:** używaj przy krótkich, prostych tekstach oraz wtedy, gdy powyższe zasady wystarczają do wykonania zadania.

**DEEP — `references/naturalny-styl.md`:** wczytaj przy dłuższej redakcji, artykule, raporcie, newsletterze lub gdy użytkownik wyraźnie chce usunąć generyczny/AI-owy charakter tekstu albo rozpoznasz kilka powtarzalnych problemów stylistycznych.

**POLSKI — `references/polszczyzna.md`:** wczytaj dla dłuższego lub publikacyjnego tekstu po polsku, zwłaszcza gdy pojawiają się kalki, nominalizacje, urzędniczy ton albo nienaturalne łączniki. Przy krótkim, prostym polskim tekście nie musisz go wczytywać.

**PRZYKŁADY POLSKIE — `references/polszczyzna-przyklady.md`:** wczytaj tylko wtedy, gdy potrzebujesz konkretnych przykładów kalek i naturalniejszych zamienników. Nie używaj go jako czarnej listy.

**LEGAL — `references/tekst-prawniczy.md`:** wczytaj dla tekstów prawnych, prawniczych, procesowych, kontraktowych i eksperckich o prawie. To wyłącznie warstwa redakcyjna; nie zastępuje researchu prawnego ani skilla merytorycznego i nie może nadpisywać zweryfikowanych wniosków prawnych.

## Treść przed szlifem

Najpierw sprawdź, czy tekst realizuje cel użytkownika i czy akapity mają funkcję. Usuwaj przede wszystkim fragmenty, które ani nie dodają informacji, argumentu, przykładu czy zastrzeżenia, ani nie pomagają odbiorcy zrozumieć treści.

Nie rób jednak z tekstu telegramu. Zdanie może pełnić funkcję objaśniającą, łączącą, rytmiczną lub retoryczną, jeżeli rzeczywiście pomaga czytelnikowi.

Nie wymuszaj sztucznej zmienności długości zdań. Nie wyrównuj rytmu; pozwól mu wynikać z treści.

## Pisanie od zera i redakcja

Rozpoznaj automatycznie, czy użytkownik chce napisać tekst od zera, czy poprawić istniejący materiał. Nie wymagaj specjalnych komend ani formularza.

Przy redakcji ingeruj oszczędnie. Jeżeli użytkownik mówi „zachowaj mój styl”, traktuj to jako silne ograniczenie i zmieniaj przede wszystkim fragmenty szablonowe, nieprecyzyjne albo nienaturalne.

## Fakty i źródła

Nie twórz z pamięci pozornie wiarygodnych przypisów, sygnatur, tytułów publikacji, numerów przepisów ani nazw instytucji, jeżeli nie wynikają z materiału wejściowego lub zweryfikowanych danych dostarczonych przez inne aktywne narzędzie/skill.

Jeżeli brakująca informacja jest konieczna, użyj neutralnego znacznika, np. `[data]`, `[kwota]`, `[nazwa]`, `[źródło]`, zamiast zgadywać.

## Format wyjścia

Domyślnie zwracaj wyłącznie gotowy tekst do skopiowania lub publikacji. Nie dodawaj „Oto propozycja”, omówienia zmian ani informacji o działaniu skilla, chyba że użytkownik o to poprosi.

Dopasuj konwencję do medium. Post nie ma brzmieć jak raport, artykuł jak pismo procesowe, a analiza jak wpis na LinkedIn.

## Kontrola końcowa

Przed zwróceniem tekstu sprawdź po cichu:

1. Czy tekst realizuje cel użytkownika i zachowuje jego stanowisko?
2. Czy poprawki dotyczą rzeczywistych problemów, a nie samego faktu, że można coś przepisać inaczej?
3. Czy zachowano dobre, charakterystyczne fragmenty autora?
4. Czy tekst nie powtarza tej samej myśli i nie zawiera pustych ogólników?
5. Czy rytm wynika z treści, a nie z mechanicznego mieszania długości zdań?
6. Czy nie ma skupisk szablonowych konstrukcji, łączników, trójek, kontrastów lub sztucznego formatowania?
7. Czy żadnej pojedynczej cechy nie potraktowano jak zakazanej?
8. Czy nie wprowadzono nieuzasadnionych faktów, źródeł ani terminów?
9. Jeżeli tekst jest po polsku: czy brzmi idiomatycznie, a nie jak kalka?
10. Jeżeli tekst jest prawniczy: czy styl nie zaciemnia terminologii, argumentu ani związku z konkretnym problemem?

Zwróć dopiero wersję po tej kontroli.
