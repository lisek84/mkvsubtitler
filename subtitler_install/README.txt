
Ten skrypt ma za zadanie wmuxowac napisy w z pliku srt w utf8 do plikow mkv.
Najprosciej go zainstalowac uruchamiajac plik install_synology z uprawnieniami administratorskimi.

czyli np. ./install_synology jako root
lub sudo ./install_synology jako inny user.

Jesli cos sie wysypie warto sprobowac przez sh install_synology.

Jesli instalator nie ruszy...

Przydalo by sie zainstalowac troche niezbednych elementow.

Instalujemy poprzez ipkg install nazwa_paczki

To czego potrzebuje skrypt oraz skrypt do napiprojektu:

bash
iconv
md5sum
mplayer (powinien byc wraz z Audiostation)
gawk  (potrzebne jest polecenie awk)
mkvtoolnix

Wtedy najprosciej skopiowac pliki do katalogu w ktorym system bedzie je w stanie wykonac:

cp mkv_subtitler* *.sh /usr/bin/

Teraz mozna /usr/bin/mkv_subtitler_crontab dodac do uruchamiania w harmonogramie zadan w panelu sterowania albo dopisac do /etc/crontab


Instalator sam sprawdza czy ma odpowiednie narzedzia, ale nie koniecznie zadziala u kazdego, bo opiera sie na roznych narzedziach ktore nie u kazdego musza sie znajdowac.
Sam skrypt jednak powinien dzialac smialo na kazdym synology.
Niewykluczone, ze dla konkretnych modeli dyskow synology, nie uda sie zdobyc wszystkich niezbednych paczek np. mkvtoolnix - nic na to nie poradze ;)

Bardzo bym chcial moc przetestowac wszystko na kazdym modelu synology, ale do dyspozycji mam tylko ds212j ;)
W dodatku z bardzo wieloma dodatkowymi narzedziami pod linuxa ;)




Nie jest wykluczone, ze skrypty bedzie trzeba dostosowac do konkretnego srodowiska recznie. Sa bardzo proste i mozna je dowolnie modyfikowac.

Jesli korzystasz z innych skryptow do pobierania napisow - ten skrypt nie powinien sięz nimi gryzc - bo zabierze napisy z katalogu z filmem i wstawi je do pliku - a inny skrypt bedzie znowu szukal napisow dla nowo
powstalego pliku. Nie powinno to powodowac problemow.

W razie problemow z instalacja - przeanalizuj skryp install_synology - na pewno sie rozjasni wszystko.

Wszelkie zmienne konfiguracyjne znajdziesz w pliku mkv_subtitler_crontab.

W przypadku pytan mozna sie ze mna kontaktowac tutaj przez forum pronas.pl - http://pronas.pl/member2504.html




