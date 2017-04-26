# npmdoc-mysql2

#### basic api documentation for  [mysql2 (v1.2.0)](https://github.com/sidorares/node-mysql2#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-mysql2.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-mysql2) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-mysql2.svg)](https://travis-ci.org/npmdoc/node-npmdoc-mysql2)

#### fast mysql driver. Implements core protocol, prepared statements, ssl and compression in native JS

[![NPM](https://nodei.co/npm/mysql2.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/mysql2)

- [https://npmdoc.github.io/node-npmdoc-mysql2/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-mysql2/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-mysql2/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-mysql2/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-mysql2/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-mysql2/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Andrey Sidorov"
    },
    "bugs": {
        "url": "https://github.com/sidorares/node-mysql2/issues"
    },
    "dependencies": {
        "cardinal": "1.0.0",
        "denque": "^1.1.1",
        "generate-function": "^2.0.0",
        "iconv-lite": "^0.4.13",
        "long": "^3.2.0",
        "lru-cache": "^4.0.1",
        "named-placeholders": "1.1.1",
        "object-assign": "^4.1.1",
        "readable-stream": "2.2.2",
        "safe-buffer": "^5.0.1",
        "seq-queue": "0.0.5",
        "sqlstring": "^2.2.0"
    },
    "description": "fast mysql driver. Implements core protocol, prepared statements, ssl and compression in native JS",
    "devDependencies": {
        "assert-diff": "^1.0.1",
        "eslint": "3.15.0",
        "eslint-plugin-markdown": "^1.0.0-beta.2",
        "husky": "^0.13.0",
        "portfinder": "^1.0.10",
        "progress": "1.1.8",
        "urun": "0.0.8",
        "utest": "0.0.8"
    },
    "directories": {
        "example": "examples"
    },
    "dist": {
        "shasum": "3ac6a419a783a66aac8fd7eab8a71089a2612b79",
        "tarball": "https://registry.npmjs.org/mysql2/-/mysql2-1.2.0.tgz"
    },
    "engines": {
        "node": ">= 0.10"
    },
    "files": [
        "lib",
        "index.js",
        "promise.js"
    ],
    "gitHead": "c5c0c90000e72259381306d86f2c80ec9f4c38b1",
    "homepage": "https://github.com/sidorares/node-mysql2#readme",
    "keywords": [
        "mysql",
        "client",
        "server"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "iarna"
        },
        {
            "name": "sidorares"
        },
        {
            "name": "sushantdhiman"
        }
    ],
    "name": "mysql2",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/sidorares/node-mysql2.git"
    },
    "scripts": {
        "benchmark": "./benchmarks/run-unit.js",
        "lint": "npm run lint:docs && npm run lint:code",
        "lint:code": "eslint index.js promise.js 'lib/**/*.js' 'test/**/*.js'",
        "lint:docs": "eslint README.md Contributing.md 'documentation/**/*.md' examples/*.js",
        "precommit": "npm run lint",
        "test": "npm run lint && npm run test:raw",
        "test:raw": "node ./test/run.js && MYSQL_USE_COMPRESSION=1 node ./test/run.js"
    },
    "version": "1.2.0",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
