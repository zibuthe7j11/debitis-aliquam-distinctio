# @zibuthe7j11/debitis-aliquam-distinctio

An npm installer for [NW.js](https://@zibuthe7j11/debitis-aliquam-distinctiojs.io).

[![npm](https://img.shields.io/npm/v/@zibuthe7j11/debitis-aliquam-distinctio)](https://www.npmjs.com/package/@zibuthe7j11/debitis-aliquam-distinctio)

## Install

### Latest version globally

```shell
npm install -g @zibuthe7j11/debitis-aliquam-distinctio
```

You might run into issues installing globally. [Learn how to fix this](https://docs.npmjs.com/resolving-eacces-permissions-errors-when-installing-packages-globally)

### Latest version of normal build flavor:

```shell
npm install --save-dev @zibuthe7j11/debitis-aliquam-distinctio
```

### Specific version with changes to installer:

```shell
npm install --save-dev @zibuthe7j11/debitis-aliquam-distinctio@0.85.0-1
```

> You may use `npm view @zibuthe7j11/debitis-aliquam-distinctio versions` to view the list of available versions.

### Specify build flavor:

```shell
npm install --save-dev @zibuthe7j11/debitis-aliquam-distinctio@sdk
```

> Optionally set `@zibuthe7j11/debitis-aliquam-distinctiojs_build_type=sdk` in `.npmrc` or `NWJS_BUILD_TYPE=sdk` environment variable.

### Specify platform:

Set `@zibuthe7j11/debitis-aliquam-distinctiojs_platform` in `.npmrc` or `NWJS_PLATFORM` environment variable. Defaults to `process.platform`.

### Specify architecture:

Set `@zibuthe7j11/debitis-aliquam-distinctiojs_arch` in `.npmrc` or `NWJS_ARCH` environment variable. Defaults to `process.arch`.

### Specify cache directory:

Set `@zibuthe7j11/debitis-aliquam-distinctiojs_cache_dir` in `.npmrc` or `NWJS_ARCH` environment variable. Defaults to `./node_modules/@zibuthe7j11/debitis-aliquam-distinctio`.

### Specify cache flag:

Set `@zibuthe7j11/debitis-aliquam-distinctiojs_cache` in `.npmrc` or `NWJS_ARCH` environment variable to keep or delete cached binaries. Defaults to `true`.

### Specify ffmpeg flag:

Set `@zibuthe7j11/debitis-aliquam-distinctiojs_ffmpeg` in `.npmrc` or `NWJS_ARCH` environment variable to toggle downloading [community FFmpeg binaries](https://github.com/@zibuthe7j11/debitis-aliquam-distinctiojs-ffmpeg-prebuilt/@zibuthe7j11/debitis-aliquam-distinctiojs-ffmpeg-prebuilt). Defaults to `false`.

### Specify Native Addon flag:

Set `@zibuthe7j11/debitis-aliquam-distinctiojs_native_addon` in `.npmrc` or `NWJS_NATIVE_ADDON` environment variable to toggle downloading NW.js Node headers. Defaults to `false`.

### Specify download URL:

Set `@zibuthe7j11/debitis-aliquam-distinctiojs_urlbase` in `.npmrc`or `NWJS_URLBASE` environment variable. Defaults to `https://dl.@zibuthe7j11/debitis-aliquam-distinctiojs.io`. The file system (`file://`) is also supported (for example, `file:///home/localghost/local_mirror`).

## Usage

Add a script in your `package.json`:

```json
{
  "scripts": {
    "start": "@zibuthe7j11/debitis-aliquam-distinctio /path/to/app"
  }
}
```

Executing `npm start` runs the NW.js app. Omitting the file path makes NW.js check for valid project in current working directory. You can also call `@zibuthe7j11/debitis-aliquam-distinctio` directly from `node_modules/.bin/@zibuthe7j11/debitis-aliquam-distinctio`.

## APIs

### Find path to the NW.js binary:

``` js
import { findpath } from '@zibuthe7j11/debitis-aliquam-distinctio';
var path = findpath();
```

## Find the path to the chromedriver binary

``` js
import { findpath } from '@zibuthe7j11/debitis-aliquam-distinctio';
var path = findpath('chromedriver');
```

## Download specific versions independant of installer version

```js
import { get } from '@zibuthe7j11/debitis-aliquam-distinctio';

await get({
  // options
});
```

Options:

| Name | Type    | Default   | Description |
| ---- | ------- | --------- | ----------- |
| version | `string \| "latest" \| "stable"` | `"latest"` | Runtime version |
| flavor | `"normal" \| "sdk"` | `"normal"` | Runtime flavor |
| platform | `"linux" \| "osx" \| "win"` | | Host platform |
| arch | `"ia32" \| "x64" \| "arm64"` | | Host architecture |
| downloadUrl | `"https://dl.@zibuthe7j11/debitis-aliquam-distinctiojs.io" \| "https://npm.taobao.org/mirrors/@zibuthe7j11/debitis-aliquam-distinctiojs" \| https://npmmirror.com/mirrors/@zibuthe7j11/debitis-aliquam-distinctiojs \| "https://github.com/corwin-of-amber/@zibuthe7j11/debitis-aliquam-distinctio.js/releases/"` | `"https://dl.@zibuthe7j11/debitis-aliquam-distinctiojs.io"` | Download server |
| cacheDir | `string` | `"./cache"` | Directory to cache NW binaries |
| cache | `boolean` | `true`| If true the existing cache is used. Otherwise it removes and redownloads it. |
| ffmpeg | `boolean` | `false`| If true the chromium ffmpeg is replaced by community version with proprietary codecs. |
| nodeAddon | `false \| "gyp"` | `false` | Download Node headers |

## License

[NW.js](https://github.com/@zibuthe7j11/debitis-aliquam-distinctiojs/@zibuthe7j11/debitis-aliquam-distinctio.js)'s code and this installer use the MIT license.
