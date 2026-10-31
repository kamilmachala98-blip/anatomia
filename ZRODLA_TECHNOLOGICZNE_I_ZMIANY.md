# Anatomia z Graya 4.20 — źródła technologiczne, zmiany i ograniczenia

## Główne wykorzystane podręczniki / dokumentacje (online)

1. **MDN Learn Web Development**, https://developer.mozilla.org/en-US/docs/Learn_web_development — HTML, CSS, JavaScript, responsywność i semantyka.
2. **MDN JavaScript — Przewodnik (PL)**, https://developer.mozilla.org/pl/docs/Web/JavaScript/Guide — funkcje, obiekty, moduły, JSON i obsługa zdarzeń.
3. **MDN Web Performance: HTML**, https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Performance/HTML — lazy loading, optymalizacja obrazów i kolejności pobierania.
4. **Three.js Manual — Installation**, https://threejs.org/manual/pages/installation.html — podział na moduły, GLTFLoader i OrbitControls. Dokumentacja użyta jako odniesienie architektoniczne, ale aplikacja 4.20 nadal ma własny renderer WebGL2 bez zależności.
5. **Three.js Docs — GLTFLoader / OrbitControls / Raycaster**, https://threejs.org/docs/pages/GLTFLoader, https://threejs.org/docs/pages/OrbitControls, https://threejs.org/docs/pages/Raycaster.html — import glTF, sterowanie kamerą i wybieranie siatek.
6. **Khronos glTF 2.0 Specification**, https://registry.khronos.org/glTF/specs/2.0/glTF-2.0.html — nagłówek GLB, chunki JSON/BIN, bufferViews, accesory i struktura sceny.
7. **Blender Manual — glTF 2.0**, https://docs.blender.org/manual/en/5.1/addons/import_export/scene_gltf2.html; https://docs.blender.org/manual/en/latest/ — aktualny podręcznik Blendera 5.2 LTS i opis eksportu — eksport modelu, materiałów i nazwanych siatek.
8. **Blender Manual Translations**, https://projects.blender.org/blender/blender-manual — dostępne wersje m.in. polska, niemiecka, francuska, hiszpańska, włoska i japońska. W przypadku różnic technicznych nadrzędna jest aktualna wersja oryginalna.
9. **Z-Anatomy**, https://github.com/Z-Anatomy/Models-of-human-anatomy — potencjalne źródło licencjonowanych siatek do przyszłego importu; warunki i pochodzenie konkretnego pliku należy zweryfikować przed wdrożeniem.

## Przemyślane usprawnienia (już w tej wersji)

- 96 lekkich miniatur WebP (248×176) z pełnego zbioru obrazów. Galeria i menu ładują miniatury, pełne obrazy są używane w centralnej planszy.
- Jednolita funkcja `thumbnailURL()` oddziela zasoby podglądowe od źródłowych.
- W folderowym atlasie obowiązuje leniwe pobieranie ilustracji w galerii; w wersji samodzielnej wszystkie zasoby pozostają osadzone, więc HTML jest większy.
- Laboratorium 3D importuje **nieskompresowane GLB 2.0** z lokalnego dysku, rozpakowuje GLB JSON/BIN, odczytuje accesory, zagnieżdżone transformacje sceny, nazwy i kolory, a następnie tworzy oddzielnie wybieralne siatki. Ograniczenia: bez Draco/Meshopt, skinningu, tekstur PBR, morph target, rzadkich accessorów. To demonstrator technologii, NIE anatomia referencyjna.
- Nazwy siatek zachowywane są w UI. Modele po imporcie nie stają się automatycznie zweryfikowane medycznie.
- Ulepszenia dostępności: focus widoczny podczas obsługi klawiaturą, preferencja ograniczenia animacji, responsywne miniatury.

## Weryfikacja merytoryczna

- Ryciny wygenerowane komputerowo wciąż wymagają indywidualnego porównania z Grayem, Sobotą i Rohenem–Yokochim. Miniatury są pochodnymi tych samych obrazów, bez zmiany ich anatomii.
- Wcześniejsze orientacyjne kalibracje pozostają orientacyjne. Ten etap **nie podnosi ich statusu do zweryfikowanych**.
- Import glTF / GLB nie zastępuje geometrii segmentowanej z CT/MR lub atlasu o potwierdzonym pochodzeniu.

## Jak przetestować GLB

1. Otwórz zakładkę „3D — laboratorium”.
2. Wczytaj `prototyp_3d_419.glb` przez przycisk wyboru pliku.
3. Model powinien zawierać oddzielne nazwane obiekty; przetestuj obrót, ukrywanie grup i zaznaczenie myszą.
4. Wczytaj model glTF/GLB wyeksportowany z Blendera z siatkami i bez kompresji Draco; jeśli model wymaga rozszerzenia, moduł pokaże komunikat.
5. Nie używaj demonstracyjnej geometrii do nauki relacji przestrzennych prawdziwych mięśni.
