# node环境搭建

方法有很多，使用一种最简单的

[下载二进制包nodeXXX.tar.xz](https://nodejs.org/en/download/)

解压

```shell
tar -Jxv -f nodexxx.tar.xz
```

之后使用软链接的方式，将node和npm放到可执行路径上

```shell
sudo ln -s /home/zhang/software/node/bin/node /usr/local/bin/node
sudo ln -s /home/zhang/software/node/bin/npm /usr/local/bin/npm
```

注意，我们全局安装的模块，放在我们放置node的目录下的lib中的node_modules中

## 安装全局模块

有时候需要全局安装一下构建工具，例如gulp，可以先

```shell
npm install -g gulp
```

安装之后，gulp会放置在你安装node的该文件下的lib/node_modules下，我们可以通过软链接的方式，来创建gulp命令

```shell
sudo ln -s /home/zhang/software/node/lib/node_modules/gulp/bin/gulp.js  /usr/local/bin/gulp
```

其他的也类似。