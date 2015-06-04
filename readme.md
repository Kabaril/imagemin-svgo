# imagemin-svgo [![Build Status](http://img.shields.io/travis/imagemin/imagemin-svgo.svg?style=flat)](https://travis-ci.org/imagemin/imagemin-svgo) [![Build status](https://ci.appveyor.com/api/projects/status/esa7m3u8bcol1mtr?svg=true)](https://ci.appveyor.com/project/ShinnosukeWatanabe/imagemin-svgo)

> svgo imagemin plugin


## Install

```
$ npm install --save imagemin-svgo
```


## Usage

```js
var Imagemin = require('imagemin');
var imageminSvgo = require('imagemin-svgo');

new Imagemin()
	.src('images/*.svg')
	.dest('build/images')
	.use(imageminSvgo())
	.run();
```

You can also use this plugin with [gulp](http://gulpjs.com):

```js
var gulp = require('gulp');
var imageminSvgo = require('imagemin-svgo');

gulp.task('default', function () {
	return gulp.src('images/*.svg')
		.pipe(imageminSvgo()())
		.pipe(gulp.dest('build/images'));
});
```


## API

### imageminSvgo(options)

#### options

Type: `object`

Pass options to [svgo](https://github.com/svg/svgo).


## License

MIT © [imagemin](https://github.com/imagemin)
