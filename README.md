# api documentation for  [cli-spinner (v0.2.6)](https://github.com/helloIAmPau/node-spinner#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-cli-spinner.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-cli-spinner) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-cli-spinner.svg)](https://travis-ci.org/npmdoc/node-npmdoc-cli-spinner)
#### A simple spinner

[![NPM](https://nodei.co/npm/cli-spinner.png?downloads=true)](https://www.npmjs.com/package/cli-spinner)

[![apidoc](https://npmdoc.github.io/node-npmdoc-cli-spinner/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-cli-spinner_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-cli-spinner/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-cli-spinner/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-cli-spinner/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Pasquale Boemio",
        "email": "boemianrapsodi@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/helloIAmPau/node-spinner/issues"
    },
    "contributors": [
        {
            "name": "Bryce Kahle"
        },
        {
            "name": "Brian Hirt"
        },
        {
            "name": "Nathan Bleigh"
        },
        {
            "name": "Kendrick Taylor"
        }
    ],
    "dependencies": {},
    "description": "A simple spinner",
    "devDependencies": {},
    "directories": {},
    "dist": {
        "shasum": "8a59703324e93a908f6e601e4e74f5b85b371e5c",
        "tarball": "https://registry.npmjs.org/cli-spinner/-/cli-spinner-0.2.6.tgz"
    },
    "engines": {
        "node": ">=0.10"
    },
    "gitHead": "96105f75d8b8bfdd9f5e9d1ba221ea3c1bf2dda8",
    "homepage": "https://github.com/helloIAmPau/node-spinner#readme",
    "keywords": [
        "cli"
    ],
    "license": "MIT",
    "main": "./index.js",
    "maintainers": [
        {
            "name": "helloiampau",
            "email": "boemianrapsodi@gmail.com"
        }
    ],
    "name": "cli-spinner",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/helloIAmPau/node-spinner.git"
    },
    "scripts": {},
    "version": "0.2.6"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module cli-spinner](#apidoc.module.cli-spinner)
1.  [function <span class="apidocSignatureSpan">cli-spinner.</span>Spinner (options)](#apidoc.element.cli-spinner.Spinner)
1.  object <span class="apidocSignatureSpan">cli-spinner.</span>Spinner.prototype

#### [module cli-spinner.Spinner](#apidoc.module.cli-spinner.Spinner)
1.  [function <span class="apidocSignatureSpan">cli-spinner.</span>Spinner (options)](#apidoc.element.cli-spinner.Spinner.Spinner)
1.  [function <span class="apidocSignatureSpan">cli-spinner.Spinner.</span>setDefaultSpinnerDelay (value)](#apidoc.element.cli-spinner.Spinner.setDefaultSpinnerDelay)
1.  [function <span class="apidocSignatureSpan">cli-spinner.Spinner.</span>setDefaultSpinnerString (value)](#apidoc.element.cli-spinner.Spinner.setDefaultSpinnerString)
1.  object <span class="apidocSignatureSpan">cli-spinner.Spinner.</span>spinners

#### [module cli-spinner.Spinner.prototype](#apidoc.module.cli-spinner.Spinner.prototype)
1.  [function <span class="apidocSignatureSpan">cli-spinner.Spinner.prototype.</span>clearLine (stream)](#apidoc.element.cli-spinner.Spinner.prototype.clearLine)
1.  [function <span class="apidocSignatureSpan">cli-spinner.Spinner.prototype.</span>isSpinning ()](#apidoc.element.cli-spinner.Spinner.prototype.isSpinning)
1.  [function <span class="apidocSignatureSpan">cli-spinner.Spinner.prototype.</span>setSpinnerDelay (n)](#apidoc.element.cli-spinner.Spinner.prototype.setSpinnerDelay)
1.  [function <span class="apidocSignatureSpan">cli-spinner.Spinner.prototype.</span>setSpinnerString (str)](#apidoc.element.cli-spinner.Spinner.prototype.setSpinnerString)
1.  [function <span class="apidocSignatureSpan">cli-spinner.Spinner.prototype.</span>setSpinnerTitle (str)](#apidoc.element.cli-spinner.Spinner.prototype.setSpinnerTitle)
1.  [function <span class="apidocSignatureSpan">cli-spinner.Spinner.prototype.</span>start ()](#apidoc.element.cli-spinner.Spinner.prototype.start)
1.  [function <span class="apidocSignatureSpan">cli-spinner.Spinner.prototype.</span>stop (clear)](#apidoc.element.cli-spinner.Spinner.prototype.stop)



# <a name="apidoc.module.cli-spinner"></a>[module cli-spinner](#apidoc.module.cli-spinner)

#### <a name="apidoc.element.cli-spinner.Spinner"></a>[function <span class="apidocSignatureSpan">cli-spinner.</span>Spinner (options)](#apidoc.element.cli-spinner.Spinner)
- description and source-code
```javascript
Spinner = function (options){
  if(!(this instanceof Spinner)) return new Spinner(options)

  if(typeof options === "string"){
    options = { text: options };
  } else if(!options){
    options = {};
  }

  this.text = options.text || '';
  this.setSpinnerString(defaultSpinnerString);
  this.setSpinnerDelay(defaultSpinnerDelay);
  this.onTick = options.onTick || defaultOnTick;
  this.stream = options.stream || process.stdout;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.cli-spinner.Spinner"></a>[module cli-spinner.Spinner](#apidoc.module.cli-spinner.Spinner)

#### <a name="apidoc.element.cli-spinner.Spinner.Spinner"></a>[function <span class="apidocSignatureSpan">cli-spinner.</span>Spinner (options)](#apidoc.element.cli-spinner.Spinner.Spinner)
- description and source-code
```javascript
Spinner = function (options){
  if(!(this instanceof Spinner)) return new Spinner(options)

  if(typeof options === "string"){
    options = { text: options };
  } else if(!options){
    options = {};
  }

  this.text = options.text || '';
  this.setSpinnerString(defaultSpinnerString);
  this.setSpinnerDelay(defaultSpinnerDelay);
  this.onTick = options.onTick || defaultOnTick;
  this.stream = options.stream || process.stdout;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cli-spinner.Spinner.setDefaultSpinnerDelay"></a>[function <span class="apidocSignatureSpan">cli-spinner.Spinner.</span>setDefaultSpinnerDelay (value)](#apidoc.element.cli-spinner.Spinner.setDefaultSpinnerDelay)
- description and source-code
```javascript
setDefaultSpinnerDelay = function (value) {
  defaultSpinnerDelay = value;
}
```
- example usage
```shell
...


**'Spinner.setDefaultSpinnerString(spinnerString)'**

Sets the default spinner string for all newly created instances. Accepts either a String or an Integer index to reference the [built
-in spinners](#demo).


**'Spinner.setDefaultSpinnerDelay(spinnerDelay)'**

Sets the default spinner delay for all newly created instances.


**'Spinner.setSpinnerTitle(spinnerTitle)'**

Sets the spinner title. Use printf-style strings to position the spinner.
...
```

#### <a name="apidoc.element.cli-spinner.Spinner.setDefaultSpinnerString"></a>[function <span class="apidocSignatureSpan">cli-spinner.Spinner.</span>setDefaultSpinnerString (value)](#apidoc.element.cli-spinner.Spinner.setDefaultSpinnerString)
- description and source-code
```javascript
setDefaultSpinnerString = function (value) {
  defaultSpinnerString = value;
}
```
- example usage
```shell
...


**'obj.setSpinnerDelay(spinnerDelay)'**

Sets the spinner animation speed.


**'Spinner.setDefaultSpinnerString(spinnerString)'**

Sets the default spinner string for all newly created instances. Accepts either a String or an Integer index to reference the [built
-in spinners](#demo).


**'Spinner.setDefaultSpinnerDelay(spinnerDelay)'**

Sets the default spinner delay for all newly created instances.
...
```



# <a name="apidoc.module.cli-spinner.Spinner.prototype"></a>[module cli-spinner.Spinner.prototype](#apidoc.module.cli-spinner.Spinner.prototype)

#### <a name="apidoc.element.cli-spinner.Spinner.prototype.clearLine"></a>[function <span class="apidocSignatureSpan">cli-spinner.Spinner.prototype.</span>clearLine (stream)](#apidoc.element.cli-spinner.Spinner.prototype.clearLine)
- description and source-code
```javascript
clearLine = function (stream) {
  readline.clearLine(stream, 0);
  readline.cursorTo(stream, 0);
}
```
- example usage
```shell
...
'''
var obj = new Spinner('processing.. %s')

var obj = new Spinner({
    text: 'processing.. %s',
    stream: process.stderr,
    onTick: function(msg){
        this.clearLine(this.stream);
        this.stream.write(msg);
    }
})
'''

Create a new spinner object. The advanced options can be used in any combination, none of them are required.
...
```

#### <a name="apidoc.element.cli-spinner.Spinner.prototype.isSpinning"></a>[function <span class="apidocSignatureSpan">cli-spinner.Spinner.prototype.</span>isSpinning ()](#apidoc.element.cli-spinner.Spinner.prototype.isSpinning)
- description and source-code
```javascript
isSpinning = function () {
  return this.id !== undefined;
}
```
- example usage
```shell
...


**'Spinner.setSpinnerTitle(spinnerTitle)'**

Sets the spinner title. Use printf-style strings to position the spinner.


**'Spinner.isSpinning()'**

Returns true/false depending on whether the spinner is currently spinning.

##Demo

To see a demonstration of the built-in spinners, point your console at the 'example' folder and run:
...
```

#### <a name="apidoc.element.cli-spinner.Spinner.prototype.setSpinnerDelay"></a>[function <span class="apidocSignatureSpan">cli-spinner.Spinner.prototype.</span>setSpinnerDelay (n)](#apidoc.element.cli-spinner.Spinner.prototype.setSpinnerDelay)
- description and source-code
```javascript
setSpinnerDelay = function (n) {
  this.delay = n;
}
```
- example usage
```shell
...


**'obj.setSpinnerString(spinnerString)'**

Sets the spinner string. Accepts either a String or an Integer index to reference the [built-in spinners](#demo).


**'obj.setSpinnerDelay(spinnerDelay)'**

Sets the spinner animation speed.


**'Spinner.setDefaultSpinnerString(spinnerString)'**

Sets the default spinner string for all newly created instances. Accepts either a String or an Integer index to reference the [built
-in spinners](#demo).
...
```

#### <a name="apidoc.element.cli-spinner.Spinner.prototype.setSpinnerString"></a>[function <span class="apidocSignatureSpan">cli-spinner.Spinner.prototype.</span>setSpinnerString (str)](#apidoc.element.cli-spinner.Spinner.prototype.setSpinnerString)
- description and source-code
```javascript
setSpinnerString = function (str) {
  this.chars = mapToSpinner(str, this.spinners).split('');
}
```
- example usage
```shell
...

## Example usage

''''javascript
var Spinner = require('cli-spinner').Spinner;

var spinner = new Spinner('processing.. %s');
spinner.setSpinnerString('|/-\\');
spinner.start();
''''

## API

'''
var obj = new Spinner('processing.. %s')
...
```

#### <a name="apidoc.element.cli-spinner.Spinner.prototype.setSpinnerTitle"></a>[function <span class="apidocSignatureSpan">cli-spinner.Spinner.prototype.</span>setSpinnerTitle (str)](#apidoc.element.cli-spinner.Spinner.prototype.setSpinnerTitle)
- description and source-code
```javascript
setSpinnerTitle = function (str) {
  this.text = str;
}
```
- example usage
```shell
...


**'Spinner.setDefaultSpinnerDelay(spinnerDelay)'**

Sets the default spinner delay for all newly created instances.


**'Spinner.setSpinnerTitle(spinnerTitle)'**

Sets the spinner title. Use printf-style strings to position the spinner.


**'Spinner.isSpinning()'**

Returns true/false depending on whether the spinner is currently spinning.
...
```

#### <a name="apidoc.element.cli-spinner.Spinner.prototype.start"></a>[function <span class="apidocSignatureSpan">cli-spinner.Spinner.prototype.</span>start ()](#apidoc.element.cli-spinner.Spinner.prototype.start)
- description and source-code
```javascript
start = function () {

  var current = 0;
  var self = this;

  this.id = setInterval(function() {
    var msg = self.text.indexOf('%s') > -1
      ? self.text.replace('%s', self.chars[current])
      : self.chars[current] + ' ' + self.text;

    self.onTick(msg);

    current = ++current % self.chars.length;
  }, this.delay);
}
```
- example usage
```shell
...
## Example usage

''''javascript
var Spinner = require('cli-spinner').Spinner;

var spinner = new Spinner('processing.. %s');
spinner.setSpinnerString('|/-\\');
spinner.start();
''''

## API

'''
var obj = new Spinner('processing.. %s')
...
```

#### <a name="apidoc.element.cli-spinner.Spinner.prototype.stop"></a>[function <span class="apidocSignatureSpan">cli-spinner.Spinner.prototype.</span>stop (clear)](#apidoc.element.cli-spinner.Spinner.prototype.stop)
- description and source-code
```javascript
stop = function (clear) {
  clearInterval(this.id);
  this.id = undefined;
  if (clear) {
    this.clearLine(this.stream);
  }
}
```
- example usage
```shell
...


**'obj.start()'**

Starts the spinner.


**'obj.stop(clean)'**

Stops the spinner. Accepts a Boolean parameter to clean the console.


**'obj.setSpinnerString(spinnerString)'**

Sets the spinner string. Accepts either a String or an Integer index to reference the [built-in spinners](#demo).
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
