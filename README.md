# npmdoc-sequelize-auto

#### basic api documentation for  [sequelize-auto (v0.4.28)](https://github.com/sequelize/sequelize-auto#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-sequelize-auto.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-sequelize-auto) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-sequelize-auto.svg)](https://travis-ci.org/npmdoc/node-npmdoc-sequelize-auto)

#### Automatically generate bare sequelize models from your database.

[![NPM](https://nodei.co/npm/sequelize-auto.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/sequelize-auto)

- [https://npmdoc.github.io/node-npmdoc-sequelize-auto/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-sequelize-auto/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-sequelize-auto/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-sequelize-auto/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-sequelize-auto/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-sequelize-auto/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Daniel Durante"
    },
    "bin": {
        "sequelize-auto": "bin/sequelize-auto"
    },
    "bugs": {
        "url": "https://github.com/sequelize/sequelize-auto/issues"
    },
    "dependencies": {
        "async": "^2.1.5",
        "graceful-fs-extra": "^2.0.0",
        "mkdirp": "^0.5.1",
        "sequelize": "^3.30.2",
        "yargs": "^6.6.0"
    },
    "description": "Automatically generate bare sequelize models from your database.",
    "devDependencies": {
        "chai": "^3.5.0",
        "cross-env": "^3.2.4",
        "istanbul": "^0.4.5",
        "lcov-result-merger": "^1.2.0",
        "mkdirp": "^0.5.1",
        "mocha": "^3.2.0",
        "mysql": "^2.13.0",
        "nyc": "^10.1.2",
        "pg": "^6.1.5",
        "pg-hstore": "^2.3.2",
        "sqlite3": "^3.1.8",
        "tedious": "^1.14.0"
    },
    "directories": {},
    "dist": {
        "shasum": "9102048a9e37aec30c434d1c75556f7aed10f6f1",
        "tarball": "https://registry.npmjs.org/sequelize-auto/-/sequelize-auto-0.4.28.tgz"
    },
    "engines": {
        "node": ">=0.10"
    },
    "gitHead": "863441e27ead2dc5a2184a1ac70617a215464fce",
    "homepage": "https://github.com/sequelize/sequelize-auto#readme",
    "keywords": [
        "mysql",
        "postgres",
        "sequelize",
        "sequelizejs",
        "mapper"
    ],
    "license": "MIT",
    "main": "index",
    "maintainers": [
        {
            "name": "durango"
        }
    ],
    "name": "sequelize-auto",
    "nyc": {
        "exclude": [
            "**/test/**.js"
        ]
    },
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/sequelize/sequelize-auto.git"
    },
    "scripts": {
        "clean-coverage": "rm -rf coverage && rm -rf coverage-*",
        "codeclimate": "npm run cover-all && npm run codeclimate-send && npm run clean-coverage",
        "codeclimate-send": "npm install -g codeclimate-test-reporter && CODECLIMATE_REPO_TOKEN=b9a25c5bf4c3875fb46ecb6d3a5f99e49f6872e6b92c074e5725d6dc2cd94f22 codeclimate-test-reporter < coverage/lcov.info",
        "cover": "rm -rf coverage && COVERAGE=true ./node_modules/.bin/nyc -r lcov npm run test",
        "cover-all": "npm run cover-mysql && npm run cover-postgres && npm run cover-postgres-native && npm run cover-sqlite && npm run merge-coverage",
        "cover-mysql": "DIALECT=mysql npm run cover && mv coverage coverage-mysql",
        "cover-postgres": "DIALECT=postgres npm run cover && mv coverage coverage-postgres",
        "cover-postgres-native": "DIALECT=postgres-native npm run cover && mv coverage coverage-postgres-native",
        "cover-sqlite": "DIALECT=sqlite npm run cover && mv coverage coverage-sqlite",
        "merge-coverage": "rm -rf coverage && mkdir coverage && ./node_modules/.bin/lcov-result-merger 'coverage-*/lcov.info' 'coverage/lcov.info'",
        "test": "mocha --globals setImmediate,clearImmediate,__core-js_shared__ --ui tdd --check-leaks --colors -t 15000 --reporter spec \"test/**/*.test.js\"",
        "test-mssql": "cross-env DIALECT=mssql npm run test",
        "test-mysql": "cross-env DIALECT=mysql npm run test",
        "test-postgres": "cross-env DIALECT=postgres npm run test",
        "test-sqlite": "cross-env DIALECT=sqlite npm run test"
    },
    "version": "0.4.28"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
