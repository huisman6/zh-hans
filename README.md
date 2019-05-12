# 文史

## 资料来源

资料来源自：[维基文库](https://zh.wikisource.org/wiki/Wikisource:%E9%A6%96%E9%A1%B5)

本仓库主要负责基于文库生成各种PDF/MOBI格式的书籍。

## 书籍生成

基于Gitbook + Markdwon 来生成电子书籍。

如果需要在本地预览以及生成PDF，则需要安装 Gitboook 和 Calibre Ebook Converter，请参考下文。

### Gitbook

#### 下载 Nodejs

请自行前往官网：https://nodejs.org/zh-cn/download ，下载GA版本，点击安装。

#### 安装 Gitbook

在控制台执行以下命令：

``` shell
npm install gitbook-cli -g
```
有可能速度较慢，建议翻墙(全局代理）。

#### 预览书籍

``` shell
# 首次执行建议安装插件，后面可不执行此行命令
gitbook install
# 启动web服务器，浏览器里访问：http://localhost:4000
gitbook  serve

```

### 生成PDF

GitBook can generates a website, but can also output content as ebook (ePub, Mobi, PDF).

``` shell
# 切换到书籍根目录
# Generate a PDF file
$ gitbook pdf ./ ./文史-长短经-赵蕤.pdf

# Generate an ePub file
$ gitbook epub ./ ./文史-长短经-赵蕤.epub

# Generate a Mobi file
$ gitbook mobi ./ ./文史-长短经-赵蕤.mobi
```

`ebook-convert` is required to generate ebooks (epub, mobi, pdf).


#### 一.下载 ebook-convert

请自行前往官网下载：https://calibre-ebook.com/download 

#### 二. 设置PATH

##### OS X

Download the [Calibre application](https://calibre-ebook.com/download). After moving the `calibre.app` to your Applications folder create a symbolic link to the ebook-convert tool:

``` shell
$ sudo ln -s ~/Applications/calibre.app/Contents/MacOS/ebook-convert /usr/bin
```

You can replace `/usr/bin` with any directory that is in your $PATH.

MacOS 无法创建快捷方式的解决方法请参考：[cannot-create-a-symlink-inside-of-usr-bin-even-as-sudo](https://stackoverflow.com/questions/36730549/cannot-create-a-symlink-inside-of-usr-bin-even-as-sudo)

#### 三. Cover [书籍封面可忽略]

Covers are used for all the ebook formats. You can either provide one yourself, or generate one using the [autocover plugin](https://plugins.gitbook.com/plugin/autocover).

To provide a cover, place a **`cover.jpg`** file at the root directory of your book. Adding a **`cover_small.jpg`** will specify a smaller version of the cover. The cover should be a **JPEG** file.

A good cover should respect the following guidelines:

* Size of 1800x2360 pixels for `cover.jpg`, 200x262 for `cover_small.jpg`
* No border
* Clearly visible book title
* Any important text should be visible in the small version

## 扩展资源

* [常见Logo搜索](https://www.vectorlogo.zone/search.html)
* [常见ICON搜索](http://www.iconfont.cn/search/index?searchType=icon)
