# Docker images for Node.js

## Tags

### latest

* Based on [node:slim](https://hub.docker.com/_/node/) image
* Includes [Supervisor](http://supervisord.org) to manage your application process
* Adds application code to `/app` folder on build.
* `npm -q start` command executed in `/app` folder
* Console output directed to `/logs/out.log` and `/logs/err.log` files. You can access them by bind-mounting `/logs` path.
* Includes globally installed CoffeeScript to execute coffee files directly without transpilation.

See [sample application](https://github.com/eabay/docker-nodejs/tree/master/example) for basic usage.


### dev

Development version has the essentials to install packages require compilation steps. It also includes [supervisor](https://www.npmjs.org/package/supervisor) to restart your server on file changes and [node-inspector](https://www.npmjs.org/package/node-inspector) to debug your application. You can use [yarn](https://yarnpkg.com/) as a package manager.


## Alpine Linux based versions

There are Alpine Linux based versions (tagged as *alpine* and *dev-alpine*) build from [alpine-node](https://hub.docker.com/r/mhart/alpine-node/) image for minimal builds.
