# swnpm -- NPM 包源管理工具

### 请允许我吐槽一下，我本来想用 `ncm` 这个名字，但是npm官方包源里已经有这个名字了，然后我用了这个名字，多了一个字母，所以辛苦大家用的时候多敲一个字母了，请多多包涵哟。


`swnpm` 可以帮助你容易的、快速的去切换不同的npm 包源,
目前,收录的包源有: `npm`, `cnpm`, `taobao`, `nj(nodejitsu)`, `rednpm`.

## 如何使用私有的包源去配置管理工具?
在你的工程目录里添加一个 .yarnrc的文件，然后在里面写上:
`registry “http://your.registry”`
或者你把它配置到你的主目录的 .yarnrc里


## 安装

```
$ npm install -g swnpm
```

## 例子
```
$ swnpm ls

* npm -----  https://registry.npmjs.org/
  cnpm ----  http://r.cnpmjs.org/
  taobao --  https://registry.npm.taobao.org/
  nj ------  https://registry.nodejitsu.com/
  rednpm -- http://registry.mirror.cqupt.edu.cn
  skimdb -- https://skimdb.npmjs.com/registry

```

```
$ swnpm use cnpm  //switch registry to cnpm

    Registry has been set to: http://r.cnpmjs.org/

```

## 使用命令的用法

```
Usage: swnpm [options] [command]

  Commands:

    ls                           包源列表
    use <registry>               使用这个包源切换当前的包源
    add <registry> <url> [home]  添加一个包源
    del <registry>               删除一个包源
    home <registry> [browser]    使用可选浏览器打开包源的首页
    test [registry]              显示一个或所有包源的响应时间
    help                         打印本项目的帮助

  Options:

    -h, --help     输出用法信息
    -V, --version  输出版本号
```

## 包源列表

* [npm](https://www.npmjs.org)
* [cnpm](http://cnpmjs.org)
* [nodejitsu](https://www.nodejitsu.com)
* [taobao](http://npm.taobao.org/)
* [rednpm](http://npm.mirror.cqupt.edu.cn)


## 注意事项

当你使用一个其他的包源的时候，你不能使用 `publish` 命令.

## TODO

* 我写的这个包已经在npm官方包源上面了哟。

## LICENSE
MIT
