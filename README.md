
![](https://raw.githubusercontent.com/abrarShariar/ng2-webpack-starter/master/image.png)


This is a barebone starter project for getting up and running with [Angular 2](https://angular.io) using the popular module bundler [Webpack](https://webpack.github.io/)
The directory structure has been kept as similar as possible to the [Style Guide](https://angular.io/docs/ts/latest/guide/style-guide.html).

## Quick Start

```bash
# clone this repo
$ git clone https://github.com/abrarShariar/ng2-webpack-starter.git ng2-webpack

# change directory to your app
$ cd ng2-webpack

# install the dependencies with npm
$ npm install

# start the webpack-dev-server
$ npm start
```

Your site is running at [localhost:8081](http://localhost:8081/)

## Dependencies:
  
  * `node` and `npm`
  * Ensure you're running Node (`v5.x.x`+) and NPM (`3.x.x`+)


## Before getting started

Some important things to get acquainted with before you start coding :

  - The following files are neccessary at your project root before you hit **npm install**
  
     ```
    package.json
    tsconfig.json
    typings.json
    karma.conf.js
    webpack.config.js
     ```
	  Each of these files have specific purpose mentioned in the [official docs](https://angular.io)
  
  - For this starter kit the following files are kept in the ```/config``` folder
  
    ```
    helpers.js
    webpack.common.js
    webpack.dev.js
    webpack.prod.js
    ```
  - Note that we only config webpack for *development* and *production*, *test* is excluded intentionally to keep things simple.  
 
  - We have the following structure in the ```/src``` folder:
  
    ```
    app/
      app.component.ts
      ...
      ..
    index.html
    main.ts
    polyfills.ts
    vendor.ts
    ```
    
  - We take a look into our ```package.json``` file so that we get a basic understanding of what is going on with each command:
  
    ```
  "scripts": {
    "start": "webpack-dev-server --inline --progress --port 8081",
    "test": "karma start",
    "build": "rimraf dist && webpack --config config/webpack.prod.js --progress --profile --bail",
    "postinstall": "typings install"
    },
    ```
  
  - Notice that I have changed my port to ```8081``` 
  
  **Note:** In case you are having issues with localhost's port, change them from the following files:
  
    ```
    package.json/
          "start": "webpack-dev-server --inline --progress --port 8081",
    ```
    
    For webpack-dev-server
    ```
      config/webpack.dev.js/
    ```
    
    If you are getting error make sure you have changed in *node_modules*
    
     
     ```
    node_modules/
    webpack-dev-server/bin/
    webpack-dev-server.js
    ```
    
## Build

```
$ npm run build
```

You will find the **dist** folder at your project root for distribution.

## Deploy

**Deploy on Firebase**

Before proceeding make sure you have [Firebase command line tools](https://www.firebase.com/docs/hosting/guide/deploying.html)

At your project root enter :

```
$ firebase init
# set your root as dist
```
firebase.json is generated. We will keep it as default here.

```
$ firebase deploy
```
Your site will be running at your selected firebase location.

**Note:** Make sure you have set the ```dist``` folder as root.

> <3 Angular 2

> <3 Webpack
