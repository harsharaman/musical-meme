# A TDD Express API Repo with CI/CD pipeline with tests on TravisCI and AppVeyor with deployment in Heroku

[![Build Status](https://app.travis-ci.com/harsharaman/musical-meme.svg?branch=master)](https://app.travis-ci.com/harsharaman/musical-meme)

[![Coverage Status](https://coveralls.io/repos/github/harsharaman/musical-meme/badge.svg?branch=master)](https://coveralls.io/github/harsharaman/musical-meme?branch=master)

[![Maintainability](https://api.codeclimate.com/v1/badges/7659d19f10ab792df335/maintainability)](https://codeclimate.com/github/harsharaman/musical-meme/maintainability)

[![Test Coverage](https://api.codeclimate.com/v1/badges/7659d19f10ab792df335/test_coverage)](https://codeclimate.com/github/harsharaman/musical-meme/test_coverage)

[![Build status](https://ci.appveyor.com/api/projects/status/6b8muew93k34tct9?svg=true)](https://ci.appveyor.com/project/harsharaman/musical-meme)

#### Uses ES6

#### scripts in package.json works as follows:
prestart scripts builds the content of the src/ folder and puts it in the build/ folder. When you issue the yarn start command, this script runs first before the start script. <br>
start script now serves the content of the build/ folder instead of the src/ folder we were serving previously. This is the script you’ll use when serving the file in production. In fact, services like Heroku automatically run this script when you deploy. <br>
yarn startdev is used to start the server during development. From now on we will be using this script as we develop the app. Notice that we’re now using babel-node to run the app instead of regular node. The --exec flag forces babel-node to serve the src/ folder. For the start script, we use node since the files in the build/ folder have been compiled to ES5. <br>