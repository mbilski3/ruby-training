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

---?code=https://raw.githubusercontent.com/mbilski3/ruby-training-template/master/Vagrantfile&lang=ruby&title=Vagrantfile

@[51-62](Konfiguracja)
@[1-10](Niezbędne biblioteki programisty)
@[11-14](RVM)
@[16-17](--no-ri --no-rdoc)
@[19-29](Instalacja ruby i ustawianie gemseta)
@[31-38](Gemy)
@[42-48](Bundle install i stop - start servera thin)

---

@title[JavaScript Block]

<p><span class="slide-title">JavaScript Block</span></p>

```javascript
// Include http module.
var http = require("http");

// Create the server. Function passed as parameter
// is called on every request made.
http.createServer(function (request, response) {
  // Attach listener on end event.  This event is
  // called when client sent, awaiting response.
  request.on("end", function () {
    // Write headers to the response.
    // HTTP 200 status, Content-Type text/plain.
    response.writeHead(200, {
      'Content-Type': 'text/plain'
    });
    // Send data and end response.
    response.end('Hello HTTP!');
  });

// Listen on the 8080 port.
}).listen(8080);
```

@[1,2](You can present code inlined within your slide markdown too.)
@[9-17](Displayed using code-syntax highlighting just like your IDE.)
@[19-20](Again, all of this without ever leaving your slideshow.)

---?gist=onetapbeyond/494e0fecaf0d6a2aa2acadfb8eb9d6e8&lang=scala&title=Scala GIST

@[23](You can even present code found within any GitHub GIST.)
@[41-53](GIST source code is beautifully rendered on any slide.)
@[57-62](And code-presenting works seamlessly for GIST too, both online and offline.)

---

## Template Help

- [Code Presenting](https://github.com/gitpitch/gitpitch/wiki/Code-Presenting)
  + [Repo Source](https://github.com/gitpitch/gitpitch/wiki/Code-Delimiter-Slides), [Static Blocks](https://github.com/gitpitch/gitpitch/wiki/Code-Slides), [GIST](https://github.com/gitpitch/gitpitch/wiki/GIST-Slides)
- [Custom CSS Styling](https://github.com/gitpitch/gitpitch/wiki/Slideshow-Custom-CSS)
- [Slideshow Background Image](https://github.com/gitpitch/gitpitch/wiki/Background-Setting)
- [Slide-specific Background Images](https://github.com/gitpitch/gitpitch/wiki/Image-Slides#background)
- [Custom Logo](https://github.com/gitpitch/gitpitch/wiki/Logo-Setting), [TOC](https://github.com/gitpitch/gitpitch/wiki/Table-of-Contents), and [Footnotes](https://github.com/gitpitch/gitpitch/wiki/Footnote-Setting)

---

### Template Versions

- #### [Base Template  @fa[external-link gp-download]](https://gitpitch.com/gitpitch/templates/netflix)
- #### [Code Maximized @fa[external-link gp-download]](https://gitpitch.com/gitpitch/templates/netflix?p=codemax)
- #### [Speaker Notes @fa[external-link gp-download]](https://gitpitch.com/gitpitch/templates/netflix?p=speaker)

---

### Questions?

<br>

@fa[twitter gp-contact](@gitpitch)

@fa[github gp-contact](gitpitch)

@fa[medium gp-contact](@gitpitch)

---?image=assets/image/gitpitch-audience.jpg

@title[Download this Template!]

### Get your presentation started!
### [Download this template @fa[external-link gp-download]](https://gitpitch.com/template/download/netflix)
