# Anatomia z Graya 4.22 — raport testów

Testy wykonano 30.10.2026. Badanie dotyczy funkcji technicznych, nie anatomicznej poprawności rycin.

## Zaliczono

- Parsowanie JavaScript aplikacji (`node --check`).
- Parsowanie dwóch skryptów renderera 3D (`node --check`): ścieżka WebGL2 i ścieżka Canvas 2D.
- Render interfejsu atlasu w Chromium, wybór przycisku zgłoszenia całej ryciny — stan przechodzi na `wymaga-korekty`.
- Widoczność zgłoszenia w audycie i przejście z audytu do konkretnego obrazu.
- Otwarcie quizu (cztery opcje odpowiedzi) i fiszek.
- Renderer Canvas 2D 3D: scena narysowana, aktywne przyciski kierunków widoku, izolacja wybranej siatki i przywrócenie wszystkich siatek.
- Import `prototyp_3d_419.glb`: 7 siatek, 780 trójkątów; brak błędów JavaScript.
- Wszystkie obrazy regionalne wskazują istniejące pliki. W katalogu zachowano 96 obrazów i 96 miniaturek.
- Archiwum ZIP zawiera 205 plików, a test integralności `testzip()` nie zgłasza błędów.
- Samodzielny HTML zawiera skrypty aplikacji, model 3D i osadzone obrazy/miniatury.

## Ograniczenia

- Nie przeprowadzono pełnego, automatycznego uruchomienia jednoplikiowego HTML (~68 MB); spójność sprawdzono statycznie.
- W tej sesji testowano renderer **Canvas 2D**. Renderera WebGL2 nie potwierdzono w działaniu na sprzętowym GPU; sprawdzono jego składnię.
- Nie zweryfikowano anatomicznie 96 syntetycznych rycin ani 111 dawnych orientacyjnych lokalizacji znaczników.
- Model 3D pozostaje **szkicem demonstracyjnym** (7 siatek), nie zatwierdzonym modelem anatomii człowieka.
- Kierunki sceny 3D są zdefiniowane względem osi modelu demonstracyjnego; prawa/lewa strona nie jest anatomicznie skalibrowana.
