# kate-wakatime

Wtyczka do edytora Kate integrująca z usługą WakaTime.

## Uwaga

Ta wersja jest przeznaczona dla Kate 6 (KTextEditor z KF 6).

Jeśli potrzebujesz wersji dla Kate 5, użyj [wydania v1.3.10](https://github.com/Tatsh/kate-wakatime/releases).

Jeśli potrzebujesz wersji dla Kate 4, użyj [wydania v0.6](https://github.com/Tatsh/kate-wakatime/releases).

## Zależności

- [CMake](https://cmake.org/) (3.31+)
- [Extra CMake Modules](https://invent.kde.org/frameworks/extra-cmake-modules)
- [KF6:TextEditor](https://develop.kde.org/products/frameworks/)
- [KF6:I18n](https://develop.kde.org/products/frameworks/)
- [wakatime-cli](https://github.com/wakatime/wakatime-cli)

Sposób instalacji tych pakietów zależy od Twojej dystrybucji. Zazwyczaj należy zainstalować edytor Kate, CMake oraz pakiety deweloperskie KDE Frameworks i Qt.

## Lokalizacja

Ta wtyczka obsługuje wiele języków:
- Angielski (domyślny)
- Polski

Jeśli chcesz pomóc w tłumaczeniu, zajrzyj do katalogu `po/`.

## Instrukcja obsługi

`wakatime-cli` lub `wakatime` musi znajdować się w `PATH` lub w katalogu `~/.wakatime`.

1. Załóż konto w serwisie [WakaTime](https://wakatime.com).
2. Pobierz swój [klucz API](https://wakatime.com/settings).
3. Skonfiguruj i skompiluj projekt:

   ```bash
   git clone git@github.com:Tatsh/kate-wakatime.git
   cd kate-wakatime
   cmake -S . -B build -G Ninja -DCMAKE_INSTALL_PREFIX=/usr
   cmake --build build
   sudo cmake --install build
   ```

4. Po zainstalowaniu wtyczki otwórz Kate i wejdź w *Ustawienia*, *Konfiguracja: Kate...*, a następnie wybierz *Wtyczki*.
5. Zaznacz pole *WakaTime* i kliknij *OK*.
6. Zrestartuj Kate, aby upewnić się, że wtyczka zainicjowała się poprawnie.
7. Wejdź w *Ustawienia*, *Konfiguracja: WakaTime...*. W oknie dialogowym wpisz swój klucz API i kliknij *OK*, aby zapisać.

Aby mieć pewność, że wszystko działa, sprawdź plik `~/.wakatime.cfg`.
