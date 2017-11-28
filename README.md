# postcss-sass [![Build Status](https://travis-ci.org/AleshaOleg/postcss-sass.svg?branch=master)](https://travis-ci.org/AleshaOleg/postcss-sass) [![Coverage Status](https://coveralls.io/repos/github/AleshaOleg/postcss-sass/badge.svg?branch=development)](https://coveralls.io/github/AleshaOleg/postcss-sass?branch=development)

A [Sass](http://sass-lang.com/) parser for [PostCSS](https://github.com/postcss/postcss), using [gonzales-pe](https://github.com/tonyganch/gonzales-pe).

**Not all Sass syntax supported. Parser under development.**

**This module does not compile Sass.** It simply parses mixins as custom at-rules & variables as properties, so that PostCSS plugins can then transform Sass source code alongside CSS.

## Install
`npm i postcss-sass --save`

## Usage
```js
var postcssSass = require("postcss-sass");

postcss(plugins).process(sass, { syntax: postcssSass }).then(function (result) {
    result.content // Sass with transformations
});
```
