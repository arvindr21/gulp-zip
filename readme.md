# [gulp](https://github.com/wearefractal/gulp)-zip [![Build Status](https://travis-ci.org/sindresorhus/gulp-zip.svg?branch=master)](https://travis-ci.org/sindresorhus/gulp-zip)

> ZIP compress files


## Install

```bash
$ npm install --save-dev gulp-zip
```


## Usage

```js
var gulp = require('gulp');
var zip = require('gulp-zip');

gulp.task('default', function () {
	return gulp.src('src/*')
		.pipe(zip('archive.zip'))
		.pipe(gulp.dest('dist'));
});
```

### Maintain Directory Structure

Add `{base: "."}` to src to maintain the directory structure

```js
var gulp = require('gulp');
var zip = require('gulp-zip');

gulp.task('default', function () {
	return gulp.src([
                'index.html',
                'css/**',
                'js/**',
                'lib/**',
                'images/**',
                'plugin/**'
            ], {base: "."}))
		.pipe(zip('archive.zip'))
		.pipe(gulp.dest('dist'));
});
```

## API

### zip(filename)


## License

[MIT](http://opensource.org/licenses/MIT) © [Sindre Sorhus](http://sindresorhus.com)
