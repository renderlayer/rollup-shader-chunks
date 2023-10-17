# @renderlayer/rollup-shader-chunks

Rollup plugin for optimising inline GLSL shaders.

[![NPM version][npm-badge]][npm-url]
[![License][license-badge]][license-url]
[![CI][ci-badge]][ci-url]

## Install

```sh
npm i @renderlayer/rollup-shader-chunks --save-dev
```

## Usage

```js
// rollup.config.js

import { shaderChunks } from '@renderlayer/rollup-shader-chunks';

export default {
  input: 'src/index.js',
  plugins: [
    //... other plugins, preprocessing
    shaderChunks(),
    //... other plugins, terser, etc
  ],
  //...other options
}
```

## Defaults

```js
shaderChunks({
  include: [            // Glob pattern, or array of glob patterns to include
    '**/*.js'
  ],
  exclude: undefined,   // Glob pattern, or array of glob patterns to ignore
  enabled: true         // Enable or disable the processing of files
})
```

## Scripts

| Action        | Command                 | Description                        |
| ------------- | ----------------------- | ---------------------------------- |
| lint          | `npm run lint`          | Run static code analysis           |
| format        | `npm run format`        | Check source file formatting       |
| format-fix    | `npm run format-fix`    | Format source files                |

## Tools

| Tool         | Reference                 |
| ------------ | ------------------------- |
| Node.js      | https://nodejs.org/       |
| rollup.js    | https://rollupjs.org      |
| ESLint       | https://eslint.org/       |
| Prettier     | https://prettier.io       |
| EditorConfig | https://editorconfig.org  |

## References

| Website | Reference                          |
| ------- | ---------------------------------- |
| WebGL2  | https://www.khronos.org/webgl/     |

## License

This project is released under the MIT [License](LICENSE).

[ci-badge]: https://github.com/renderlayer/rollup-shader-chunks/actions/workflows/ci.yml/badge.svg
[ci-url]: https://github.com/renderlayer/rollup-shader-chunks/actions
[npm-badge]: https://img.shields.io/npm/v/@renderlayer/rollup-shader-chunks
[npm-url]: https://www.npmjs.com/package/@renderlayer/rollup-shader-chunks
[license-badge]: https://img.shields.io/npm/l/@renderlayer/rollup-shader-chunks.svg?cacheSeconds=2592000
[license-url]: LICENSE
