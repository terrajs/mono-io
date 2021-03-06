<h1 align="center"><img src="https://user-images.githubusercontent.com/904724/31045653-d73c6302-a5e8-11e7-8db6-058077d4a848.png" width="350" alt="Mono"/></h1>

> Socket.io module for [Mono](https://github.com/terrajs/mono)

[![npm version](https://img.shields.io/npm/v/mono-io.svg)](https://www.npmjs.com/package/mono-io)
[![Travis](https://img.shields.io/travis/terrajs/mono-io/master.svg)](https://travis-ci.org/terrajs/mono-io)
[![Coverage](https://img.shields.io/codecov/c/github/terrajs/mono-io/master.svg)](https://codecov.io/gh/terrajs/mono-io.js)
[![license](https://img.shields.io/github/license/terrajs/mono-io.svg)](https://github.com/terrajs/mono-io/blob/master/LICENSE)

Mono-io uses [socket.io](https://github.com/socketio/socket.io) and [socketio-jwt](https://github.com/auth0-community/socketio-jwt) to handle sockets with authorization via JWT.

## Installation

```bash
npm install --save mono-io
```

Then, in your configuration file of your Mono application (example: `conf/application.js`):

```js
module.exports = {
  mono: {
    modules: ['mono-io']
  }
}
```

## Configuration

mono-io will use the `io` property of your configuration (example: `conf/development.js`):

```js
module.exports = {
  mono: {
    io: {
      // See options here: https://github.com/socketio/socket.io/blob/master/docs/API.md#new-serverhttpserver-options
    }
  }
}
```

## Usage

In your modules files, you can access `io` instance:

```js
const { io } = require('mono-io')

io.on('connection', function (socket) {
  console.log(socket)
})
```
