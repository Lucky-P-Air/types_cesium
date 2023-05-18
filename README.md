[![npm](https://img.shields.io/npm/v/@platypii/cesium)](https://www.npmjs.com/package/@platypii/cesium)
[![apache license](https://img.shields.io/badge/License-Apache-blue.svg)](https://opensource.org/licenses/Apache-2.0)

# @types/cesium

Standalone typescript definition file for [Cesium JS](https://github.com/CesiumGS/cesium).

## Why?

Have you seen how large cesium is? I just need the types.

I have a build pipeline with some expensive steps like js minification, and including Cesium makes it really slow (60+ mb). With @platypii/cesium, typescript is happy, and I can just include cesium directly in my webpage without slowing down my build process.

It is also useful to see the diff of the cesium api over time.

## How to use

Add to `package.json`:
```json
{
  "devDependencies": {
    "@Lucky-P-Air/cesium": "^1.105.1",
  }
}
```

Add to `tsconfig.json`:
```json
{
  "compilerOptions": {
    "typeRoots": [
      "node_modules/@types",
      "node_modules/@platypii"
    ]
  }
}
```

## Publishing

```
npm publish
```
