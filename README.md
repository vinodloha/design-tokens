# design-tokens
Package to make designer and developer workflow seamless, by supplying design tokens generated with [style-dictionary](https://amzn.github.io/style-dictionary/).

## Installation

```bash
yarn add @xts-ds/design-tokens
```

## Uses 

Package publishes tokens for 5 platforms.

```json
{
  "platforms": {
    "js": "dist/js/index.es6.js",
    "scss": "dist/scss/tokens.scss",
    "android": "dist/android/",
    "ios":"dist/ios/",
    "ios-swift": "dist/ios-swift/"
  }
}
```
### React

```javascript

import * as theme from '@xts-ds/design-tokens/dist/js/index.es6'

export default theme;
```

### Commit Workflow

Based on the commit messages, increment the version from the latest release.

- If the string "BREAKING CHANGE" or "major" is found anywhere in any of the commit messages or descriptions the major version will be incremented.
- If a commit message begins with the string "feat" or includes "minor" then the minor version will be increased. This works for most common commit metadata for feature additions: "feat: new API" and "feature: new API".
- All other changes will increment the patch version.

### Token Source Update 

Commit newly generated tokens under `src/*`.

```bash
git add .
git commit -m "Commit message"
git push origin fix/your-branch
```
