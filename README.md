#  [![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Dependency Status][daviddm-image]][daviddm-url]

> A deployable express based weixin server


## Install

```sh
$ npm install --g node-weixin-express
```


## Usage

1.查看命令

```sh
$ node-weixin-express --help
```

不需要再写代码，可以直接通过命令执行。

端口port默认是3333,需要配置HTTP代理才能更好的工作
  >如果没有代理服务器，请将port指定为80，以防微信验证无法通过。


1. 作为微信验证服务器


```sh
weixin --token AUTH_YOUR_TOKEN --port 3333
forever start $(which weixin) --token AUTH_YOUR_TOKEN --port 3333
```

启动后微信返回的验证需要指定到：http://YOUR_DOMAIN/weixin/auth/ack


2.作为oauth服务器

```sh
weixin --port 3333 [--port port] [--token token] [--id id] [--secret secret] [--host host]
forever start $(which weixin) --port 3333 [--port port] [--token token] [--id id] [--secret secret] [--host host]
```



## License

MIT © [JSSDKCN](blog.3gcnbeta.com)


[npm-image]: https://badge.fury.io/js/node-weixin-express.svg
[npm-url]: https://npmjs.org/package/node-weixin-express
[travis-image]: https://travis-ci.org/JSSDKCN/node-weixin-express.svg?branch=master
[travis-url]: https://travis-ci.org/JSSDKCN/node-weixin-express
[daviddm-image]: https://david-dm.org/JSSDKCN/node-weixin-express.svg?theme=shields.io
[daviddm-url]: https://david-dm.org/JSSDKCN/node-weixin-express