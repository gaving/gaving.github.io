---
layout:     post
title:      gulp-phpcbf
date:       2015-04-22 20:17:00
---

Like [gulp-phpcs](https://github.com/JustBlackBird/gulp-phpcs) in your pipeline
but want it to fix your errors too? Meet [gulp-phpcbf](https://github.com/gaving/gulp-phpcbf)!

```javascript
var gulp = require('gulp');
var phpcbf = require('gulp-phpcbf');
var gutil = require('gutil');

gulp.task('phpcbf', function () {
  return gulp.src(['src/**/*.php', '!src/vendor/**/*.*'])
  .pipe(phpcbf({
    bin: 'phpcbf',
    standard: 'PSR2',
    warningSeverity: 0
  }))
  .on('error', gutil.log)
  .pipe(gulp.dest('src'));
});
```
