# React Hybrid Boilerplate
[![License](https://img.shields.io/github/license/Bowser65/react-hybrid-boilerplate.svg?style=flat-square)](https://github.com/Bowser65/react-hybrid-boilerplate/blob/master/LICENSE)
[![Discord](https://img.shields.io/badge/chat-on%20Discord-7289DA.svg?style=flat-square)](https://discord.gg/DXKgqrP)

A boilerplate to quickly start working on React projects using hybrid rendering.

## Hybrid rendering?
Basically, in production there is a small web server (here pure native http module) that'll be in charge of
pre-rendering your React application. It then gets hydrated client-side, which means React will then bind all
the events it needs to bind and work as if it was CSR. It helps to enhance SEO, load times, and makes your
application usable by users who disabled JavaScript.

## Features
 - No expressjs: It uses Node's http module to create the web server, and not bloated stuff;
 - Hot reload: It is capable of hot reloading while developing;
 - [react-helmet](https://github.com/nfl/react-helmet), [react-router](https://github.com/ReactTraining/react-router)
and [rc-tooltip](https://github.com/react-component/tooltip) are ready to be used, no extra-setup required;
 - Image minification with [imagemin](https://github.com/imagemin/imagemin) in production builds;
 - Pre-configured eslint; Please do not hate on my config if you don't like it, and just change it on your own;
    - Based on [standard](https://github.com/standard/standard) with some tweaking and rules for React

There are also some env variables that get injected in your application through webpack's `DefinePlugin`:
 - `WEBPACK.GIT_REVISION` - Git revision; null if git isn't present.

You're of course able to edit the configuration to your needs.

**Note**: This boilerplate uses [css modules](https://github.com/css-modules/css-modules) by default. You can disable
them by looking at `webpack.config.js` line 90.

## How to use
**Note**: This boilerplate uses [pnpm](https://github.com/pnpm/pnpm) for dependency management.

### Development
Both webpack and the http server must be running
 - `pnpm run dev` - Runs the http server with [nodemon](https://github.com/remy/nodemon)
 - `pnpm run watch` - Runs webpack dev server

Then, open http://localhost:8080 in your web browser and start tinkering!

### Production
 - Build the app: `pnpm run build`
 - And then start the http server! `pnpm run start`

You can change the port by setting the PORT env variable.

## Things I consider adding in the future
 - TypeScript support
 - Redux support
 - Reduce the shitcode from 67% to 34%
 - Add gzipping
 - Something to easily configure the boilerplate w/o having to edit stuff (cli args? env vars?)
 - Markdown support (Export as React component)
