# hexo使用详解

hexo是一款博客网站的构建工具，下面就介绍

1. 在ubuntu下安装的步骤
2. 使用hexo+NexT构建我们的博客站点
3. 部署到github上。

需要先安装[node](node.md)

## 1. 安装

```shell
npm install -g hexo-cli
```

*按照官网的推荐，现在是安装hexo-cli，网上有一些是安装hexo*

## 2. 生成项目

```shell
hexo init <folder>
```

这个命令会：

1. 生成一个hexo的项目
2. 自动安装依赖（即执行npm install）
3. 下载一个默认的主题

### 2.1 目录结构

项目目录结构概览：

```
|- blogs
    - .deploy_git 后面会提供的hexo deploy生成的目录
    - public hexo生成的静态资源文件
    - scaffolds 放置一些模板文件，我们也可以定制自己的模板
        - page.md 生成页面的模板
        - post.md 生成文章的模板
        - draft.md 生成图表的模板
    - source 我们的博客站点源文件，主要是md、html和图片
        - _posts 放置博客源文件的默认目录
        - uploads 自行创建的目录，用于放置图片信息
    - themes 网站的主题，也就是网站的整体样式布局等
    - _config.yml 博客站点的配置文件
    - package.json hexo构建工具依赖
    - db.json hexo生成的网站的描述信息
```

### 2.2 基础配置

在根目录下的`_config.yml`中找到`Site`，配置网站的基本信息

1. title 网站标题
2. subtitle 网站副标题
3. description 描述
4. author 作者
5. language 语言，可以设置中文的`zh-Hans`
6. timezone 时间格式，本人设为`UTC`

### 2.3 常用命令

```shell
# 创建一篇新博客，生成source/_posts/new-post.md
hexo new 'new-post'
# 创建一个新页面，生成source/new-page/index.html
hexo new page 'new-page'

# 清理缓存文件，包括public文件夹和db.son
hexo clean
# 根据配置文件和source下的源文件生成public文件夹和
hexo generate
# 启用一个本地服务器，文件来源是public文件夹下的静态资源
# 访问localhost:4000即可预览
hexo server -s
```

## 3. 配置主题

这里使用的主题是[NexT](http://theme-next.iissnan.com/)，原因是官网的文档指南做的特别好，有什么问题都可以在上面找到答案。

*可以把themes下的主题文件夹删掉，就安装NexT就可以*

1. 下载NexT，在项目的根目录下执行，网络比较慢，可能需要等一段时间

    ```shell
    git clone https://github.com/iissnan/hexo-theme-next themes/next
    ```

2. 下载成功后，可以在themes下看到next，配置根目录下的`_config.yml`，找到`theme`，将其值改为`next`

这个时候，运行以下命令，即可以在浏览器中预览到hexo主题的效果

```shell
hexo clean
hexo generate
hexo server -s
```

## 4. 主题设置

以下配置都在`themes/next/_config.yml`。

### 4.1 主题设置

主题样式设定，NexT提供了三种不同的样式，找到`scheme`来设置不同的样式

* Muse 默认，大量留白
* Mist 单栏
* Pisces 双栏

### 4.2 设置语言

设置`language`为`zh-Hans`

### 4.3 设置网站头像

找到`avatar`，将其值设为`/uploads/avator.jpg`(其他格式也行，)，然后在source/uploads目录下放置我们的头像，重新生成静态资源即可。

### 4.4 设置社交信息

找到`Social Links`设置，例如设置github

```yml
social :
    Github : https://github.com/zhanggguixu
```

注意，对应的图标显示在`social_icons`中

### 4.5 设置友情链接

### 4.6 开启分类、标签、公益404页面

### 4.7 开启多说，以及多说分享

### 4.8 开启站点统计

### 4.9 设置代码主题

### 4.10 SEO设置

### 4.11 网站本地搜索

## 5. 配置github

## 6. 部署

## 7. 同步自己的博客项目

## 8. 参考

1. [hexo](https://hexo.io/docs)
2. [hexo主题](https://www.zhihu.com/question/24422335)
3. [HEXO+Github,搭建属于自己的博客](http://www.jianshu.com/p/465830080ea9)
4. [NexT](http://theme-next.iissnan.com/)