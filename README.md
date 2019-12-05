# Gulp

[gulp.js](https://gulpjs.com/) - The streaming build system
Automate and enhance your workflow  

## [Quick Start](https://gulpjs.com/docs/en/getting-started/quick-start)

Check for node, npm, and npx `node -v` `npx -v`
`npx mkdirp my-project`  
`cd my-project`
`npm init`
`npm install --save-dev gulp`

`gulp`

## Notes


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

## References

[npx 使用教程](https://www.ruanyifeng.com/blog/2019/02/npx.html)
`$ npx create-react-app my-react-app`  避免全局安装模块
执行 GitHub Gist 源码