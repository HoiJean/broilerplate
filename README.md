Broilerplate
================

A boilerplate with SASS & JS. It serves the following goodness on a shiny plate:

* SASS
* jQuery Plugin builder
* Grunt support
* Opengraph implementation
* Best practices for icons
* RTL-support
* Support for old IEs (aka `oldie`)
* Support for [editorconfig](http://editorconfig.org/)

So you can eat your broiler and have it.

Installation
------------

Download this repository via…

* [Bower](http://bower.io/): `bower install git://github.com/fboes/broilerplate.git`
* [NPM](https://www.npmjs.org/): `npm install git+https://github.com/fboes/broilerplate.git`

You also need:

* [Grunt](http://gruntjs.com/)
* [SASS](http://sass-lang.com/)

Setup your development space:

1. Install Grunt plugins via `npm install`
2. Check Gruntfile for any file or host references
3. You may want to replace all variables (like `{{ VARNAME }}`) with a meaningful text or variable

Variables used in templates:

* `{{ BASE_URL }}`: Base url including protocol, domain name and base path. Does not end with `/`
* `{{ RELATIVE_URL }}`: URL of current document relative to base path. Does start with a `/`
* `{{ SITENAME }}`: Title of your project
* `{{ TITLE }}`: Title of the current page
* `{{ DESCRIPTION }}`: Description of the current page

Developing
----------

1. Start Grunt watcher via `grunt watch`
2. Start [LiveReload](http://livereload.com/) in your browser
3. Develop
4. Commit to your repository
5. Use `grunt shell:prev` to deploy to your preview server

See `docs/development` for more information

Version
-------

Version: 1.0.0 (2015-04-08)

Legal stuff
-----------

Author: [Frank Boës](http://3960.org)

Copyright & license: See LICENSE.txt
