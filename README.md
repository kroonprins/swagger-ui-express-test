```
node run.js
```
=> ok

```
node --experimental-modules --es-module-specifier-resolution=node run.mjs
```
=> ko, error:

```
(node:28397) ExperimentalWarning: The ESM module loader is experimental.
internal/modules/esm/default_resolve.js:59
  let url = moduleWrapResolve(specifier, parentURL);
            ^

Error: Cannot find module '/tmp/swagger-ui-express-test/node_modules/swagger-ui-express/lib/index.js' imported from /tmp/swagger-ui-express-test/app.mjs
    at Loader.resolve [as _resolve] (internal/modules/esm/default_resolve.js:59:13)
    at Loader.resolve (internal/modules/esm/loader.js:70:33)
    at Loader.getModuleJob (internal/modules/esm/loader.js:143:40)
    at ModuleWrap.<anonymous> (internal/modules/esm/module_job.js:43:40)
    at link (internal/modules/esm/module_job.js:42:36) {
  code: 'ERR_MODULE_NOT_FOUND'
}
```