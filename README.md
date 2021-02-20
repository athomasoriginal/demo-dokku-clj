# demo-dokku-clj

A barebones Clojure app, which can easily be deployed to Heroku or Dokku.

## About this Demo

This project was adapted from the https://github.com/heroku/clojure-getting-started.git project.  The difference is that we want to show you how to use `Clojure CLI Tools` instead of `Leiningen`.  How did we adapt it?

- add a `deps.edn` file (port the `project.clj` to `deps.edn`)
- add custom `bin/build.sh`
- add an alias to build the uberjar
- update `Procfile` to call custom alias

## Running Locally

Make sure you have Clojure installed.

```bash
$ git clone https://github.com/heroku/clojure-getting-started.git
$ cd clojure-getting-started
$ lein repl
```

Run the app

```clojure
user=> (require 'clojure-getting-started.web)
user=> (def server (clojure-getting-started.web/-main))
```

Visit the app at http://localhost:5000/

## Deploying to Dokku

The following are the official docs for a local Dokku setup which I recommend as a test run

- Setup Vagrant
  https://dokku.com/docs/getting-started/install/vagrant/
- Deploy Dokku app
  https://dokku.com/docs~v0.23.6/deployment/application-deployment/
  > To set the Clojure CLI version use the following `dokku config:set clojure-getting-started CLOJURE_CLI_VERSION=1.10.2.786`

## Deploying to Heroku

Also, install the [Heroku Toolbelt](https://toolbelt.heroku.com/)

```sh
$ heroku create
$ git push heroku main
$ heroku open
```

or

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

## Documentation

For more information about using Clojure on Heroku, see these Dev Center articles:

- [Clojure on Heroku](https://devcenter.heroku.com/categories/clojure)
