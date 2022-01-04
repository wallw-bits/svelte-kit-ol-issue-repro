# SvelteKit/OpenLayers Issue Reproduction

## reproduce:
```
npm i
npm run build
```

which produces the error:
```
Error [ERR_MODULE_NOT_FOUND]: Cannot find module '${project}/node_modules/ol/Feature' imported from ${project}/.svelte-kit/output/server/entries/pages/index.svelte.js
Did you mean to import ol/Feature.js?
    at new NodeError (node:internal/errors:371:5)
    at finalizeResolution (node:internal/modules/esm/resolve:416:11)
    at moduleResolve (node:internal/modules/esm/resolve:932:10)
    at defaultResolve (node:internal/modules/esm/resolve:1044:11)
    at ESMLoader.resolve (node:internal/modules/esm/loader:422:30)
    at ESMLoader.getModuleJob (node:internal/modules/esm/loader:222:40)
    at ModuleWrap.<anonymous> (node:internal/modules/esm/module_job:76:40)
    at link (node:internal/modules/esm/module_job:75:36)
> 500 /
Error: 500 /
    at file://${project}/node_modules/@sveltejs/kit/dist/chunks/index5.js:167:11
    at visit (file://${project}/node_modules/@sveltejs/kit/dist/chunks/index5.js:326:5)
```

## recreate from scratch:
```
npm init svelte@next <app>
# skeleton, yes to TS, no to eslint/prettier
cd <app>
npm i
npm i -D ol
# add src/routes/index.svelte
```

