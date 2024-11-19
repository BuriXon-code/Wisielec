# Gra Wisielec! 🇵🇱
![Gra](/gra3.png)

## O grze...

### Jest to klasyczna znana gra w Wisielca, polegająca na odgadywaniu ukrytego słowa.

Do wyboru jest kilka "poziomów", lub raczej kategorii odgadywanych haseł.

Gra może operować na konretnej grupie słów lub na puli ponad 1.5mln słów w kategorii 'mix'.

Możliwe jest także wybranie własnego pliku ze słowami.

### Gra jest w 100% skryptem shell'owym.

Gra nie zawiera żadnych poleceń poza funkcjami bash oraz wbudowanymi komendami coreutils.

> [!WARNING]
> - Gra nie będzie działała prawidłowo na systemach z busybox (wymagane coreutils)!
> - Instalator gry potrzebuje skonfigurowanego pakietu 'wget' oraz 'tar'! 

## Instalacja i uruchomienie ...

Posiadać zainstalowany bash, coreutils, tar, wget.

### Instalator

Dla ułatwienia instalacji napisałem skrypt instalatora wraz z instrukcjami po instalacji i w przypadku niepowodzenia.

![Gra](/gra1.png)

### Pobieranie i instalacja :

```
git clone https://github.com/BuriXon-code/Wisielec
cd Wisielec
chmod +x *
./install.sh
```
### Uruchamianie :
```
./wisielec
```

### Przed pierwszym uruchomieniem :
![Gra](/gra2.png)

Przed pierwszym uruchomieniem zalecane jest użycie flagi -h lub --help, aby zapoznać się z instrukcją dotyczącą gry.
```
./wisielec --help
```
lub 
```
./wisielec -h
```

> [!WARNING]
> - Przed pierwszym uruchomieniem porównaj sumy MD5 instalowanego pliku i MD5 z pliku w repozytoium!

### Instalacja ręczna

Aby zainstalować grę ręcznie w przypadku niepowodzenia instalacji automatycznej, należy wykonać następujące kroki:

```
# Pobieranie plików z github
git clone https://github.com/BuriXon-code/Wisielec
cd Wisielec
chmod +x wisielec*
```
```
# Tworzenie katalogu dla plików z pierwiastkami:
# W miejcu '/path/to/directory/' należy wpisać wybraną przez siebie ścieżkę, w której znajdą się pliki ze słowami
mkdir /path/to/directory/ && cd /path/to/directory/
```
```
# Pobieranie plików ze słowami:
wget https://burixon.com.pl/pliki/slowa.tar.xz
```
```
# Rozpakowywanie pierwiastków:
tar xvf slowa.tar.xz
```
```
# Eksportowanie wybranej ścieżki
# W miejcu '/path/to/.shellrc' należy wpisać ścieżkę do pliku konfiguracyjnego shella
echo "export WISIELEC=\"/path/to/directory/\"" >> /path/to/.shellrc
```
```
# Stosowanie zmian w pliku konfiguracyjnym:
source /path/to/.shellrc
```

Gotowe :) Gra została zainstalowana. Teraz można ją uruchomić:

```
./wisielec
```


## Uwagi!
### Przytrzymanie CTRL+C :
Przytrzymanie przycisków CTRL+C może wpłynąć źle na działanie skryptu i zatrzymać go przed ukończeniem gry.

### Kompatybilność :
Skrypt kompatybilny jest z wszystkimi systemami Linux oraz Termux.

Co jednak ważne - przez wzgląd na użycie kolorów RGB (ANSI escape \e[38;2...) gra nie będzie dopasowywać się do schematów kolorów używanego emulatora terminala.

Zalecane uruchamianie w terminalu z ciemnym motywem.

![Gra](/gra4.png)

