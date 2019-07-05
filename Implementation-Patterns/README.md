This presentation uses [reveal-md](https://github.com/webpro/reveal-md). 

First install Node, e.g. with [nvm](https://github.com/nvm-sh/nvm). 
Then `nvm install node`. Then `npm install -g reveal-md`.

To view the presentation run `reveal-md Java-Forum-Stuttgart-2019.md -w --css style.css`. 

To convert to PDF for printing use 
```
reveal-md Java-Forum-Stuttgart-2019.md -w --css style.css --print Frank-Gerhardt-Implementation-Patterns-Java-Forum-Stuttgart-2019.pdf --puppeteer-chromium-executable="/usr/bin/chromium"
```
Adapt the browser as necessary.

The HTML version looks as intended and the PDF export has some glitches.

If anything goes wrong, prefix the command line with `DEBUG=reveal-md`.
