AG Modern Electrics — propozycje projektu strony (poglądowe)
==============================================================

ZAWARTOŚĆ PAKIETU
------------------
- index.html                        -> strona-prezentacja z podglądem wszystkich 10 wariantów (do pokazania klientowi)
- wariant-1-klasyczny.html          -> Klasyczny / Korporacyjny
- wariant-2-bold.html               -> Bold / Energetyczny (dark mode)
- wariant-3-minimalistyczny.html    -> Minimalistyczny / Premium
- wariant-4-konwersyjny.html        -> Konwersyjny / Usługowy (formularz wyceny w hero)
- wariant-5-diagonalny.html         -> Diagonalny / Dynamiczny (przekątny podział hero)
- wariant-6-magazynowy.html         -> Magazynowy / Bento grid (asymetryczna siatka)
- wariant-7-sidebar.html            -> Sidebar Navigation (pionowe menu boczne sticky)
- wariant-8-dashboard.html          -> App-like Bento Dashboard (kafelkowy, aplikacyjny)
- wariant-9-fullbleed.html          -> Full-bleed Hero z overlayem (pełnoekranowe, wyśrodkowane)
- wariant-10-swiss.html             -> Swiss / Poster Big Type (duża typografia, płaskie bloki koloru)
- assets/icon.png, assets/logo-full.png -> zoptymalizowane wersje dostarczonego logo

JAK OTWORZYĆ
------------
To zwykłe pliki HTML — wystarczy kliknąć dwukrotnie (otworzą się w przeglądarce).
Najlepiej otworzyć index.html — tam widać wszystkie 10 wariantów obok siebie z linkami
do pełnych podglądów ("Otwórz pełny podgląd" otwiera wariant w nowej karcie — działa
nawet gdy plik index.html jest otwarty samodzielnie, bez reszty plików obok). Każdy
wariant jest w pełni responsywny (przetestowany na widoku mobilnym).

KOLORYSTYKA MARKI (wyciągnięta bezpośrednio z logo)
----------------------------------------------------
Czerwień:  #C63157
Granat:    #3F5E9A

Wszystkie 10 wariantów trzyma się tej samej kolorystyki — różnią się układem,
kompozycją i charakterem (jasne/ciemne, klasyczne/dynamiczne, minimalistyczne/
maksymalistyczne), tak żeby strona pozostała spójna z dostarczonym logo
niezależnie od wybranego kierunku.

TREŚCI
------
Wszystkie teksty (usługi, opinie, dane kontaktowe, statystyki) są przykładowe —
to placeholdery pokazujące strukturę i ton komunikacji. Przed wdrożeniem trzeba
je podmienić na docelowe treści klienta.

DALSZE KROKI (Next.js)
-----------------------
Po wybraniu wariantu przez klienta, strukturę HTML/CSS łatwo przenieść na komponenty:
- Header/Nav -> components/Header.tsx
- Hero -> components/Hero.tsx
- Sekcja usług (grid/bento kart) -> components/Services.tsx + tablica danych
- "Dlaczego my" / stats -> components/WhyUs.tsx
- Opinie -> components/Testimonials.tsx
- CTA + formularz (wariant 4) -> components/QuoteForm.tsx (z realną integracją, np. wysyłka maila / webhook)
- Footer -> components/Footer.tsx

Czyste CSS w plikach (bez frameworka) można 1:1 przepisać na CSS Modules / Tailwind —
nazwy klas są semantyczne i łatwe do zmapowania. Grafiki logo (assets/) trafiają
do folderu public/ w projekcie Next.js.
