# Tuner chromatyczny — PWA na iPhone'a

## Co jest w paczce
- `index.html` — tuner z wykrywaniem wysokości dźwięku i wskaźnikiem centów
- `manifest.webmanifest` — ustawienia PWA i ikony
- `sw.js` — cache/offline dla plików aplikacji
- `icons/icon-192.png`, `icons/icon-512.png` — ikony aplikacji

## Ważne
Aby mikrofon działał na iPhonie, aplikacja musi być otwarta pod adresem HTTPS. Samo otwarcie pliku HTML z aplikacji Pliki nie wystarczy. PWA nie jest aplikacją natywną z App Store, ale można dodać ją do ekranu początkowego.

## Najprostsze uruchomienie: hosting statyczny HTTPS
1. Rozpakuj ZIP na komputerze.
2. Umieść zawartość folderu `tuner-pwa` na statycznym hostingu obsługującym HTTPS (np. GitHub Pages lub Netlify).
   - Netlify: zaloguj się na Netlify w przeglądarce na komputerze i przeciągnij folder projektu do obszaru ręcznego wdrażania, jeśli ta opcja jest dostępna na Twoim koncie.
   - GitHub Pages: utwórz repozytorium, wgraj pliki z folderu (nie sam folder nadrzędny), a następnie w Settings → Pages włącz publikację z gałęzi `main` i katalogu `/ (root)`.
3. Otwórz otrzymany adres `https://...` na iPhonie w Safari.
4. Stuknij przycisk udostępniania (kwadrat ze strzałką w górę).
5. Wybierz „Dodaj do ekranu początkowego”. Jeśli pojawi się opcja „Otwórz jako aplikację internetową”, włącz ją.
6. Stuknij „Dodaj”. Uruchamiaj tuner z nowej ikony „Tuner”.
7. W aplikacji stuknij „Włącz mikrofon” i zezwól na dostęp.

## Używanie
- Zagraj jedną strunę naraz i przytrzymaj dźwięk.
- Jeśli wskaźnik jest po lewej stronie środka, dźwięk jest za niski; po prawej — za wysoki.
- Środek i zielony komunikat oznaczają, że dźwięk jest w przybliżeniu nastrojony.
- Standardowy strój gitary od najgrubszej struny: E2, A2, D3, G3, B3, E4.

## Jeśli mikrofon nie działa
- Otwórz stronę w Safari, nie w przeglądarce osadzonej w innej aplikacji.
- Sprawdź, czy adres zaczyna się od `https://`.
- Sprawdź Ustawienia iPhone'a → Safari → Mikrofon (nazwa opcji może zależeć od wersji iOS).
- Zamknij i otwórz aplikację ponownie, a następnie zaakceptuj prośbę o mikrofon.
- Dla dokładniejszego strojenia ogranicz hałas i zagraj tylko jedną strunę.

## Prywatność
Dźwięk jest analizowany lokalnie przez przeglądarkę. Kod nie wysyła nagrania na serwer ani nie zapisuje go.
