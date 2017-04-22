# npmdoc-soap

#### api documentation for  [soap (v0.19.0)](https://github.com/milewise/node-soap#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-soap.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-soap) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-soap.svg)](https://travis-ci.org/npmdoc/node-npmdoc-soap)

#### A minimal node SOAP client

[![NPM](https://nodei.co/npm/soap.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/soap)

- [https://npmdoc.github.io/node-npmdoc-soap/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-soap/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-soap/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-soap/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-soap/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-soap/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Vinay Pulim"
    },
    "bugs": {
        "url": "https://github.com/milewise/node-soap/issues"
    },
    "dependencies": {
        "compress": "^0.99.0",
        "concat-stream": "^1.5.1",
        "debug": "~0.7.4",
        "ejs": "~2.5.5",
        "finalhandler": "^0.5.0",
        "lodash": "^3.10.1",
        "optional": "^0.1.3",
        "request": ">=2.9.0",
        "sax": ">=0.6",
        "selectn": "^0.9.6",
        "serve-static": "^1.11.1",
        "strip-bom": "~0.3.1",
        "ursa": "0.8.5 || >=0.9.4",
        "uuid": "^3.0.1",
        "xml-crypto": "~0.8.0"
    },
    "description": "A minimal node SOAP client",
    "devDependencies": {
        "body-parser": "^1.15.2",
        "colors": "^1.1.2",
        "coveralls": "^2.11.6",
        "diff": "^2.2.1",
        "doctoc": "^1.0.0",
        "duplexer": "~0.1.1",
        "express": "^4.14.0",
        "glob": "~3.2.8",
        "istanbul": "^0.4.1",
        "jshint": "2.3.0",
        "mocha": "~1.17.0",
        "readable-stream": "~2.0.2",
        "semver": "~5.0.3",
        "should": "~3.3.0",
        "sinon": "^1.17.5",
        "timekeeper": "~0.0.4"
    },
    "directories": {
        "lib": "./lib"
    },
    "dist": {
        "shasum": "e80d1ac07d43d2259869d5ca70f41499abf5f34e",
        "tarball": "https://registry.npmjs.org/soap/-/soap-0.19.0.tgz"
    },
    "engines": {
        "node": ">=0.10.0"
    },
    "gitHead": "bd762cc3a822fa699ad8bbceff753d58e5b2dafe",
    "homepage": "https://github.com/milewise/node-soap#readme",
    "keywords": [
        "soap"
    ],
    "license": "MIT",
    "main": "./index.js",
    "maintainers": [
        {
            "name": "vpulim"
        },
        {
            "name": "aaron"
        },
        {
            "name": "jsdevel"
        },
        {
            "name": "herom"
        }
    ],
    "name": "soap",
    "optionalDependencies": {
        "ursa": "0.8.5 || >=0.9.4"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/milewise/node-soap.git"
    },
    "scripts": {
        "cover": "istanbul cover _mocha -- --timeout 10000 test/*-test.js test/security/*.js",
        "coveralls": "cat ./coverage/lcov.info | ./node_modules/coveralls/bin/coveralls.js -v",
        "pretest": "jshint index.js lib test",
        "test": "mocha --timeout 10000 test/*-test.js test/security/*.js",
        "toc": "doctoc Readme.md --github --maxlevel 3"
    },
    "version": "0.19.0",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
