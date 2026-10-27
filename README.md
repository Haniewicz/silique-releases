# Silique — instalatory i aktualizacje

Oficjalne paczki Silique dla macOS, Androida, Windows i Linux GTK4: **[pobierz najnowsze wydanie](https://github.com/Haniewicz/silique-releases/releases/latest)**.

To repozytorium zawiera instalatory oraz podpisane informacje o aktualizacjach. Kod aplikacji i serwera jest utrzymywany osobno w prywatnych repozytoriach.

- macOS 12 lub nowszy, Apple Silicon i Intel: od 0.2.30 pobierz DMG, otwórz go i przeciągnij Silique.app do skrótu Applications (Programy), zastępując poprzednią instalację. Następnie wysuń obraz dysku i uruchom aplikację z Programów. Obecne paczki mają podpis lokalny, bez notaryzacji Apple; przy pierwszym uruchomieniu może być konieczna zgoda w Ustawieniach systemowych → Prywatność i ochrona → Otwórz mimo to. Sam format DMG nie usuwa tej kontroli.
- Android 7 lub nowszy: pobierz APK i zainstaluj jako aktualizację dotychczasowej aplikacji.
- Windows x64: instalator EXE dla bieżącego użytkownika albo ZIP przenośny. ZIP trzeba rozpakować w całości i uruchomić silique.exe. EXE nie ma podpisu Authenticode.
- Linux x64 na GTK4: DEB dla Ubuntu 24.04+, RPM sprawdzony na Fedorze 44 oraz archiwum tar.gz. Wymagane GTK4 >= 4.14, glibc >= 2.39 i działający Secret Service, np. GNOME Keyring. Wsparcie GTK4 korzysta z niestandardowego silnika Fluttera i jest eksperymentalne. RPM nie ma podpisu OpenPGP.
- `SHA256SUMS.txt` w wydaniu pozwala sprawdzić zgodność pobranych plików.

Podpisane kanały aktualizacji: `latest.json` (aplikacja) i `appcast.xml` (macOS). Pierwsza wersja z updaterem to 0.2.5; przy przejściu z wcześniejszych wersji trzeba zainstalować ją ręcznie. macOS i Android sprawdzają nowe wersje automatycznie, a użytkownik potwierdza instalację. Od 0.2.7 instalacje Linux zarządzane przez RPM/DEB również sprawdzają aktualizacje i pozwalają na instalację z aplikacji po systemowej autoryzacji (polkit/pkexec). Przejście z Linux 0.2.6 do 0.2.7 wymaga ręcznej instalacji DEB/RPM. Windows i Linux z archiwum tar.gz aktualizuje się ręcznie przez stronę wydań. Pobieranie nie wymaga konta GitHub.

## Przejście macOS z ZIP na DMG

Wersja 0.2.30 i wszystkie kolejne wydania macOS są dostępne wyłącznie jako DMG. Ten sam podpisany obraz służy do ręcznej instalacji i aktualizacji Sparkle.

**macOS 0.2.29 lub starszy wymaga jednorazowej ręcznej instalacji z DMG.** Stary aktualizator rozpoznaje wyłącznie paczki ZIP. Zamknij aplikację, zastąp ją w Programach i zachowaj dotychczasowe dane oraz poświadczenia. Nie usuwaj folderów notatek ani wpisów pęku kluczy. Od 0.2.30 aktualizacja z aplikacji korzysta już z DMG. Zmiana nie wymaga ręcznej migracji starszych instalacji Androida i Linuksa.

## Prywatność

Nie umieszczamy tutaj notatek, vaultów, danych kont, kluczy ani kodu źródłowego Silique. Przed aktualizacją zamknij poprzednią wersję aplikacji. Aktualizacja zachowuje dane i klucze istniejącej instalacji.
