![logo](https://raw.githubusercontent.com/TrigenSoftware/ColaScript/master/colalogo.png)

ColaScript is the language that compiles into JavaScript. This language is similar to Dart, CoffeeScript, Python, Go and PHP, with some original ideas. Compiler based on [UglifyJS2](https://github.com/mishoo/UglifyJS2). You can try ColaScript [here (stable)](http://cola.trigen.pro) or [here (dev)](http://cola.trigen.pro/dev/). [Learn more about ColaScript](https://github.com/TrigenSoftware/ColaScript/wiki/A-Tour-of-the-ColaScript).

## Installation

Firstly, make sure you have installed the latest version of [node.js](http://nodejs.org/)
(You may need to restart your computer after this step).

From NPM for use as a command line app:

```
$ npm install cola-script -g
```

From NPM for programmatic use:

```
$ npm install cola-script
```

From Bower for using in browser:

```
$ bower install cola-script
```

From Git:

```
$ git clone git://github.com/TrigenSoftware/ColaScript.git
$ cd ColaScript
$ npm link .
```

## Usage
    
Use it same as in [UglifyJS2](https://github.com/mishoo/UglifyJS2), except:

```
-j, --js, --javascript        Work with JavaScript (by default Cola will
                              expect ColaScript).                    [boolean]
-n, --node                    Enable compilation for node.           [boolean]
-P, --packages                Path to packages.json (packages.json by
                              default).                               [string]
-i, --ignore-main-wrapping    Ignore `main` wrapping.                [boolean]
--browser-cola                Build itself (Cola) for running Cola in browser.
                                                                     [boolean]
```
       
Simple example of usage:

```
$ cola main.cola -o main.min.js -m -c
```
    
## In browser

During developing is more comfortable to compile the code directly in your browser, for that add `browser-cola.js` to `your.html` code:

```html
<script src="path/to/browser-cola.js"></script>
```
	
Now you can run your Cola-Code:

```html
<script type="text/colascript" src="path/to/your.cola"></script
```
	
If `your.cola` depends on other scripts in `your.html`, it's better to notice `browser-cola` about it:

```html
<script type="text/colascript" src="angular.min.js"></script>
<script type="text/colascript" src="path/to/your.cola"></script>
```	