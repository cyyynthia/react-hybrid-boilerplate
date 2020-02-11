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

 - No express: It uses Node's http module to create the web server;
 - Hot reload: It is capable of hot reloading while developing;
 - React Helmet and React Router are ready to be used, no extra-setup required;
 - Image minification with [imagemin](https://github.com/imagemin/imagemin) in production builds;
 - Pre-configured eslint; Please do not hate on my config if you don't like it, and just change it on your own;

You're of course able to edit the configuration to your needs.

**Note**: This boilerplate uses [css modules](https://github.com/css-modules/css-modules) by default. You can disable
them by looking at `webpack.config.js` line 90.

## Things I consider adding in the future

 - TypeScript support
 - Redux support
 - Reduce the shitcode from 64% to 34%
