# Maven

*需要先安装java环境*

[下载二进制文件tar.gz](http://maven.apache.org/download.cgi)

解压

```shell
tar -xvf apache-maven-xxx.tar.gz
```

配置环境变量，同样有两种方式，我们还是选择修改~/.bashrc

打开文件

```shell
gedit ~/.bashrc
```

在文件后面添加

```shell
# set maven
export M2_HOME=/home/zhang/software/maven
export PATH=$M2_HOME/bin:$PATH
```

## 添加maven国内镜像

在maven的根目录下的conf文件夹下的`setting.xml`文件

```xml
<mirrors>
    <mirror>
      <id>alimaven</id>
      <name>aliyun maven</name>
      <url>http://maven.aliyun.com/nexus/content/groups/public/</url>
      <mirrorOf>central</mirrorOf>        
    </mirror>
  </mirrors>
```