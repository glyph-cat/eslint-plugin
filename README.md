<div align="center">

[![Version](https://img.shields.io/npm/v/@chin98edwin/eslint-plugin)](https://github.com/chin98edwin/eslint-plugin/releases)
![Bundle size](https://img.shields.io/bundlephobia/min/@chin98edwin/eslint-plugin)
[![License](![GitHub](https://img.shields.io/github/license/chin98edwin/eslint-plugin))](https://github.com/chin98edwin/eslint-plugin/blob/main/LICENSE)
[![Support me on Ko-fi](https://img.shields.io/static/v1?label&logo=kofi&logoColor=ffffff&message=Support%20me%20on%20Ko-fi&color=FF5E5B)](https://ko-fi.com/dev_chin98edwin)

</div>

<br/>

# Table of Contents
<!-- Automatically generated by VS Code -->
- [Table of Contents](#table-of-contents)
- [About](#about)
- [Disclaimer](#disclaimer)
- [Installation](#installation)
- [Usage](#usage)

<br/>

# About
* A shared ESLint plugin/config used by me; they are used in many of my open
  source projects and it has been a pain to copy-paste the long configs, so I
  am making it into a package instead.
* The configs assume the project using it are written in TypeScript, but they
  should work just fine with plain JavaScript in most circumstances.

<br/>

# Disclaimer
* The compilation of rules are just my personal preferences.
* There might be drastic changes in the configs from one version to another, and
  this applies for all future versions until this package reaches a stable
  version.

<br/>

# Installation

With [NPM](https://www.npmjs.com/package/@chin98edwin/eslint-plugin):
```sh
npm i @chin98edwin/eslint-plugin
```
<br/>

With [Yarn](https://yarnpkg.com/package/@chin98edwin/eslint-plugin):
```sh
yarn add @chin98edwin/eslint-plugin
```
<br/>

# Usage
You can extend from one of the two available configs:

```js
// .eslintrc.js
module.exports = {
  extends: [

    // For developing websites and apps:
    'plugin:@chin98edwin/recommended',

    // For maintaining libraries:
    'plugin:@chin98edwin/strict',
    // (Same as '/recommended', but warnings are treated as errors)

  ],
}
```

<br/>
