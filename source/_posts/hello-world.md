---
title: Hexo 教程
date: 2017-11-11 11:11:11
tags:
    - Hexo
categories:
	- 工具使用
---
欢迎使用[Hexo](https://hexo.io/)! 这是一篇关于Hexo的简介, 翻译自Hexo的Hello World!

Hexo的文档在[这里](https://hexo.io/docs/),可以直接由文档获取帮助。

如果使用Hexo的时候有其他的问题，可以在如果使用Hexo的时候有其他的问题，可以在 [疑难问题](https://hexo.io/docs/troubleshooting.html)寻求解决方法，或者在[GitHub](https://github.com/hexojs/hexo/issues)上提出问题。

## 快速开始

### 新建一篇文章

``` bash
$ hexo new "My New Post"
```

详细信息: [Writing](https://hexo.io/docs/writing.html)

### 启动本地服务

``` bash
$ hexo server
```

详细信息: [Server](https://hexo.io/docs/server.html)

### 生成静态资源

``` bash
$ hexo generate
```

详细信息: [Generating](https://hexo.io/docs/generating.html)

### 部署到云端

``` bash
$ hexo deploy
```

详细信息: [Deployment](https://hexo.io/docs/deployment.html)

## 部署方案

这里利用不用的git分支，将MarkDown的源文件和生成的静态资源都发布到github。

具体做法是：

1. 将源文件保存在hexo分支
2. 将生成的静态资源放在master分支
3. 在写完文章后，可以使用`hexo server`来预览效果，确认没问题后，直接使用
`hexo generate` && `hexo deploy` 来部署到github，最后`git add` &&
`commit` && `push` 来保存源文件