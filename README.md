> Importing a module compiled with `@babel/preset-env` with
> `useBuiltIns` after a module compiled with `@babel/plugin-runtime`
> does not work.

```
> yarn
> yarn start
yarn run v1.3.2
$ node index.js
/issue-babel-env-runtime/lib-preset-env/dist/index.js:13
regeneratorRuntime.mark(function _callee() {
^

ReferenceError: regeneratorRuntime is not defined
    at Object.<anonymous> (/issue-babel-env-runtime/lib-preset-env/dist/index.js:13:1)
    at Module._compile (module.js:660:30)
    at Object.Module._extensions..js (module.js:671:10)
    at Module.load (module.js:573:32)
    at tryModuleLoad (module.js:513:12)
    at Function.Module._load (module.js:505:3)
    at Module.require (module.js:604:17)
    at require (internal/module.js:11:18)
    at Object.<anonymous> (/issue-babel-env-runtime/index.js:5:1)
    at Module._compile (module.js:660:30)
error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```

Related to https://github.com/facebook/regenerator/issues/337
