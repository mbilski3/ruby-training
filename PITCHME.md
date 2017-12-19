## Ruby training

#### Ruby and Sinatra for Frontend Peeps

---

## Ready for this? Thus...

![](https://ljdchost.com/OpJjQlm.gif "Ready for this? Thus...")

---

## Dowiecie się:

- Jak poprawnie zainstalować i skonfigurować środowisko programisty? |
- Rvm, gemsets, przełączanie między wersjami |
- Vagrant - Szybki provisioning i pierwsza appka |
- Aplikacje rack-based, jak je traktować? |
- Bundler i Gemfile, co to są? |

---

## Dowiecie się c.d:

- Jak zrobić sobie MVC w Sinatra? |
- Routing w Sinatra |
- BaseController - Co powinno się w nim znaleźć? |
- Layouty, HAML i helpery |
- Przekazywanie zmiennych do widoków |
- Params - query strings, body, jak je ugryźć? |

---

#### Mamy goły obraz Ubuntu

RVM - Ruby Version Manager, narzędzie linii komend do zarządzania wersjami Ruby i Gemów.

#### Po co? Przecież mamy apt-get!

- W repozytoriach apt-get jest oczywiście ruby, natomiast wersje nie są już uaktualniane na bieżąco |
- Co jeśli mamy projekt X który wymaga Ruby 1.9.3 i projekt Y który wymaga 2.4? |
- Projekt X potrzebuje gema Rails w wersji 3, projekt Y potrzebuje go w wersji 5? |

---

#### RVM

https://rvm.io/

Dodajemy klucze
```bash
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
```

Pobieramy i uruchamiamy skrypt instalacyjny
```bash
\curl -sSL https://get.rvm.io | bash -s stable
```

Instalujemy wybraną wersję
```bash
rvm install 2.4.0
```

---

#### RVM - gemsets automat

Gemsets to wydzielone przestrzenie do instalacji gemów. W zależności od tego, nad jakim projektem aktualnie pracujemy, ustawiamy wersję Ruby i przestrzeń z której będziemy używać Gemów.

.ruby-gemset
```bash
ruby-training
```

.ruby-version
```bash
2.4.0
```

---

#### Spróbujmy Vagranta

- https://www.vagrantup.com/downloads.html |
- https://www.virtualbox.org/wiki/Downloads |
- https://github.com/mbilski3/ruby-training-template |

---?code=https://raw.githubusercontent.com/mbilski3/ruby-training-template/master/Vagrantfile&lang=ruby&title=Vagrantfile

@[51-62](Konfiguracja)
@[1-10](Niezbędne biblioteki programisty)
@[11-14](RVM)
@[16-17](--no-ri --no-rdoc)
@[19-29](Instalacja ruby i ustawianie gemseta)
@[31-38](Gemy)
@[42-48](Bundle install i stop - start servera thin)

---?image=assets/image/dirs.jpg&size=20%

Struktura projektu (może się różnić)
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

---

### Pytania?

<br>

@fa[github gp-contact](mbilski3)

@fa[envelope gp-contact](mbilski3@gmail.com)
