# Raport testów Anatomia z Graya 4.21

## Wykonane testy przeglądarkowe
- Otwieranie atlasu i ładowanie głównej ryciny — **OK** (1086 px, obraz barku i pachy).
- Wybór `axillary_artery` z listy — **OK**, panel pokazuje tętnicę pachową.
- Przyciski lokalnej oceny oznaczeń — **OK**; status `wymaga-korekty` zapisany w stanie aplikacji.
- Zakładka Audyt — **OK**; zgłoszenie widoczne i możliwy powrót do odpowiedniej struktury.
- Quiz i fiszki — **OK**; dostępne odpowiedzi i ekran fiszki.
- Laboratorium 3D bez WebGL2 — **OK**; rysowany rzeczywisty obracany model przez Canvas 2D, 7 siatek.
- Wskazanie siatki z listy — **OK**; szczegóły aktualizowane.
- Import przykładowego GLB — **OK**; 7 siatek, 780 trójkątów.
- Brak błędów JavaScript w powyższych przebiegach.

## Kontrole pakietu
- Archiwum ZIP — test integralności `testzip()`: **OK**.
- Wszystkie 96 obrazów i 96 miniaturek zachowane.
- W samodzielnym HTML moduł 3D osadzony jest bajtowo zgodnie z plikiem `model3d_lab.html`.
- Brak zależności `app.js` i `style.css` od zewnętrznych plików w HTML offline.

## Ograniczenia
- Automatyczny test uruchomienia całego jednoplikiowego HTML (~68 MB) **przekroczył limit czasu**. Nie oznaczamy go jako zaliczony.
- Renderowanie WebGL2 w przeglądarce z GPU nie zostało potwierdzone w tej sesji; zweryfikowano renderer Canvas2D.
- Model 3D pozostaje uproszczonym szkicem technologicznym, nie zweryfikowaną anatomicznie siatką.
- Oznaczenia na rycinach nadal są orientacyjne. Ocena „przejrzano lokalnie” nie oznacza potwierdzenia atlasowego.
