useragent.js
===========
[![npm](https://img.shields.io/npm/v/useragent.js.svg)](https://www.npmjs.com/package/useragent.js)
[![Coverage Status](https://coveralls.io/repos/zsxsoft/useragent.js/badge.svg)](https://coveralls.io/r/zsxsoft/useragent.js)
[![Build Status](https://travis-ci.org/zsxsoft/useragent.js.svg?branch=master)](https://travis-ci.org/zsxsoft/useragent.js)
[![David deps](https://david-dm.org/zsxsoft/useragent.js.svg)](https://david-dm.org/zsxsoft/useragent.js)
[![npm](https://img.shields.io/npm/dm/useragent.js.svg)](https://www.npmjs.com/package/useragent.js)
[![GitHub release](https://img.shields.io/github/release/zsxsoft/useragent.js.svg)](https://github.com/zsxsoft/useragent.js/releases)

A User-agent analyze project. Demo: http://project.zsxsoft.com/useragent.js/withimage.html

##Compatibility
Node.JS / (Windows) Classical ASP / (Windows) WScript / (Windows) CScript / Internet Explorer *+ / Google Chrome / Mozilla Firefox / Apple Safari

###IE&lt;8
Please import a Polyfill of ``Object.keys`` before import this. See here: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/keys)

##Installion
``$ npm install useragent.js``

##Compress

If you want to use it in the browser directly, please run ``grunt`` to compress it.

##Test
```bash
$ npm test
```

##Run
####In Node
```javascript
var userAgent = require("useragent.js");
var ua = userAgent.analyze("Mozilla/5.0 (Windows NT 10.0; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/41.0.2251.0 Safari/537.36");
console.log("TEST UA: " + ua.ua);
console.log("TEST BROWSER:" + ua.browser.full + " (" + ua.browser.name + " VERSION = " + ua.browser.version + " )");
console.log("TEST OS:" + ua.os.full + " (" + ua.os.name + " VERSION = " + ua.os.version + " )");
console.log("TEST DEVICE:" + ua.device.full);
```

####In Webpack / browserify
```javascript
import Useragent from 'useragent.js';
console.log(Useragent);
```

####In Browser
[Click here](http://zsxsoft.github.io/useragent.js/basic.html)
```javascript
(function () {
		var ua = USERAGENT.analyze(navigator.userAgent);
		document.getElementById("useragent").innerHTML = ua.ua;
		document.getElementById("browser").innerHTML = ua.browser.full + " (" + ua.browser.name + " VERSION = "  + ua.browser.version + " )";
		document.getElementById("os").innerHTML = ua.os.full + " (" + ua.os.name + " VERSION = "  + ua.os.version + " )";
		document.getElementById("device").innerHTML = ua.device.full;
})();
```

####In RequireJS
[Click here](http://zsxsoft.github.io/useragent.js/requirejs.html)

####In SeaJS
[Click here](http://zsxsoft.github.io/useragent.js/seajs.html)

####In Classical ASP
[Click here](http://zsxsoft.github.io/useragent.js/classicalasp.html)

## Result
```javascript
{ ua: 'Mozilla/5.0 (iPad; CPU OS 7_1_2 like Mac OS X) AppleWebKit/537.51.2 (KHTML, like Gecko) Mobile/11D257 IPadQQ/4.1.1.14',
  os:
   { ua: 'Mozilla/5.0 (iPad; CPU OS 7_1_2 like Mac OS X) AppleWebKit/537.51.2 (KHTML, like Gecko) Mobile/11D257 IPadQQ/4.1.1.14',
     name: 'iOS',
     version: '7.1.2',
     full: 'iOS 7.1.2',
     windows: false,
     linux: false,
     x64: false,
     dir: 'os',
     image: 'mac-3' },
  device:
   { ua: 'Mozilla/5.0 (iPad; CPU OS 7_1_2 like Mac OS X) AppleWebKit/537.51.2 (KHTML, like Gecko) Mobile/11D257 IPadQQ/4.1.1.14',
     name: 'Apple iPad',
     image: 'ipad',
     brand: 'Apple',
     model: 'iPad',
     dir: 'device',
     full: 'Apple iPad' },
  browser:
   { ua: 'Mozilla/5.0 (iPad; CPU OS 7_1_2 like Mac OS X) AppleWebKit/537.51.2 (KHTML, like Gecko) Mobile/11D257 IPadQQ/4.1.1.14',
     name: 'QQ',
     version: '4.1.1.14',
     full: 'QQ 4.1.1.14',
     image: 'qq',
     dir: 'browser' },
  platform: 
  /*
    Copied from device or os.
    .platform = .device, 
        but if device.name === "" then .platform = .os
   */
   { ua: 'Mozilla/5.0 (iPad; CPU OS 7_1_2 like Mac OS X) AppleWebKit/537.51.2 (KHTML, like Gecko) Mobile/11D257 IPadQQ/4.1.1.14',
     name: 'Apple iPad',
     image: 'ipad',
     brand: 'Apple',
     model: 'iPad',
     dir: 'device',
     full: 'Apple iPad' } }
```

## Supported Browsers/Platforms

[Click here to see full list.](http://project.zsxsoft.com/useragent.js/supported.html)

Tested Browsers: Amazon Silk / Android Webkit / Avant Browser / Comodo Dragon / curl / Firefox / Google Chrome / Internet Explorer / Microsoft Edge / Links / Lynx / Maxthon / MxNitro / Opera / QQBrowser / Safari SRWare Iron / Teleca Q7 / UC Browser / Vivaldi / W3M / wget / Yandex.Browser and so on.. 

OS: Android / Arch Linux / CentOS / Chrome OS / Debain / Fedora / FreeBSD / OSX / Red Hat / openSUSE / SymbianOS / Unix / Palm webOS / Windows 3.1 - 10 / Ubuntu / Linux and so on..

Devices: Xiaomi / BlackBerry / Nexus / HTC / Huawei / Kindle / Lenovo / LG / Motorola / Nokia / OnePlus / PlayStation / Samsung / Sony Xperia / ZTE / Ubuntu / Windows Phone / Apple Family and so on.


## License

The MIT License

The images can be gotten from [php-useragent](https://github.com/zsxsoft/php-useragent).