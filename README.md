# About
* A shared ESLint plugin/config used by me; they are used in many of my open
  source projects and it has been a pain to copy-paste the long configs, so I
  am making it into a package instead.
* The configs assume the project using it are written in TypeScript, but they
  should work just fine with plain JavaScript in most circumstances.

# Disclaimer
* The compilation of rules are just my personal preferences.
* There might be drastic changes in the configs from one version to another, and
  this applies for all future versions until this package reaches a stable
  version.

<br/>

# Usage
You can extend from one of the two available configs:

```js
// .eslintrc.js
module.exports = {
  extends: [
    // Simply recommended.
    // Suited for developing websites and apps.
    'plugin:@chin98edwin/recommended',
    // Same as above, but with warnings treated as errors.
    // Suited for maintaining libraries.
    'plugin:@chin98edwin/strict',
  ],
}
```

<br/>
