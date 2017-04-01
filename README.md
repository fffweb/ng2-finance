# NG2 Finance
Can produce dist files , but dist file not work in local file system, cause path is not set right like ist   <link rel="stylesheet" href="/css/main.css?1491027775205">

[![Build Status](https://travis-ci.org/mpetkov/ng2-finance.svg?branch=master)](https://travis-ci.org/mpetkov/ng2-finance)
[![Coverage Status](https://coveralls.io/repos/github/mpetkov/ng2-finance/badge.svg?branch=master)](https://coveralls.io/github/mpetkov/ng2-finance?branch=master)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Dependencies Status](https://david-dm.org/mpetkov/ng2-finance/status.svg)](https://david-dm.org/mpetkov/ng2-finance)
[![DevDependencies Status](https://david-dm.org/mpetkov/ng2-finance/dev-status.svg)](https://david-dm.org/mpetkov/ng2-finance?type=dev)

Finance dashboard using Yahoo's public APIs. 
* [Live Demo*](http://projects.marinpetkov.com/ng2-finance/#/watchlist/FB) - Loads Yahoo's public API.
* [Static Demo*](http://projects.marinpetkov.com/ng2-finance/static/#/watchlist/FB) - Loads local JSON files.

<i>*This is for demo purposes only, please don't rely on the prices provided.</i>

![Screenshot](http://projects.marinpetkov.com/ng2-finance/preview.jpg)

# Features

* Search for any stock symbol to view historical data, summary, and news.
* Add and remove stock symbols to favorites.
* Stock data refreshes every 15 seconds in the background.
* Settings are saved to local storage.
* Fully responsive.
* Continuous integration and code coverage with Travis CI and Coveralls.

# Todo List

- [ ] 100% code coverage
- [ ] Convert to React
- [ ] Add advanced chart options
- [ ] Add a way to view more info about a stock
- [ ] Create a markets overview page that displays movers, gainers, loser, etc

# Quick Start

```bash
$ git clone https://github.com/mpetkov/ng2-finance.git
$ cd ng2-finance
$ npm install
$ npm start
```

# Configuration

Default application server configuration

```js
var PORT             = 5555;
var LIVE_RELOAD_PORT = 4002;
var DOCS_PORT        = 4003;
var APP_BASE         = '/';
```

Configure at runtime

```bash
$ npm start -- --port 8080 --reload-port 4000 --base /my-app/
```

## Environment configuration

If you have different environments and you need to configure them to use different end points, settings, etc. you can use the files `dev.ts` or `prod.ts` in`./tools/env/`. The name of the file is environment you want to use.

The environment can be specified by using:

```bash
$ npm start -- --env-config ENV_NAME
```

Currently the `ENV_NAME`s are `dev`, `prod`, `staging`, but you can simply add a different file `"ENV_NAME.ts".` file in order to alter extra such environments.

# Running tests

```bash
$ npm test

# Development. Your app will be watched by karma
# on each change all your specs will be executed.
$ npm run test.watch
# NB: The command above might fail with a "EMFILE: too many open files" error.
# Some OS have a small limit of opened file descriptors (256) by defaul
# and will result in the EMFILE error.
# You can raise the maximum of file descriptors by running the command below:
$ ulimit -n 10480


# code coverage (istanbul)
# auto-generated at the end of `npm test`
# view coverage report:
$ npm run serve.coverage

# e2e (aka. end-to-end, integration) - In three different shell windows
# Make sure you don't have a global instance of Protractor
# Make sure you do have Java in your PATH (required for webdriver)

# npm install webdriver-manager <- Install this first for e2e testing
# npm run webdriver-update <- You will need to run this the first time
$ npm run webdriver-start
$ npm run serve.e2e
$ npm run e2e

# e2e live mode - Protractor interactive mode
# Instead of last command above, you can use:
$ npm run e2e.live
```

# License

The MIT License

# Acknowledgments

* [mgechev](https://github.com/mgechev) for creating the excellent [angular-seed](https://github.com/mgechev/angular-seed) project