# amplitude-esbuild

Build with:
```
yarn install
yarn build
```

Results in:


```
yarn run v1.22.17
$ yarn run esbuild --bundle index.js
$ /home/adam/amplitude-esbuild/node_modules/.bin/esbuild --bundle index.js
 > node_modules/amplitude-js/amplitude.esm.js:1:26: error: Could not resolve "@babel/runtime/helpers/objectSpread" (mark it as external to exclude it from the bundle)
    1 │ import _objectSpread from '@babel/runtime/helpers/objectSpread';
      ╵                           ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

 > node_modules/amplitude-js/amplitude.esm.js:2:28: error: Could not resolve "@babel/runtime/helpers/defineProperty" (mark it as external to exclude it from the bundle)
    2 │ import _defineProperty from '@babel/runtime/helpers/defineProperty';
      ╵                             ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

 > node_modules/amplitude-js/amplitude.esm.js:4:20: error: Could not resolve "@babel/runtime/helpers/typeof" (mark it as external to exclude it from the bundle)
    4 │ import _typeof from '@babel/runtime/helpers/typeof';
      ╵                     ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

 > node_modules/amplitude-js/amplitude.esm.js:5:31: error: Could not resolve "@babel/runtime/helpers/toConsumableArray" (mark it as external to exclude it from the bundle)
    5 │ import _toConsumableArray from '@babel/runtime/helpers/toConsumableArray';
      ╵                                ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

 > node_modules/amplitude-js/amplitude.esm.js:6:28: error: Could not resolve "@babel/runtime/helpers/classCallCheck" (mark it as external to exclude it from the bundle)
    6 │ import _classCallCheck from '@babel/runtime/helpers/classCallCheck';
      ╵                             ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

 > node_modules/amplitude-js/amplitude.esm.js:7:25: error: Could not resolve "@babel/runtime/helpers/createClass" (mark it as external to exclude it from the bundle)
    7 │ import _createClass from '@babel/runtime/helpers/createClass';
      ╵                          ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

6 errors
child_process.js:800
    throw err;
    ^

Error: Command failed: /home/adam/amplitude-esbuild/node_modules/esbuild-linux-64/bin/esbuild --bundle index.js
    at checkExecSyncError (child_process.js:760:11)
    at Object.execFileSync (child_process.js:797:15)
    at Object.<anonymous> (/home/adam/amplitude-esbuild/node_modules/esbuild/bin/esbuild:108:26)
    at Module._compile (internal/modules/cjs/loader.js:1072:14)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1101:10)
    at Module.load (internal/modules/cjs/loader.js:937:32)
    at Function.Module._load (internal/modules/cjs/loader.js:778:12)
    at Function.executeUserEntryPoint [as runMain] (internal/modules/run_main.js:76:12)
    at internal/main/run_main_module.js:17:47 {
  status: 1,
  signal: null,
  output: [ null, null, null ],
  pid: 564457,
  stdout: null,
  stderr: null
}
error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```

Runnng
```
yarn add @babel/runtime
```
adds babel runtime and things build ok.
