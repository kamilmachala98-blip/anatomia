# Anatomia z Graya 4.23 — testy i ograniczenia

Data: 31.10.2026.

## Testy wykonane

| Test | Wynik |
|---|---|
| Sprawdzenie składni `app.js` w Node.js | Zaliczone |
| Uruchomienie atlasu w Chromium (HTML/CSS/JS osadzone do testu) | Zaliczone |
| Wybranie mięśnia podgrzebieniowego na rycinie barku | Zaliczone |
| Przycisk „Otwórz w 3D” pojawia się przy strukturze z dokładnym odpowiednikiem nazwy siatki | Zaliczone |
| Przejście 2D → laboratorium 3D; zaznaczenie odpowiadającej siatki przez `postMessage` | Zaliczone (1 aktywna siatka) |
| Powrót 3D → atlas 2D z zachowaniem wybranej struktury | Zaliczone |
| Trening lokalizacji: ukrycie etykiety, wyświetlenie pytania, klikalne punkty i ocena odpowiedzi | Zaliczone |
| Otwieranie quizu | Zaliczone |
| Brak błędów JavaScript w powyższych interakcjach | Zaliczone |
| Kontrola zasobów: 96 pełnych rycin i 96 miniaturek | Zaliczone |
| Skompresowany ZIP: poprawność wpisów i integralność archiwum | Zaliczone |
| Samodzielny HTML: osadzenie 96 obrazów, miniaturek, modelu i aplikacji | Kontrola struktury — bez pełnego testu w przeglądarce |

## Zastrzeżenia

- W testach przeglądarkowych użyto odtworzenia kodu folderowego jako osadzonych HTML/CSS/JS w przeglądarce. Nie zastępuje to pełnego testu opublikowanej strony w Netlify ani 65 MB samodzielnego HTML.
- Model barku 3D pozostaje **uproszczonym demonstratorem**, niezależnym od atlasowo zweryfikowanej geometrii anatomicznej.
- Łączenie struktur 2D↔3D dotyczy tylko **czterech** dokładnych identyfikatorów i nie potwierdza poprawności geometrii.
- Wszystkie dotychczasowe znaczniki z wcześniejszych wersji nadal są **orientacyjne**; poprawność topograficzna całej biblioteki nie została ustalona.
- Trening lokalizacji wykorzystuje punkty orientacyjne. Nie należy interpretować jego wyniku jako oceny wiedzy na podstawie zweryfikowanego atlasu. Punkty zgłoszone do korekty są pomijane przy losowaniu.
- Importowane przez użytkownika modele GLB **nie otrzymują automatycznie powiązań anatomicznych na podstawie indeksu siatki**.

## Pliki

- `index.html`, `app.js`, `style.css` — atlas 2D i system audytu.
- `model3d_lab.html` — demonstracyjne laboratorium 3D z protokołem identyfikatorów.
- `mapowanie_nazw_3d_422.json` — rejestr nazw; w 4.23 dodane `exact_2d_atlas_links`.
- `assets/`, `thumbs/` — 96 obrazów i 96 miniaturek.
