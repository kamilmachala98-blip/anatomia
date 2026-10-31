# Raport testów – Anatomia z Graya 4.54

## Testowane scenariusze przeglądarkowe (Chromium)

- Uruchomienie atlasu oraz otwarcie głównej ryciny: OK.
- Wejście w zakładkę „Priorytety”: 104 wpisów, wyszukiwanie działa.
- Wybór punktu i powrót do przypisanej ryciny: OK (wybrano `axillary_artery`).
- Wyświetlenie etykiety na obrazie: OK (liczba etykiet: 1).
- Zgłoszenie punktu do korekty: OK.
- Quiz terminologiczny: 4 odpowiedzi do wyboru, bez błędu JS.
- Fiszki: 1 aktywna karta, bez błędu JS.
- Zakładka 3D i osobny renderer Canvas 2D: OK; 20 siatek.
- Wybór obiektu 3D i metryka: OK.
- Import lokalnego modelu GLB: regionalny_model_3d_444.glb · 2106 trójkątów; renderer CPU wyświetla próbkę przy dużych modelach..
- Eksport priorytetów do CSV: gray454_priorytety.csv.
- Eksport manifestu siatek do JSON: gray454_siatki.json.
- 96 wpisów audytu rycin: OK.
- Błędy JavaScript wykryte w tych testach: **0**.

## Kontrola danych

- Pliki graficzne i SHA-256: **96/96**.
- Aktywne punkty: **104**; 7 starszych wpisów pozostało w archiwum wcześniejszej wersji.
- Kandydaci podobieństwa perceptualnego dHash: **50 par**. Nie usuwano duplikatów na tej podstawie.
- Priorytety punktów: {"wysoki": 2, "średni": 5, "standardowy": 97}. Te wartości NIE oznaczają potwierdzonego błędu w anatomii.
- Domyślna scena 3D: 20 siatek; 1053 trójkąty w danych źródłowych sceny. Osobny plik GLB 4.44 zawiera 2106 trójkątów według jego akcesoriów.

## Co nie zostało potwierdzone

- **0/96 rycin** ma certyfikowaną weryfikację anatomiczną.
- Żadne historyczne oznaczenie nie zostało automatycznie uznane za idealnie trafione.
- Siatki 3D są ilustracyjne; nie zastępują prawdziwych modeli z BodyParts3D, Z-Anatomy ani segmentacji CT/MR.
- Przenikanie warstw pozostaje efektem przezroczystości istniejących siatek, nie rzeczywistą rekonstrukcją głębokości tkanek.
- Nie przeprowadzono pełnego testu przeglądarkowego 68 MB jednoplikiowego HTML na wszystkich systemach; jego zgodność osadzonych plików została sprawdzona statycznie.

## Źródła referencyjne i licencje

Por. `ZRODLA_I_ZASTRZEZENIA_4_54.md` i wcześniejsze dokumenty audytu.
