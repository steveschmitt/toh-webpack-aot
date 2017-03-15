# toh-webpack-aot
Tour of Heroes sample using AOT via Webpack plugin

This app is adapted from the [Tour of Heroes](https://angular.io/resources/live-examples/toh-6/ts/eplnkr.html) app from the [Angular Tutorial](https://angular.io/docs/ts/latest/tutorial/)

This app can be run in two different ways.

1. Run with JIT
2. Run with AOT

## Run with JIT (client-side module loading and compilation)
This is the same as shown in the [Tour of Heroes tutorial](https://angular.io/docs/ts/latest/tutorial/).  The **build** step just compiles TypeScript to JavaScript.  The **serve** steps starts lite-server with `src` as the root directory.  In the browser, the app starts by first loading SystemJS, which then loads the JavaScript, HTML, and CSS resources required by the app.
```
npm install
npm run clean
npm run build
npm run serve
```

## Run with AOT (ahead-of-time compilation)
This uses Webpack with the AOT plugin.  The **build:aot** step compiles the Angular modules into executable JavaScript in a single `build.js` file.  The **serve:aot** step starts lite-server with `aot` as the root directory.  In the browser, `build.js` starts the compiled app.
```
npm install
npm run clean
npm run build:aot
npm run serve:aot
```
