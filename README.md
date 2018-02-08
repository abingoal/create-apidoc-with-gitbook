# 介绍

> 使用 gitbook 创建 api 文档

## 安装

**要求环境**

* NodoJS (推荐 4.0 以上版本)
* Windows，Linux，Unix 或者 Mac OS(X 以上)

**通过 NPM 安装**

```bash
$ (sudo) npm install gitbook-cli -g
```

如果提示权限不足，加上`sudo`重新执行上面的命令。

**创建文档**

```bash
$ gitbook init
```

如果自定义目录创建，可以执行`gitbook init ./directory`

或者在自己创建好的目录下直接执行初始化命令来创建文档。

**预览文档**

```bash
$ gitbook serve
```

执行上面的命令来预览文档，并且支持实时刷新。

**构建发布**

```bash
$ gitbook build
```

执行命令后会在根目录下生成`_book`文件夹，里面是已经编译好的静态 html 文件，可直接发布在服务器上，至于部署方式，可自由选择。

**调试**

可以使用`--log=debug` 和`--debug`选项来显示调试信息。

```bash
$ gitbook build ./ --log=debug --debug
```

## 目录

```bash
.
├── book.json
├── README.md
├── SUMMARY.md
├── api-1/
|   ├── README.md
|   └── something.md
└── api-2/
    ├── README.md
    └── something.md
```

SUMMARY.md 中列出的所有文档最后都会被转换为 html 文件。

**文档结构简单介绍**

| 文件          | 描述                                     |
| ------------- | ---------------------------------------- |
| `book.json`   | 文档生成[配置](#config) data (**可选**)  |
| `README.md`   | 前言或介绍 (**必选**)                    |
| `SUMMARY.md`  | 目录 (参考 [Pages](pages.md)) (**可选**) |
| `GLOSSARY.md` | 词汇/术语列表（请参阅词汇表)(**可选**)   |

如果需要子目录的话，可以这样设置目录

```bash
.
├── book.json
└── docs/
    ├── README.md
    └── SUMMARY.md
```

然后在`book.json`中添加以下配置:

```json
{
  "root": "./docs"
}
```

## 配置文件

使用配置文件 book.json 来自定义文档。

**以下是常用设置:**

| 变量          | 描述                                                                                             |
| ------------- | ------------------------------------------------------------------------------------------------ |
| `root`        | 除`book.json`文件之外的文档目录                                                                  |
| `structure`   | 指定 Readme, Summary, Glossary 的目录                                                            |
| `title`       | 标题，默认读取 README 中的                                                                       |
| `description` | 描述                                                                                             |
| `author`      | 作者名                                                                                           |
| `isbn`        | 书籍 ISBN                                                                                        |
| `language`    | 本书的语言的[ISO code](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) 代码，默认值是`en` |
| `direction`   | 文本的方向。可以是`rtl`或`ltr`，默认值取决于`language`的值                                       |
| `gitbook`     | 应该使用的 GitBook 版本。使用[SemVer](http://semver.org)规范，例如`“> = 3.0.0”`                  |

**插件**

插件及其配置在`book.json`中指定，详细信息请查看[官方文档](https://github.com/GitbookIO/gitbook/blob/master/docs/plugins/README.md)

3.0.0 版本之后支持自定义主题，该部分同样在[官方文档](https://github.com/GitbookIO/gitbook/blob/master/docs/themes/README.md)查看

配置好之后需要执行`gitbook install` 来安装。

## 生成 eBook 和 PDF 文档

生成的电子书支持 ePub，Mobi，PDF

**安装 ebook-convert**

```
# 生成DPF
$ gitbook pdf ./ ./mybook.pdf

# 生成ePub
$ gitbook epub ./ ./mybook.epub

# 生成Mobi
$ gitbook mobi ./ ./mybook.mobi
```

生成 PDF 的详细配置可以[参考](https://github.com/GitbookIO/gitbook/blob/master/docs/config.md)

**封面**
需要插件实现，[参考](https://plugins.gitbook.com/plugin/autocover)
