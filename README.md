# Naturalne pisanie

Skill do pisania i redagowania tekstów tak, żeby brzmiały jak napisane przez człowieka — konkretnie, adekwatnie do gatunku i bez powtarzalnych manier generycznego stylu modeli językowych. Działa po polsku i ma osobną warstwę dla tekstów prawniczych.

Nie obiecuje niewykrywalności przez detektory AI i nie optymalizuje tekstu pod detektor. Nie traktuje pojedynczego słowa ani znaku interpunkcyjnego jako dowodu autorstwa maszyny.

## Co robi inaczej

Większość instrukcji „pisz naturalnie" to czarne listy słów. Ta działa odwrotnie: **domyślną odpowiedzią jest brak zmiany**.

- Reaguje dopiero wtedy, gdy cecha się powtarza, występuje w skupieniu z innymi manierami albo nie pasuje do gatunku.
- Zachowuje trafne, charakterystyczne sformułowania autora zamiast je wygładzać.
- Nie wymusza sztucznej zmienności długości zdań ani „uczłowieczania" przez literówki i urwaną interpunkcję.
- Nie wymyśla faktów, źródeł, sygnatur ani przepisów. Przy brakach wstawia znacznik, np. `[data]`, `[źródło]`.

## Struktura

| Plik | Kiedy się wczytuje |
|---|---|
| `SKILL.md` | zawsze — zasady twarde, korekcyjne i sygnały ostrzegawcze |
| `references/naturalny-styl.md` | dłuższa redakcja, tekst publikacyjny, kilka powtarzalnych problemów |
| `references/polszczyzna.md` | dłuższy tekst po polsku: kalki, nominalizacje, urzędniczy ton |
| `references/polszczyzna-przyklady.md` | gdy potrzebne są konkretne zamienniki kalek |
| `references/tekst-prawniczy.md` | teksty prawne, procesowe, kontraktowe i eksperckie o prawie |

Referencje nie ładują się wszystkie naraz — `SKILL.md` wskazuje, kiedy sięgnąć po którą. Przy krótkim tekście wystarcza sam `SKILL.md`.

## Instalacja

### Claude Code

Dla wszystkich projektów:

```bash
git clone https://github.com/PiotrKantorowski/naturalne-pisanie.git ~/.claude/skills/naturalne-pisanie
```

Tylko dla jednego projektu — sklonuj do `.claude/skills/naturalne-pisanie/` w katalogu projektu.

Po restarcie sesji skill pojawi się na liście i można go wywołać przez `/naturalne-pisanie`.

### Inne narzędzia

Katalog `agents/` zawiera opis interfejsu dla platform, które czytają metadane z osobnego pliku. Sam skill to zwykły Markdown — da się go użyć wszędzie tam, gdzie można podać modelowi instrukcję systemową.

## Warstwa prawnicza

`references/tekst-prawniczy.md` to **wyłącznie warstwa redakcyjna**. Nie zastępuje researchu prawnego ani skilla merytorycznego i nie nadpisuje zweryfikowanych wniosków prawnych. Pilnuje m.in. tego, żeby:

- argument przechodził pełną drogę *teza → podstawa → zastosowanie → skutek*, ze szczególnym naciskiem na zastosowanie do konkretnych faktów,
- terminy prawne nie były traktowane jak synonimy stylistyczne,
- forma pisma nie była mylona z kompletnością treści.

## Format wyjścia

Domyślnie skill zwraca sam gotowy tekst — bez „Oto propozycja", bez omówienia zmian i bez informacji o tym, że w ogóle zadziałał.
