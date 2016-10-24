# time-grunt [![Build Status](https://travis-ci.org/sindresorhus/time-grunt.svg?branch=master)](https://travis-ci.org/sindresorhus/time-grunt)

> Display the elapsed execution time of [grunt](http://gruntjs.com) tasks

![](screenshot.png)


## Install

```
$ npm install --save-dev time-grunt
```


## Usage

```js
// Gruntfile.js
module.exports = grunt => {
	// require it at the top and pass in the grunt instance
	require('time-grunt')(grunt);

	grunt.initConfig();
}
```


## Optional callback

If you want to collect the timing stats for your own use, pass in a callback:

```js
require('time-grunt')(grunt, (stats, done) => {
	// do whatever you want with the stats
	uploadReport(stats);

	// be sure to let grunt know when to exit
	done();
});
```


## Clean layout

The `watch` task is hidden to reduce clutter.


## License

MIT © [Sindre Sorhus](https://sindresorhus.com)
