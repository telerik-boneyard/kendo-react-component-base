[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)
[![Build Status](https://travis-ci.org/telerik/kendo-react-component-base.svg?branch=master)](https://travis-ci.org/telerik/kendo-react-component-base)
[![npm version](https://badge.fury.io/js/%40telerik%2Fkendo-react-component-base.svg)](https://badge.fury.io/js/%40telerik%2Fkendo-react-component-base)

A starter repository for Kendo UI React components, which provides the basic directory structure and dependencies.

## Structure

- The `src` directory contains the component source code. All files should be have the `.jsx` extensions so that the build scripts may pick them.
- The `src/main.jsx` file should import and re-export all public components of the package. It is used for the `build-cdn` task. It is also the main entry point for the NPM package (as specified by the `package.json`). The `build-npm-package` transpiles it to `dist/npm/js/main.js`;
- The `src/Component.jsx` file is the actual sample component implementation.
- The `src/util.jsx` is an optional example of an additional file - you may remove it if unnecessary.

- The `examples` directory hosts the demos for the component. As a bare minimum, the component should have a `basic usage` and a `CDN` example.  The `CDN` example should work as expected after the `build-cdn` task has been run.
- The `test` directory contains the component tests. They are transpiled just like the source code itself, and are run with Jasmine in NodeJS.
- The `e2e` directory contains the end-to-end tests. They are transpiled just like the source code itself, and are run with Karma and Jasmine in the browser.
- The `docs` directory contains markdown files that document the specifics of the component.

## Gulp tasks

- `build-npm-package` - builds the scripts and styles in `dist/npm` in CommonJS format;
- `build-cdn` - builds the scripts and styles in `dist/cdn` in UMD format.
- `start` - starts the webpack-dev-server (with browsersync in front of it) - suitable for example preview, development and testing.
- `test` - runs the tests with Jasmine in NodeJS.
- `watch-test` - runs the tests in watch mode.
- `docs` - launches a preview server for the documentation in the `docs` directory
