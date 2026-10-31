# Raport kontroli wersji 4.34

Data: 2026-10-31. Testy dotyczą kodu i funkcji interfejsu, nie walidacji anatomicznej obrazów.

## Potwierdzone

- 10 kolejnych zestawów zmian w kodzie, z zapisem każdej iteracji i sumami SHA-256.
- 96 wcześniejszych rycin i 96 miniaturek zostało zachowanych.
- Istnieją wszystkie odwołania do plików `DATA.assets`.
- `node --check app.js`: bez błędów składni.
- Przeglądarka Chromium: wczytanie głównego UI, od razu działający dok 3D, zamknięcie doku, quiz 4-odpowiedziowy, fiszki, link do widoku i przejście do audytu — bez błędów JavaScript.
- Quiz 10 pytań: 10 celowo błędnych odpowiedzi → sesja błędów 10 pytań; poprawny przycisk powtórki.
- Eksport listy punktów w CSV z właściwą nazwą pliku.
- Laboratorium 3D Canvas2D: 7 siatek w demonstracji, wyszukiwanie „podgrzebieniowy” pozostawia 1 wynik, zmiana projekcji, izolowanie obiektu — bez błędów JavaScript.
- ZIP: kontrola integralności `testzip()` = None.
- Podgląd aplikacji w Chromium wyrenderowany przy użyciu osadzonych danych wybranych obrazów.

## Niepotwierdzone / ograniczenia

- Weryfikacja anatomiczna 96 rycin i 111 orientacyjnych oznaczeń nadal nie jest zakończona.
- Moduł 3D wciąż korzysta z 7 uproszczonych siatek, a nie z referencyjnego, zarejestrowanego modelu kończyny górnej.
- WebGL2/GPU oraz obsługa plików GLB z Draco/skinningiem nie zostały przetestowane ani zaimplementowane w pełnym zakresie.
- Kompletny duży samodzielny HTML nie przeszedł pełnej automatycznej sesji przeglądarkowej; sprawdzono kompletność osadzonych obrazów, kodu i laboratorium.
- Przegląd źródeł publicznych repozytoriów objął funkcje, opisy architektury, część list plików; bezpośrednie pobieranie pełnych plików kodu z GitHub nie było dostępne. Kod naszego produktu jest opracowaniem własnym.

## Pliki testowe (nie dołączono do ZIP)

`test434_results.json`, `test434_extended_results.json`, `test434_3d_results.json` w katalogu sesji przygotowania.
