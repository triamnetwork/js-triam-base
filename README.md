# JS Triam Base

The triam-base library is the lowest-level Triam network helper library.  It consists of classes
to read, write, hash, and sign the xdr structures that are used in [stellar-core](https://github.com/stellar/stellar-core).
This is an implementation in JavaScript that can be used on either Node.js or web browsers.

* **[API Reference](https://triamnetwork.github.io/js-triam-base/)**

> **Warning!** Node version of this package is using [`ed25519`](https://www.npmjs.com/package/ed25519) package, a native implementation of [Ed25519](https://ed25519.cr.yp.to/) in Node.js, as an [optional dependency](https://docs.npmjs.com/files/package.json#optionaldependencies). This means that if for any reason installation of this package fails, `stellar-base` will fallback to the much slower implementation contained in [`tweetnacl`](https://www.npmjs.com/package/tweetnacl).
>
> If you are using `triam-base` in a browser you can ignore this. However, for production backend deployments you should definitely be using `ed25519`. If `ed25519` is successfully installed and working `TriamBase.FastSigning` variable will be equal `true`. Otherwise it will be `false`.

## Quick start

Using npm to include js-triam-base in your own project:
```shell
npm install --save triam-base
```

## Install

### To use as a module in a Node.js project
1. Install it using npm:

  ```shell
  npm install --save triam-base
  ```
2. require/import it in your JavaScript:

  ```js
  var TriamBase = require('triam-base');
  ```

Note that this method relies using a third party to host the JS library. This may not be entirely secure.

Make sure that you are using the latest version number. They can be found on the [releases page in Github](https://github.com/triamnetwork/js-triam-base/releases).

### To develop and test js-triam-base itself
1. Clone the repo

  ```shell
  git clone https://github.com/triamnetwork/js-triam-base.git
  ```
2. Install dependencies inside js-triam-base folder

  ```shell
  cd js-triam-base
  npm install
  ```

## Usage
For information on how to use js-triam-base, take a look at the docs in the [docs folder](./docs).

## Testing
To run all tests:
```shell
gulp test
```

To run a specific set of tests:
```shell
gulp test:node
gulp test:browser
```

## Documentation
Documentation for this repo lives inside the [docs folder](./docs).

## Contributing
Please see the [CONTRIBUTING.md](./CONTRIBUTING.md) for details on how to contribute to this project.

## Publishing to npm
```
npm version [<newversion> | major | minor | patch | premajor | preminor | prepatch | prerelease]
```
A new version will be published to npm **and** Bower by Travis CI.

npm >=2.13.0 required.
Read more about [npm version](https://docs.npmjs.com/cli/version).

## License
js-stellar-base is licensed under an Apache-2.0 license. See the [LICENSE](./LICENSE) file for details.
