# Platformy do nauki anatomii i inspiracje techniczne

Data przeglądu: 2026-10-31. Nie jest możliwe zagwarantowanie kompletnej listy wszystkich platform na świecie. Poniżej wybrane, publicznie weryfikowalne rozwiązania.

## Otwarte repozytoria (można analizować publiczny kod i architekturę)

- **Open Anatomy Atlas** — https://github.com/CognitionLabSNUC/open-anatomy-atlas — MIT (kod); hierarchie part-of / is-a, widoki przekrojowe, atlas offline, 3D quiz. Dane anatomiczne wymagają osobnej analizy licencji.
- **OABrowser** — https://github.com/mhalle/oabrowser — przeglądarka atlasów WebGL, architektura rozdzielająca dane atlasowe od widoku.
- **Human-Atlas (slorksmo)** — https://github.com/slorksmo/Human-Atlas — kod MIT, 3D Three.js z wyborem siatek, etykietami, wielojęzycznością i wsparciem RTL; modele CC BY (odrębna licencja).
- **Body Atlas 3D (ImliStack)** — https://github.com/ImliStack/Body-Atlas-3D — izolacja, etykiety przytwierdzone do modelu, bookmarki URL, PWA, renderer fallback, skróty.
- **Body Atlas (yamz8)** — https://github.com/yamz8/human-body-simulator — Vite + Three.js, płynna przezroczystość, awaryjny model, walidacja pozycjonowania siatek.
- **Human Atlas (ashemag)** — https://github.com/ashemag/human-atlas — liczne siatki i wyszukiwanie części; szczególna uwaga na separację kodu MIT od licencji danych.
- **Z-Anatomy (nqwrc)** — https://github.com/nqwrc/3d-anatomy — wielowarstwowa wizualizacja i tryb isolate; repo zawiera zróżnicowane licencje (w tym NC), nie kopiować danych do publicznego projektu bez audytu.
- **Open Twin XR** — https://github.com/Opening-Science/open-twin-xr — warstwa renderowania oddzielona od danych i metryk.

## Platformy, których wewnętrzny kod nie jest publicznie udostępniany jako otwarte repozytorium

- **Complete Anatomy (Elsevier)** — https://www.elsevier.com/products/complete-anatomy — tryb preparowania i izolowania, quizy, własne widoki, radiologia.
- **BioDigital Human** — https://www.biodigital.com/product/the-biodigital-human — opisy, modelowanie lekcji/tour, tworzenie quizów i osadzanie widoków.
- **Anatomyka** — https://www.anatomyka.com/ — wielojęzyczność, predefiniowane regiony, przypięte etykiety.
- **Anatomy 3D Atlas** — https://anatomy3datlas.com/features/ — przezroczystość, przypięte etykiety, centrum obrotu, izolacja, ukrywanie.
- **Anatomage Table** — https://anatomage.com/table/ — rzeczywiste obrazowanie zwłok / preparowanie warstwowe i przekroje.
- **Visible Body** — https://libguides.lib.miamioh.edu/visiblebody/content-tools — porównania z preparatami i obrazowaniem, przekroje, anotacje.

## Ograniczenia audytu kodu

Publiczne strony repozytoriów, ich opisy i drzewa plików były dostępne; próby pobrania części plików źródłowych z GitHub i raw.githubusercontent.com nie powiodły się w tym środowisku. Nie twierdzę więc, że przejrzałem kod każdego wymienionego projektu linia po linii. Techniczne rozwiązania poniżej zostały samodzielnie zaimplementowane w naszym kodzie bez kopiowania zasobów.

## Wykorzystane pomysły

1. Testowalne rozdzielenie atlasu 2D i szkicu 3D; sterowanie dockiem naprawione.
2. Deep-link do ryciny i struktury w adresie URL.
3. Nawigacja klawiaturą i skróty.
4. Walidacja punktów znormalizowanych do oryginalnej ryciny.
5. Oddzielenie oznaczeń zgłoszonych do korekty.
6. Zestawienie kilku ujęć jednej struktury.
7. Eksport statusów audytu do CSV.
8. Sesyjna powtórka błędnie rozpoznanych struktur.
9. Jawne provenance geometrycznego szkicu 3D.
10. Ujednolicenie informacji o jakości i udostępnianie widoków.

**Licencje:** sam kod źródłowy MIT/Apache nie upoważnia automatycznie do użycia siatek, obrazów lub baz opatrzonych CC BY-SA, NC lub innym ograniczeniem. Każde pobranie gotowego modelu wymaga osobnej kontroli licencji i atrybucji.
