# Testy techniczne 4.44 — 31.10.2026

- 96/96 ilustracji odnaleziono i odczytano; 96/96 miniaturek dostępnych.
- 104 czynne oznaczenia, 7 nieprzypisanych wyłączonych i zachowanych w archiwum (łącznie 111 pozycji historycznych).
- Sześć rycin przejrzano pod kątem ogólnej topografii; **zero** rycin ma status pełnej weryfikacji anatomicznej.
- 20 siatek topograficznego szkicu 3D, 2106 trójkątów, poprawny zapis/odczyt GLB.
- Chromium: główny atlas, wybór struktury `infraspinatus`, marker, zakładka Kontrola 4.44, quiz i fiszki — brak błędów JS.
- Chromium (osobne laboratorium): renderer Canvas2D, 20 nazw siatek, ukrywanie nerwów/naczyń, wybór obiektu — brak błędów JS.
- Składnia `app.js` i skryptów `model3d_lab.html` sprawdzona.
- ZIP sprawdzony pod kątem integralności.

**Nieprzetestowane w pełni:** WebGL2 na GPU, duża jednoplikiowa wersja HTML w pełnej sesji przeglądarkowej, obsługa skompresowanych glTF/Draco/skinningu.
**Niezweryfikowane:** rzeczywiste relacje przestrzenne 20 parametrycznych siatek i dokładność 96 rycin oraz ich punktów.

**Dodatkowy test importu:** Chromium Canvas2D wczytał `regionalny_model_3d_444.glb` jako 20 siatek i 2106 trójkątów; bez błędów JS.
