<div align="center">

[![Version](https://img.shields.io/npm/v/@chin98edwin/eslint-plugin)](https://github.com/chin98edwin/eslint-plugin/releases)
![Bundle size](https://img.shields.io/bundlephobia/min/@chin98edwin/eslint-plugin)
[![License](https://img.shields.io/github/license/chin98edwin/eslint-plugin)](https://github.com/chin98edwin/eslint-plugin/blob/main/LICENSE)
[![Support me on Ko-fi](https://img.shields.io/static/v1?label&logo=kofi&logoColor=ffffff&message=Support%20me%20on%20Ko-fi&color=FF5E5B)](https://ko-fi.com/dev_chin98edwin)

</div>

<br/>

# About
* A shared ESLint plugin/config used by me; they are used in many of my open
  source projects and is a pain to copy-paste the long configs every time, so I
  made it into a package instead.
* The configs assume the project using it are written in TypeScript, but they
  should work just fine with plain JavaScript in most circumstances.
* It is named `eslint-plugin`, not `eslint-config` because I might be adding
  custom rules to this package in the future. So calling it "plugin" would be
  more appropriate in the long run.

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
npm i -D @chin98edwin/eslint-plugin
```
<br/>

With [Yarn](https://yarnpkg.com/package/@chin98edwin/eslint-plugin):
```sh
yarn add -D @chin98edwin/eslint-plugin
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

# Known Issues & Ways Around Them
In some cases, you may get errors like this:
> `ESLint couldn't determine the plugin "import" uniquely.`

Even with enough expertise in the NPM/Yarn/NodeJS ecosystem, you might be able
to solve it once before receiving the same error for another plugin.

Below are some approaches you can try to get around this problem. They are not
guaranteed to work, but should increase your odds in solving this problem.

<br/>

## 1. Use Yarn resolutions
[This ESLint guide](https://eslint-kit.gitbook.io/eslint-kit/common-issues#eslint-couldnt-determine-the-plugin-foo-uniquely) explains how to
resolve package conflicts by adding a `resolution` property to your project's
`package.json`.

<br/>

## 2. Update ESLint Plugin Dependencies
Update any dependencies related to ESLint to the latest versions available
(along with this one).

I will try to update this package as often as possible so that any plugins that
this package depends on stays up to date.

For example, your project might be using `eslint-config-next`.

Under the hood, both `eslint-config-next` and `@chin98edwin/eslint-plugin` uses
`eslint-plugin-import`.

When they depend on *different* versions of `eslint-plugin-import`, this causes
the error "`ESLint couldn't determine the plugin "import" uniquely.`" to appear.

If the latest versions of `eslint-config-next` and `@chin98edwin/eslint-plugin`
depend the *same* version of `eslint-plugin-import`, updating the packages would
solve the error.

<br/>

## 3. Pray

If all else fails, contact the authors of the related plugin libraries and
[pray](https://i.imgur.com/qfQYYPJ.jpg) that the depended libraries can be
updated soon so that you can resolve the issue with
[Method #2](#2-update-eslint-plugin-dependencies).

<br/>
