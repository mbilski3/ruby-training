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
- Jak zrobić sobie MVC w Sinatra? |

---

## Dowiecie się c.d:

- Routing w Sinatra |
- BaseController - Co powinno się w nim znaleźć? |
- Layouty, HAML i helpery |
- Przekazywanie zmiennych do widoków |
- Formularze i CSRF |
- Debugowanie |

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

@[54-65](Konfiguracja)
@[1-10](Niezbędne biblioteki programisty)
@[11-14](RVM)
@[16-17](--no-ri --no-rdoc)
@[19-29](Instalacja ruby i ustawianie gemseta)
@[31-38](Gemy)
@[45-51](Bundle install i stop - start servera thin)

---?image=assets/image/dirs.jpg&size=contain

---

#### Aplikacje Rack-based

https://rack.github.io/

- Rack jest interfejsem między webserverem a kodem ruby |
- config.ru |
- rackup - domyślnie używa webrick-a (my zastąpimy thin) |

---

#### Bundler i Gemfile

- touch Gemfile |
- gem install bundler |
- bundle install |

---

#### Gemfile, rubygems, groups

- source rubygems |
- gem 'sinatra' |
- można zainstalować konkretną wersję, jak w package.json |
- tak samo w package.json groups, np: development |

---?code=https://raw.githubusercontent.com/mbilski3/ruby-training-template/master/Gemfile&lang=ruby&title=Gemfile

@[1](source)
@[3-7](gemy używane zawsze)
@[9-16](gemy tylko development)

---?code=https://raw.githubusercontent.com/mbilski3/ruby-training-template/master/app.rb&lang=ruby&title=app.rb

@[1-3](bundler)

---?code=src/sinatra.rb&lang=ruby&title=sinatra.rb

---

#### MVC - krótkie omówienie

- Małe aplikacje - jeden plik, DSL, bez otwierania klas. Jest to po prostu użycie metod (get, post, delete) z "głównego" obieku ruby |
- Duże aplikacje - proponuję stosować MVC i mechanizmy obiektowości, by mieć izolację od poszczególnych elementów aplikacji (konfig, requiry, kod, routesy) |
- W tym celu katalogi MVC + helpers |

---?code=https://raw.githubusercontent.com/mbilski3/ruby-training-template/master/app.rb&lang=ruby&title=app.rb

@[5-10](require)

---?image=assets/image/routes.jpg&size=contain

---?image=assets/image/routes1.jpg&size=contain

---?image=assets/image/routes2.jpg&size=contain

---?code=https://raw.githubusercontent.com/mbilski3/ruby-training-template/master/lib/controllers/base_controller.rb&lang=ruby&title=base_controller.rb

@[2-7](development)
@[9-33](overall)
@[35](helpers)

---

#### HAML i layouts

- gem 'haml' |
- haml :index |
- default layout: views/layout.haml |
- set :haml, layout: 'layouts/layout'.to_sym |

---?code=https://raw.githubusercontent.com/mbilski3/ruby-training-template/master/lib/controllers/main_controller.rb&lang=ruby&title=main_controller.rb

@[4-7](render haml)
@[2](set layout)

---

#### HAML

- wcięcia |
- brak domknięć |
- element: %div |
- klasa: .class |
- id: #id |
- domyślny element: div, np: .class#id |

---

#### HAML

- atrybut: %html(xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en") |
- ruby: %a(title=@title href=href) Stuff |
- inne ruby (preferowane): %a{title: @title, href: href} Stuff |
- zmienne z @ działają bez ich przekazywania (binding) |
- przekazywanie zmiennych bez @: haml :index, locals: {x: 5} |
- i wtedy używanie bez @ |

---

#### HAML

- wypisanie zmiennej: = @title |
- NALEŻY używać helperów |
- partial: = haml :partial |
- operacje ruby bez wypisywania: - x = 5 |
---

---?code=https://raw.githubusercontent.com/mbilski3/ruby-training-template/master/lib/views/index.haml&lang=haml&title=index.haml

@[9-12](form haml)

---


### Pytania?

<br>

@fa[github gp-contact](mbilski3)

@fa[envelope gp-contact](mbilski3@gmail.com)
