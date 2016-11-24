# java环境搭建

[下载jdk（tar.gz）](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

解压

```shell
tar -xvf jdkxx.tar.gz
```

配置环境变量，有两种方式

* 系统全局环境变量，放置在/etc/profie(不建议)
* 用户环境变量，放置在~/.bashrc中

打开配置文件

```shell
gedit ~/.bashrc
```

在文件后面添加

```shell
# set java environment
export JAVA_HOME=/home/zhang/software/jdk1.8.0
export JRE_HOME=$JAVA_HOME/jre
export CLASSPATH=$JAVA_HOME/lib:$CLASSPATH
export PATH=$JAVA_HOME/bin:$PATH
```

配置文件生效

```shell
source ~/.bashrc
```
