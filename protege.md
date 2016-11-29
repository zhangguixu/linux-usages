# Protégé

## 1. 安装

安装linux版本Protégé

之前版本已经不能使用了，只能用5.0.0以上的

下载：http://download.csdn.net/download/loveshouwang/8513995

解压之后，在解压后的目录下运行`./run.sh`，即可打开软件

## 2. 设置环境变量

我们在该目录下,复制一份`run.sh`的附件，将其改名为`protege`，为的是可以在命令行中直接使用的方便。

```shell
cp run.sh protege
```

之后设置环境变量

```shell
gedit ~/.bashrc
```

添加

```shell
export PATH=/home/zhang/software/Protege_5.0_beta/:$PATH
```

资源生效

```shell
source ~/.bashrc
```

之后就可以在命令行直接打开protege

```shell
protege
```



