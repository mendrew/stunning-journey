# Reproduction of an issue with @size-limit/webpack-css package on version 10.0.1.

## Steps to reproduce
```sh
npm install
npm run size
```

You'll see these error:
```sh
> size-limit-experiment@1.0.0 size
> size-limit --json

{
  "error": "ReferenceError: require is not defined in ES module scope, you can use import instead\nThis file is being treated as an ES module because it has a '.js' file extension and '/Users/andrey.medvedev/src/experiment
/size-limit-experiment/node_modules/@size-limit/webpack-css/package.json' contains \"type\": \"module\". To treat it as a CommonJS script, rename it to use the '.cjs' file extension.\n    at file:///Users/andrey.medvedev/s
rc/experiment/size-limit-experiment/node_modules/@size-limit/webpack-css/index.js:6:9\n    at ModuleJob.run (node:internal/modules/esm/module_job:193:25)\n    at async Promise.all (index 0)\n    at async ESMLoader.import (
node:internal/modules/esm/loader:528:24)\n    at async Promise.all (index 2)\n    at async loadPlugins (file:///Users/andrey.medvedev/src/experiment/size-limit-experiment/node_modules/size-limit/load-plugins.js:24:14)\n
 at async findPlugins (file:///Users/andrey.medvedev/src/experiment/size-limit-experiment/node_modules/size-limit/run.js:28:17)\n    at async default (file:///Users/andrey.medvedev/src/experiment/size-limit-experiment/node_modules/size-limit/run.js:57:19)"
}
```
