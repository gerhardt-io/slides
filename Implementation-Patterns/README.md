# Abstract

Implementation Patterns ist ein leider in Vergessenheit
geratenes Buch von Kent Beck aus dem Jahr 2007. Diese Patterns,
auch Idiome genannt, sind unterhalb von Design Patterns aber
oberhalb von Code-Formatierungsregeln angesiedelt. Bei den
Implementation Patterns geht es darum wie man einzelne Klassen und
Methoden gestaltet. In Code Reviews bin ich immer wieder auf Fälle
gestoßen, bei denen schlechter Code auf Unkenntnis der
Implemenation Patterns zurück geführt werden kann. Anfänger und
Fortgeschrittene können die Qualität ihres Codes wesentlich
verbessern, wenn sie die Implementation Pattern kennen und
anwenden.

## HTML

This presentation uses [reveal-md](https://github.com/webpro/reveal-md). 

First install Node, e.g. with [nvm](https://github.com/nvm-sh/nvm). 
Then `nvm install node`. Then `npm install -g reveal-md`.

To view the presentation run `reveal-md Java-Forum-Stuttgart-2019.md -w --css style.css`. 

## PDF

To convert to PDF for printing use 
```
reveal-md Java-Forum-Stuttgart-2019.md -w --css style.css --print Frank-Gerhardt-Implementation-Patterns-Java-Forum-Stuttgart-2019.pdf --puppeteer-chromium-executable="/usr/bin/chromium"
```
Adapt the browser as necessary.

The HTML version looks as intended and the PDF export has some glitches.

If anything goes wrong, prefix the command line with `DEBUG=reveal-md`.
