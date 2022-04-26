# Strona Chóralnych Ackeleracji

Strona jest budowana statycznie z użyciem https://jekyllrb.com

Wygenerowane pliki są wrzucane na serwer FTP.

## Środowiska
* Produkcja: http://akceleracje.uw.edu.pl
* Test: http://test.akceleracje.uw.edu.pl

## Uruchamianie lokalnie
Wszystko w katalogu z kodem.

Za pierwszym razem:
1. `sudo apt install ruby ruby-dev build-essential`
2. `gem install bundler`
3. `bundle config build.ffi -- --with-cflags=-Wno-implicit-function-declaration`
4. `bundle install`
5. `bundle exec jekyll serve`

Kolejne razy: `bundle exec jekyll serve`

Strona chodzi pod adresem http://127.0.0.1:4000/

Dopóki `serve` jest uruchomione strona chodzi i jest automatycznie regenerowana przy zmianach w kodzie.

## Generowanie plików do wrzucenia przez FTP
1. `rm -rf _site`
2. `bundle exec jekyll build`

Pliki do skopiowania są w folderze `_site`

## Dodawanie i edytowanie wpisów
Posty znajdują się w katalogu `_posts` i są napisane w Markdown. Ściąga:
https://www.markdownguide.org/cheat-sheet/
