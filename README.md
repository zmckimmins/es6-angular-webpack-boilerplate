# ES6 Angular & Webpack Boilerplate
A simple Angular ES6 boilerplate with babel and webpack. It comes with some components and services as examples.

**Features**:
* Webpack
* ES6
* Babel
* eslint

**Info**
* `webpack.config.js` is already configured
* Run's a fully ES6 backend using babel-register.
* Compiled an ES6 Angular front end into browser runnable code.

**Components**
This app will have just two components:
* Profile: Displays all user information stored in profiles.
* NewProfile: Form that allows the posting of a new profile to the database.

## Set up and install dependencies
```
npm install
```

## Webpack setup.
If you don't already have Webpack installed on your machine, run `npm install webpack webpack-dev-server -g` to install it globally and to be able to run `webpack` or `webpack-dev-server` from your command line.

####

**Dependencies List**
## Front-End (dev-dependencies)
* webpack
* webpack-dev-server
* babel-loader
* css-loader
* html-loader
* style-loader

## Back-End
* babel-core `This is the core of the actual Babel compiler itself.`
* babel-preset-es2015 `This is the presets that we are telling Babel to follow to compile our code.`
* babel-register `This is the plugin that allows us to transpile our server side code on the fly,
  rather than running it through a build system such as Webpack.`
* angular
* angular-ui-router
* body-parser
* cors
* express
* mongoose

A list of all the dependencies are also in the `package.json` file.

**Directory Structure**

```
es6-profile
--/main
----/components
----/styles

--/server
----/components
------/profile

--/dist
----index.html
----/src

--webpack.config.js
--package.json
--server.js
--index.js
--.gitignore
```

As you can see from the above, you'll be following a component-based architecture.
All of your pre-compiled front-end code will be going into the `/main` directory.
It will then be compiled and placed inside of `/dist/src` by Webpack.

Luckily you don't need to worry about this for the back end, where you will be using babel-register
to compile your code on the fly.


## Server info.

In the `package.json`:

```json
  "babel": {
    "presets": ["babel-preset-es2015"]
  },
```
Tell's Babel what presets we want it to be using.

This is also often done inside of a `.babelrc` file; either will accomplish the same result.

####

`index.js` file:

```javascript
require('babel-core/register');
require('./server.js')
```

This code simply pulls in our `server.js` file and runs it through the Babel compiler via babel-register.
And that's all you need to do to start writing your back end in ES6! Babel will handle the rest for you.



Type `node index.js` in your command line(terminal) and you should see in the console: `Listening on 8910`.

* [Zach McKimmins](https://zacharymckimmins.com)
