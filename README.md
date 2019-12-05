# Gulp

要使用 Gulp，要安裝 Node.js，因為 Gulp 是基於 Node.js 開發而成

[Node.js](http://nodejs.org/download/) 

`npm install -g gulp` 

專案初始化  
`npm init`  package.json

安裝這個專案的 Gulp 套件  
`npm install gulp -save-dev`  

[gulp-webserver](https://www.npmjs.com/package/gulp-webserver)的套件  
`npm install gulp-webserver -save-dev`  

gulpfile.js

```
var gulp = require('gulp');
var webserver = require('gulp-webserver');

gulp.task('webserver', function() {
  gulp.src('./app/')
    .pipe(webserver({
      port:8888,
      livereload: true,
      directoryListing: false,
      open: true,
      fallback: 'index.html'
    }));
});

gulp.task('default',['webserver']);
```


建立 app的資料夾，放入網頁，執行 `gulp`  
`$ gulp`

## Usage

`$ npm install`
`$ gulp`
open  http://localhost:1234/  