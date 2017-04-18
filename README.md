# npmdoc-forever-service

#### api documentation for  [forever-service (v0.5.9)](https://github.com/zapty/forever-service)  [![npm package](https://img.shields.io/npm/v/npmdoc-forever-service.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-forever-service) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-forever-service.svg)](https://travis-ci.org/npmdoc/node-npmdoc-forever-service)

#### Provision node script as a service via forever, allowing it to automatically start on boot, working across various Linux distros and OS

[![NPM](https://nodei.co/npm/forever-service.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/forever-service)

- [https://npmdoc.github.io/node-npmdoc-forever-service/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-forever-service/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-forever-service/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-forever-service/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-forever-service/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-forever-service/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Arvind Agarwal"
    },
    "bin": {
        "forever-service": "./bin/forever-service",
        "get-forever-config": "./bin/get-forever-config"
    },
    "bugs": {
        "url": "https://github.com/zapty/forever-service/issues"
    },
    "dependencies": {
        "async": "~0.9.0",
        "commander": "~2.3.0",
        "shelljs": "~0.3.0",
        "swig": "~1.4.2",
        "walker": "~1.0.6"
    },
    "description": "Provision node script as a service via forever, allowing it to automatically start on boot, working across various Linux distros and OS",
    "devDependencies": {
        "fs-extra": "^0.30.0",
        "mocha": "*",
        "should": "*"
    },
    "directories": {},
    "dist": {
        "shasum": "437302400aea09b9a2f0a2aa22ec737610cec75d",
        "tarball": "https://registry.npmjs.org/forever-service/-/forever-service-0.5.9.tgz"
    },
    "homepage": "https://github.com/zapty/forever-service",
    "keywords": [
        "forever",
        "nodejs",
        "aws",
        "amazon",
        "linux",
        "initd",
        "service",
        "logrotate",
        "reboot",
        "start",
        "service",
        "amazon linux",
        "centos",
        "redhat",
        "debian",
        "raspbian",
        "ubuntu",
        "busenlabs"
    ],
    "main": "lib/api.js",
    "maintainers": [
        {
            "name": "zapty"
        }
    ],
    "name": "forever-service",
    "optionalDependencies": {},
    "preferGlobal": "true",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/zapty/forever-service.git"
    },
    "scripts": {
        "test": "mocha test/*.js"
    },
    "version": "0.5.9"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
