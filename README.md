# rollup-shader-chunks

Rollup plugin for optimising inline GLSL shaders.

[![NPM version][npm-badge]][npm-url]
[![License][license-badge]][license-url]
[![CI][ci-badge]][ci-url]

## Example

This plugin processes template literals marked with a syntax highlighting and embedded script editing hint.

```glsl
// shaders.js
export const vertex = /* glsl */ `
  void main() {
      gl_Position = mvp * vec4( position, 1.0 );
  }
`;
```

## Install

```sh
npm i rollup-shader-chunks --save-dev
```

## Usage

```js
// rollup.config.js

import { shaderChunks } from 'rollup-shader-chunks';

export default {
  input: 'src/index.js',
  plugins: [
    //... other plugins, preprocessing
    shaderChunks()
    //... other plugins, terser, etc
  ]
  //...other options
};
```

## Defaults

```js
shaderChunks({
  include: [
    // Glob pattern, or array of glob patterns to include
    '**/*.js'
  ],
  exclude: undefined, // Glob pattern, or array of glob patterns to ignore
  enabled: true // Enable or disable the processing of files
});
```

## Scripts

| Action | Command          | Description              |
| ------ | ---------------- | ------------------------ |
| lint   | `npm run lint`   | Run static code analysis |
| format | `npm run format` | Format source files      |

## Tools

| Tool         | Reference                |
| ------------ | ------------------------ |
| Node.js      | https://nodejs.org       |
| rollup.js    | https://rollupjs.org     |
| ESLint       | https://eslint.org       |
| Prettier     | https://prettier.io      |
| EditorConfig | https://editorconfig.org |

## References

| Website | Reference                      |
| ------- | ------------------------------ |
| WebGL2  | https://www.khronos.org/webgl/ |

## License

This project is released under the MIT [License](LICENSE).

[ci-badge]: https://github.com/epreston/rollup-shader-chunks/actions/workflows/ci.yml/badge.svg
[ci-url]: https://github.com/epreston/rollup-shader-chunks/actions
[npm-badge]: https://img.shields.io/npm/v/rollup-shader-chunks
[npm-url]: https://www.npmjs.com/package/rollup-shader-chunks
[license-badge]: https://img.shields.io/npm/l/rollup-shader-chunks.svg
[license-url]: LICENSE
