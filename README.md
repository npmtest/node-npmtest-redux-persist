# npmtest-redux-persist

#### basic test coverage for  [redux-persist (v4.6.0)](https://github.com/rt2zz/redux-persist)  [![npm package](https://img.shields.io/npm/v/npmtest-redux-persist.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-redux-persist) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-redux-persist.svg)](https://travis-ci.org/npmtest/node-npmtest-redux-persist)

#### persist and rehydrate redux stores

[![NPM](https://nodei.co/npm/redux-persist.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/redux-persist)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-redux-persist/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-redux-persist/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-redux-persist/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-redux-persist/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-redux-persist/build/test-report.html)|
| test-server-github : | [![github.com test-server](https://npmtest.github.io/node-npmtest-redux-persist/GitHub-Mark-32px.png)](https://npmtest.github.io/node-npmtest-redux-persist/build/app/index.html) | | build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-redux-persist/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-redux-persist/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-redux-persist/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-redux-persist/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-redux-persist/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-redux-persist/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-redux-persist/build/test-report.html](https://npmtest.github.io/node-npmtest-redux-persist/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-redux-persist/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-redux-persist/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-redux-persist/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-redux-persist/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-redux-persist/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-redux-persist/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-redux-persist/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-redux-persist/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "rt2zz"
    },
    "ava": {
        "require": [
            "babel-register",
            "babel-polyfill"
        ],
        "babel": "inherit"
    },
    "bugs": {
        "url": "https://github.com/rt2zz/redux-persist/issues"
    },
    "dependencies": {
        "json-stringify-safe": "^5.0.1",
        "lodash": "^4.17.4",
        "lodash-es": "^4.17.4"
    },
    "description": "persist and rehydrate redux stores",
    "devDependencies": {
        "ava": "^0.18.1",
        "babel-cli": "^6.22.2",
        "babel-core": "^6.22.1",
        "babel-eslint": "^7.1.1",
        "babel-loader": "^6.2.10",
        "babel-polyfill": "^6.22.0",
        "babel-preset-es2015": "^6.22.0",
        "babel-preset-stage-2": "^6.22.0",
        "cross-env": "^3.1.4",
        "immutable": "^3.8.1",
        "lodash-webpack-plugin": "^0.11.0",
        "redux": "^3.6.0",
        "rimraf": "~2.5.4",
        "standard": "^8.6.0",
        "webpack": "^2.2.1"
    },
    "directories": {},
    "dist": {
        "shasum": "3994793d5f2f38bf02591c9e693e16bf8eae2728",
        "tarball": "https://registry.npmjs.org/redux-persist/-/redux-persist-4.6.0.tgz"
    },
    "files": [
        "es",
        "dist",
        "lib",
        "src",
        "constants.js",
        "storages.js",
        "index.js.flow",
        "index.d.ts"
    ],
    "gitHead": "b1e29b95a2b8bcdc4b74b9f9a76ec2b8f47619d2",
    "homepage": "https://github.com/rt2zz/redux-persist",
    "jsnext:main": "es/index.js",
    "keywords": [
        "redux",
        "redux-middleware",
        "localstorage",
        "redux-persist",
        "redux-storage",
        "redux-rehydrate"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "rt2zz"
        }
    ],
    "module": "es/index.js",
    "name": "redux-persist",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/rt2zz/redux-persist.git"
    },
    "scripts": {
        "build": "npm run build:commonjs && npm run build:es && npm run build:umd && npm run build:umd:min && npm run copy-types",
        "build:commonjs": "cross-env BABEL_ENV=commonjs babel src --out-dir lib",
        "build:es": "cross-env BABEL_ENV=es babel src --out-dir es",
        "build:umd": "cross-env BABEL_ENV=commonjs webpack",
        "build:umd:min": "cross-env BABEL_ENV=commonjs NODE_ENV=production webpack",
        "build:watch": "npm run build:commonjs -- -watch",
        "clean": "rimraf lib dist es",
        "copy-types": "cp -r type-definitions/ lib/ && cp -r type-definitions/ es/",
        "prepublish": "npm run clean && npm run build",
        "test": "standard 'src/**/*.js' 'test/**/*.js' storages.js constants.js && BABEL_ENV=commonjs ava --esnext",
        "test:watch": "npm test -- --watch"
    },
    "standard": {
        "parser": "babel-eslint"
    },
    "typings": "lib/index.d.ts",
    "version": "4.6.0",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
