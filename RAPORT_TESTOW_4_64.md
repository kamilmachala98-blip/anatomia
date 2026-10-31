# Raport testów — Anatomia z Graya 4.64

Data kontroli: 31 października 2026 r.

## Testy interfejsu i danych

Testy wykonano w Chromium (Playwright), uruchamiając HTML z osadzonymi danymi JSON oraz zaktualizowany plik `app.js`. Weryfikowano wykonanie JavaScript i interakcje, a nie dokładność anatomiczną rycin.

1. **Start atlasu i nazwa wersji:** zaliczono.
2. **Obecność danych:** 96 identyfikatorów obrazów; 104 historyczne mapowania; zaliczono.
3. **Otwieranie okolicy barku:** zaliczono.
4. **Nowy ekran „Warsztat”:** zaliczono.
5. **Zapis notatki źródłowej przy konkretnej parze rycina–struktura:** zaliczono.
6. **Eksport lokalnego audytu JSON ze schematem `gray-audit/1`:** zaliczono.
7. **Odmowa importu z nieprawidłowym schematem:** zaliczono.
8. **Przyciski poprzedniego/następnego oznaczenia:** obecność potwierdzona, wywołanie w aplikacji działa.
9. **Wskazanie mięśnia podgrzebieniowego na przypisanej rycinie:** obecność znormalizowanych współrzędnych potwierdzona; nie jest to walidacja anatomiczna.
10. **Ręczne przesunięcie punktu:** zaliczono; współrzędne zapisano.
11. **Cofnięcie i ponowienie przesunięcia:** zaliczono.
12. **Ukrywanie punktów zgłoszonych do korekty:** przełączenie stanu przetestowano.
13. **Zmiana warstwy w tej samej projekcji:** z przedramienia przedniego powierzchownego do pośredniego; zachowano widok przedni. Niezależne ilustracje nadal nie są zarejestrowane geometrycznie.
14. **Quiz i fiszki:** ekrany uruchamiają się bez błędów JS.
15. **Laboratorium 3D Canvas 2D:** załadowanie 20 siatek, wybór kierunku widoku; zaliczono.
16. **Wczytanie dostarczonego GLB 2.0:** parser wykazał 20 siatek i 2106 trójkątów; zaliczono.
17. **Błędy JavaScript:** w powyższych scenariuszach brak.

## Kontrola zasobów

- 96 pełnych ilustracji i 96 miniaturek WebP; wszystkie ścieżki z bazy atlasu wskazują istniejące zasoby.
- Wygenerowano manifest SHA-256 plików graficznych i aktualnego `app.js`.
- ZIP poddano kontroli `ZipFile.testzip()` — nie wykryto uszkodzonych wpisów.
- Zbudowano pojedynczy HTML z osadzonymi obrazami, miniaturami, CSS, JavaScript oraz modułem 3D.

## Co nie zostało w pełni potwierdzone

- **Pełne uruchomienie samodzielnego, 65 MB pliku HTML** na różnych urządzeniach i przeglądarkach — tego testu nie ukończono.
- Przegląd wszystkich 96 obrazów przez specjalistę anatomii — **nieukończony**.
- Weryfikacja wszystkich 104 oznaczeń na podstawie atlasów — **nieukończona**.
- Prawidłowość modelu 3D na podstawie segmentacji CT/MRI — **niezweryfikowana**, geometria jest poglądowa.
- Pełna zgodność importu z całym standardem glTF — **niepotwierdzona**, aplikacja obsługuje udokumentowany podzbiór niekompresowanych GLB.
