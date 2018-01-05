# CV-Flask

This project is to create a *static* website in which I can showcase my CV. I use Flask as minimalistic framework that allows to write very concisely web apps and plays nicely with a bunch libraries. Flask-Flatpages is one such library that allows to write content in Markdown and have it automatically converted to the equivalent html. Finally, Frozen-Flask can be used to "build" static Flask applications, turning everything into a collection of static html/css files that can be put on a web server (Tomcat, python) without needing additional technologies. 

The structure of the project makes a distinction between **templates**, which encode the **structure** of webpages in HTML + Jinja2 (a templating language), and the **pages**, which contain the **content** of webpages written in Markdown language. Templates are filled with the content of pages, hence there should always be more pages than templates.

## IDEA

Here's a table of key-values relevant to this project:

| Key           | Value         |
| ------------- |:-------------:|
|  inspiration  | [Static Website w. Flask](https://nicolas.perriault.net/code/2012/dead-easy-yet-powerful-static-website-generator-with-flask/) |
| technology    | Flask           |
| technology    | Frozen-Flask    |
| technology    | Flask-Flatpages |
| useful | [markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)  |
| useful | [interactive markdown](http://dillinger.io/) |
| inspiration CSS | [bootstrap](https://blackrockdigital.github.io/startbootstrap-freelancer/) |
| inspiration CSS | [Twilio](https://www.twilio.com/) |
| free CSS templates | [Templated](https://templated.co/) |
| free CSS templates | [html5up](https://html5up.net/) |
| background Flask | [Explore Flask](https://exploreflask.com/en/latest/) |
| web assets mgmt | [Flask-Assets](http://flask-assets.readthedocs.io/en/latest/) |
| web assets mgmt | [Flash-Webpack](https://github.com/nickjj/flask-webpack) |
| CSS management | [Explore Flask: Static files](http://exploreflask.com/en/latest/static.html) |
| Colour palettes | [Color-hex Palettes](http://www.color-hex.com/color-palettes/) |
| inspiration look | [Nicolas Perriault](https://nicolas.perriault.net/code/) |
| inspiration look | [Charles Leifer](http://charlesleifer.com/blog/how-to-make-a-flask-blog-in-one-hour-or-less/) |
| inspiration look | [NPR, though not blog](npr.org) |
| inspiration look | [Flask blog](https://pythonhosted.org/Flask-Mail/) |

## TODOs
* List of requirements
* Make design for website
* Future:
    * Containerisation (Kubernetes/Docker)
	* Use CSS library
    * Compile CSS beforehand with e.g. LESS 
    * Deploy on Raspberry Pi or host
	* Blogging page to write about discoveries?

## DONE
* Read *Explore Flask* (70 pages)

## DESIGN
* Landing page
	* Title bar
		* Title (left)
		* Other pages (right) 
* About me
	* Name
	* Location 
		* Inserted Open Street Maps pin Leuven
	* Education
* Career
* Side-projects
	* Ruimte-jager (needs clean-up)
	* Connect4
* Contact
* (Future: blog?)

## SOME NICE CSS TEMPLATES
* [All-in, really beautiful](https://pixelarity.com/items/demos/dimension/dark/index.html#)
* [Single page, scroll down](http://www.free-css.com/free-css-templates/page217/jwood-photography)
* [See bottom, contact](https://templated.co/interphase)

## REQUIRED
* Python 3
* pipenv + dependencies

## USEFUL BASH COMMANDS
Install pipenv for local user:
```sh
$ pip3 install --user pipenv
```

If pipenv not working, then ~/.local/bin needs to the PATH. Do this permanently by adding the following to ~/.profile:
```sh
export PATH=$PATH:~/.local/bin
``` 

Build environment:

```sh
$ pipenv install
```

Start virtual environment:

```sh
$ pipenv shell
```

Test if in virtual environment:

```sh
$ which python
```

Start Flask server:

```sh
$ python3 sitebuilder.py run
```

Alternatively, run Flask server within virtual environment:

```sh
$ pipenv run python3 sitebuilder.py run
```

Build project (=create static html/css files):

```sh
$ python3 sitebuilder.py build
```

Run static project:

```sh
$ python3 -m http.server
```

*Extra*: Read Python documents on *localhost:4040*:

```sh
$ pydoc3 -p 4040
```
