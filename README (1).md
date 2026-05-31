# Dziki Gon — Opowieść z Kontynentu

> Action-RPG w klimacie Wiedźmina 3, napisany w czystym vanilla JS + Canvas 2D.  
> Jeden plik HTML, zero dependencji, zero buildu — otwórz i graj.

---

## Opis

Wcielasz się w Geralta z Rivii i przemierzasz otwarty świat wzorowany na Velen. Tropujesz potwory, rozmawiasz z postaciami z lore, warzysz mikstury, grasz w Gwinta i ścigasz gryfa — główny cel fabularny. Gra działa całkowicie offline, w przeglądarce, z jednego pliku `wiedzmin-gpt.html`.

---

## Szybki start

```bash
git clone https://github.com/TWÓJ-LOGIN/NAZWA-REPO.git
cd NAZWA-REPO
# Otwórz plik w przeglądarce — nie trzeba serwera
open wiedzmin-gpt.html
```

Lub po prostu pobierz plik i przeciągnij do okna przeglądarki.  
Zalecane: Chrome / Edge (najlepsza wydajność Canvas). Firefox działa poprawnie.

---

## Sterowanie

| Akcja | Klawisz / Gest |
|---|---|
| Ruch | `W A S D` |
| Celowanie / obrót kamery (TPP) | Mysz |
| Atak szybki | `LPM` |
| Atak silny | `PPM` |
| Unik (Dasza) | `Spacja` |
| Bieg | `Shift` (przytrzymaj) |
| Blok / kontra | `Z` |
| Rzuć aktywny Znak | `X` |
| Alternatywny Znak | `Shift + X` / `Z + X` |
| Wybór Znaku | `1 – 5` |
| Mikstury z paska | `Alt + 1 – 5` |
| Interakcja / zbieranie | `E` |
| Wsiądź / zsiądź konia | `F` |
| Ekwipunek | `I` |
| Karta postaci / Mutageny | `C` |
| Alchemia | `L` |
| Mapa | `M` |
| Szybka Podróż | **Kliknięcie** na drogowskaz / miasto na Mapie (`M`) |
| Medytacja (Dynamiczna) | `R` |
| Przełącz widok 2D ↔ Perspektywa (Ostre High-DPI) | `P` |

---

## Mechaniki i Najnowsze Ulepszenia

### Świat
- Otwarta mapa **5200 × 4200** jednostek z czterema miastami, każde w osobnym biomie:
  - **Biały Sad** — złote łąki, wiatrak, płot
  - **Rozdroża** — gęste bory Velen, palisada, wieża strażnicza
  - **Wolne Miasto Novigrad** — kamienne zaułki, katedra, mur z blankami
  - **Bród nad Topielą** — moczary, chaty na palach
- Dynamiczny cykl dnia i nocy ze słońcem/księżycem wędrującym po niebie.
- Biomy (łąki, las, góry, miasto, moczary, wybrzeże) z płynnym mieszaniem.
- Atmosferyczna mgła dystansowa i winieta w trybie perspektywy.

### Walka i Satysfakcjonujący Combat Juice
- Dwa oręże: **stal** (ludzie i bestie) i **srebro** (potwory) — zły wybór karze obrażeniami ×0,5.
- System **parry / kontra** (`Z` w chwili uderzenia — wróg jest ogłuszony).
- **5 Znaków wiedźmińskich:** Aard, Igni, Quen, Yrden, Axii — każdy z cooldownem i kosztem wigoru.
- **Efekt Hit-Stop (NOWOŚĆ)**: Mikrozamrożenie klatki (na 50 ms) przy zadaniu uderzenia krytycznego. Nadaje walce niesamowitą fizyczną wagę i satysfakcję.

### Pełna Synteza Dźwięków (NOWOŚĆ)
Gra posiada wbudowany **w pełni syntetyczny generator dźwięków** oparty na **Web Audio API**. Gra generuje sygnały dźwiękowe bezpośrednio w przeglądarce bez ściągania żadnych plików `.mp3` ani zależności:
- **Szum miecza** przy każdym machnięciu szybkim i silnym.
- **Tępe basowe tąpnięcie** w momencie otrzymania ciosu.
- **Dźwięk buchającego ognia** w czasie rzucania Znaku Igni.
- **Wspaniała melodyjna fanfara (arpeggio)** przy awansie na wyższy poziom doświadczenia lub szybkiej podróży.

### Interaktywna Szybka Podróż (NOWOŚĆ)
Koniec z wielominutowymi podróżami na piechotę. Panel Mapy (`M`) jest teraz w pełni interaktywny! Kliknięcie na ikonę dowolnego miasta lub odkrytego drogowskazu (Signpost) natychmiast teleportuje Geralta oraz jego wierną Płotkę w wybrane miejsce.

### Płynna Dynamiczna Medytacja (NOWOŚĆ)
Zamiast statycznego czarnego ekranu, medytacja (`R`) korzysta teraz z **przezroczystego ciemnego overlayu oraz 60 FPS płynnego przyspieszenia czasu**. Podczas medytacji Geralt odpoczywa, a na ekranie w czasie rzeczywistym możesz obserwować płynny ruch chmur, cieni oraz wędrującego po niebie słońca i księżyca.

### Potwory
| Potwór | Klasa | HP | Uwagi |
|---|---|---|---|
| Utopiec | Nekro | 60 | stadny, przy wodzie |
| Ghul | Nekro | 80 | nocny |
| Wilk | Bestia | 40 | w watahach |
| Nekker | Bestia | 50 | dziurawi teren |
| Niedźwiedź | Bestia | 160 | silny |
| Zjawa | Nekro | 120 | szybka, wrażliwa na srebro |
| **Gryf** (boss) | Hybryda | 380 | nurkuje, lata, wymaga Yrden |

### Alchemia
Zbieraj zioła (`E`) i warz mikstury w menu **L**:
- Jaskółka — regeneracja HP
- Grom — bonus do obrażeń
- Płomykówka — regeneracja wigoru
- Kocie Oko — widzenie w nocy
- Olej na hybrydy — bonus vs. Gryf

### Gwint
Pełna gra karciana przeciwko Karczmarzu Hofmeierowi — do 3 rund, ręka 10 kart.  
Karty na ręce są duże i czytelne: ikona, siła, rząd słowem (Zwarcie / Dystans / Oblężenie).  
Najechanie na kartę **podświetla docelowy rząd** na planszy. Wygrana = 100 koron + 30 XP.

### Questy
1. **Bestia z Białego Sadu** — główny wątek, zakończony walką z Gryfem i wyborem moralnym (uśpienie gryfa zamiast zabijania)
2. **Zaraza utopców** — zlecenie na 5 utopców
3. **Nauka rzemiosła** — uwarzyć pierwszą miksturę

---

## Widoki kamery

| Tryb | Opis |
|---|---|
| **Rzut z góry** (domyślny) | Klasyczny top-down z kamerą śledzącą gracza. |
| **Perspektywa** (`P`) | Widok TPP (trzecioosobowy). **ZAAWANSOWANE NOWOŚCI (Pakiet Kamery)**:<br>- **Pointer Lock API**: Kliknięcie ekranu blokuje mysz, umożliwiając pełny, nieograniczony obrót kamery 3D we wszystkich kierunkach (YAW + PITCH).<br>- **Pionowy ruch kamery**: Ruch myszą w pionie (Y-axis) pochyla kamerę góra/dół, zmieniając wysokość horyzontu i terenu.<br>- **Dynamiczny Zoom (FOV)**: Kamera płynnie dopasowuje odległość (przybliża się w wioskach do 114 dla ujęć filmowych, oddala do 158 podczas sprintu i do 168 w walce dla lepszej widoczności pola bitwy).<br>- **Widok zza ramienia (Over-the-shoulder)**: Klasyczne filmowe przesunięcie Geralta lekko w lewo na ekranie.<br>- **High-DPI Support**: Pełne, niesamowicie ostre renderowanie 3D. |

---

## Wysoce Zoptymalizowana Architektura TPP
W najnowszej wersji wprowadzono **cache'owanie obliczeń trygonometrycznych na poziomie renderera**. Zamiast wyliczać `Math.cos`/`Math.sin` osobno dla każdego z setek drzew i kamieni w każdej klatce, silnik wylicza je tylko raz na klatkę. Zapewnia to drastyczny wzrost FPS i eliminuje jakiekolwiek przycięcia w trybie perspektywicznym.

---

## Architektura pliku

```
wiedzmin-gpt.html
├── <style>          — cały CSS (zmienne CSS, HUD, panele, Gwint, TPP, dynamiczne zamazanie)
├── <body>           — HTML szkielet (canvas, HUD, overlaye)
└── 8x <script>      — globalne bloki JS (brak modułów, 'use strict' w s0)
    ├── s0  config, helpery, generator dźwięków AudioSynth, gracz, walka, pętla loop
    ├── s1  BIOMY, generacja świata (E.trees/rocks/grass...)
    ├── s2  POI, światła, wędrowcy, dialogi, alchemia, otwarcie mapy
    ├── s3  UI (ekwipunek, mapa, alchemia, karta postaci)
    ├── s4  HUD, budowanie kart postaci
    ├── s5  System wzmocnień (GPT_GAMEPLAY), interaktywna mapa i Szybka Podróż
    ├── s6  Systemy środowiskowe (GPT_SYSTEMS, tropy, zlecenia), bezpieczny zapis localStorage
    └── s7  Renderer TPP, zoptymalizowana kamera 3D z cache'owaniem trigów, miasta 3D, alternatywne znaki
```

---

## Wymagania techniczne

- Przeglądarka z obsługą **Canvas 2D** i **ES6+**
- Żadnych node_modules, żadnego bundlera.
- Plik jest w pełni samodzielny — tło ekranu tytułowego zakodowane jako base64 WebP (~177 KB).
- **Zapis gry z ulepszonym fallbackiem**: Zapis trzymany jest w `localStorage` (pod kluczem `wiedzmin-gpt-save-v4`) dla pełnego bezpieczeństwa. W przypadku ograniczeń sandboxowych przeglądarki, gra automatycznie korzysta z bezpiecznego trybu w pamięci sesji.

---

## Pomysły na rozwój / TODO

- [ ] Kilka dodatkowych questów pobocznych
- [ ] System poziomowania Znaków
- [ ] Więcej kart Gwinta i przeciwnicy karcianie w każdym mieście
- [x] Tryb mapowy z szybką nawigacją (Szybka Podróż)
- [x] Efekty dźwiękowe (Web Audio API, bez dependencji)
- [ ] Więcej NPCs z drzewami dialogowymi

---

## Licencja

Projekt fanowski, non-profit. Wiedźmin / The Witcher to marka CD Projekt RED.  
Kod gry udostępniony na licencji **MIT** — możesz go forkować, modyfikować i budować na nim, o ile zachowasz informację o oryginalnym autorze.

---

*Napisane w vanilla JS + Canvas 2D, bez frameworków, bez buildu.*  
*Jeden plik. Otwierasz, grasz.*
