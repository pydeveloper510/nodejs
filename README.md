# nodejs

Error: spawn ENOENT
    at errnoException (child_process.js:1000:11)
    at Process.ChildProcess._handle.onexit (child_process.js:791:34)


(function() {
    var childProcess = require("child_process");
    var oldSpawn = childProcess.spawn;
    function mySpawn() {
        console.log('spawn called');
        console.log(arguments);
        var result = oldSpawn.apply(this, arguments);
        return result;
    }
    childProcess.spawn = mySpawn;
})();


# Error When install nodemon

- npm install nodemon -g
- Set enviroment variavles (Advanced system settings / Environment variable / Path )


# Can't call app in app function ???

# captcha usage
svg-captcha 
https://github.com/lazarofl/svg-captcha-express

# import ejs file
<%- include('./common/header'); %>
<% include ./common/header.ejs %>

# uninstall node js module
```
npm prune
```
모듈을 설치하고 나중에 사용하지 않는 모듈에 대해 정리할 때 npm prune 명령어를 쓰면 된다!!

 
```
{
  "name": "pdf",
  "version": "1.0.0",
  "description": "pdf module - lib: pdfmake",
  "main": "pdfApp.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "jin2rang",
  "license": "jin2rang",
  "dependencies": {
    "amqplib": "^0.7.1",
    "body-parser": "^1.19.0",
    "easy-pdf-merge": "^0.2.6",
    "express": "^4.17.1",
    "express-asyncify": "^1.0.1",
    "express-promise-router": "^4.1.0",
    "fs": "0.0.1-security",
    "mysql2": "^2.2.5",
    "node-fetch": "^2.6.1",
    "node-pdftk": "^2.1.3",
    "pdf-merger-js": "^3.1.0",
    "pdf-parse": "^1.1.1",
    "pdfmake": "^0.1.70",
    "request": "^2.88.2"
  }
}
```

package.json을 열어보면 현재 설치되어있는 모듈과 버전을 확인 할 수 있다.

1. dependencies에서 불필요한 모듈을 지운다.

2. 터미널 혹은 커맨드 창에 npm prune 명령어를 입력한다.

3. 끝!!
(node_modules폴더에 들어가면 내가 package.json에서 지웠던 모듈폴더가 없어져있는걸 확인 할 수 있다.)

# node js Excution_Policies Error
```
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```
