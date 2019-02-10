
# nrm

一、nrm是什么？
这是官方的原话：

　　开发的npm registry 管理工具 nrm, 能够查看和切换当前使用的registry。

顾名思义，就是说nrm是一个管理npm的工具。

二、nrm的安装
$ npm install -g nrm

三、nrm命令
$ nrm ls　　// 查看所有的支持源（有*号的表示当前所使用的源,以下[name]表示源的名称）

$ nrm use [name]　　// 将npm下载源切换成指定的源

$ nrm add        // 使用 add 添加仓库

$ nrm del        // 使用 del 可以删除仓库

$ nrm help　　// 查看nrm帮助

$ nrm home [name]　　// 跳转到指定源的官网
# ===================================================



# egg-msg-flash

[![NPM version][npm-image]][npm-url]
[![build status][travis-image]][travis-url]
[![Test coverage][codecov-image]][codecov-url]
[![David deps][david-image]][david-url]
[![Known Vulnerabilities][snyk-image]][snyk-url]
[![npm download][download-image]][download-url]

[npm-image]: https://img.shields.io/npm/v/egg-msg-flash.svg?style=flat-square
[npm-url]: https://npmjs.org/package/egg-msg-flash
[travis-image]: https://img.shields.io/travis/eggjs/egg-msg-flash.svg?style=flat-square
[travis-url]: https://travis-ci.org/eggjs/egg-msg-flash
[codecov-image]: https://img.shields.io/codecov/c/github/eggjs/egg-msg-flash.svg?style=flat-square
[codecov-url]: https://codecov.io/github/eggjs/egg-msg-flash?branch=master
[david-image]: https://img.shields.io/david/eggjs/egg-msg-flash.svg?style=flat-square
[david-url]: https://david-dm.org/eggjs/egg-msg-flash
[snyk-image]: https://snyk.io/test/npm/egg-msg-flash/badge.svg?style=flat-square
[snyk-url]: https://snyk.io/test/npm/egg-msg-flash
[download-image]: https://img.shields.io/npm/dm/egg-msg-flash.svg?style=flat-square
[download-url]: https://npmjs.org/package/egg-msg-flash

git remote add origin https://github.com/JackYang3567/-egg-msg-flash.git
git push -u origin master
<!--
Description here.
-->

## Install

```bash
$ npm i egg-msg-flash --save
```

## Usage

```js
// {app_root}/config/plugin.js
exports.flash = {
  enable: true,
  package: 'egg-msg-flash',
};
```

## Configuration

```js
// {app_root}/config/config.default.js
exports.flash = {
};
```

see [config/config.default.js](config/config.default.js) for more detail.

## Example

<!-- example here -->
```
ctx.flash = {
  type: 'success',
  message: {
    some: 'one'
  }
}

// or

ctx.flash_success({some:'one})

ctx.flash_error()
ctx.flash_info()
ctx.flash_warning()

ctx.request.flash(type, message)

// get flash by

ctx.flash
```

## Questions & Suggestions

Please open an issue [here](https://github.com/eggjs/egg/issues).

## License

[MIT](LICENSE)
