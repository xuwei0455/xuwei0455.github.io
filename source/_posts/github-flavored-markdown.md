---
title: GitHub Flavored Markdown
date: 2017-11-10 16:36:41
tags:
    - Markdown
categories:
    - 标记语言
---

GitHub扩展了Markdown语法，支持了一些很实用的feature，使得渲染出的结果显得更加整洁明了，为了在写作的时候不至于弄混两者的语法，在这里将官方的[文档](https://guides.github.com/features/mastering-markdown/)翻译如下，以供记忆、学习。另外，其实这翻译的只是一个简化版的，详细版的文档在[这里](https://github.github.com/gfm/)。

## GitHub Flavored Markdown
注意有一些语法特性只能在项目描述和Issue/PR的评论中才能够使用。其中包括了@mentions以及对SHA-1哈希，Issues, 和Pull Requests的应用。任务列表只能在Gist评论和Gist Markdown文件中使用。


### 语法高亮

这里有一个使用GitHub Flavored Markdown语法高亮的例子：

```javascript
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```

也可以直接在代码前加上缩进：
``` txt
	function fancyAlert(arg) {
      if(arg) {
        $.facebox({div:'#foo'})
      }
    }
```
	
这里有一个Python代码的语法高亮例子：
``` python
def foo():
    if not bar:
        return True

```
### 任务列表

如果你在Issue的第一条评论里加上一个任务列表，那么你就可以获得一个方便的进度指示器，这个在Pull Requests中同样有效。

```
- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item
```
以上列表会被渲染成：

- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item

### 表格

你可以使用"-"符号分隔每一行，"|"符号来分隔每一列，这样就可以快速的组装成一个表格：
```
First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column
```
会被渲染成:

First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

### SHA引用

所有指向commit的hash值的应用都会被自动转换成一个链接到commit的地址。
```
16c999e8c71134401a78d4d46435517b2271d6ac
mojombo@16c999e8c71134401a78d4d46435517b2271d6ac
mojombo/github-flavored-markdown@16c999e8c71134401a78d4d46435517b2271d6ac
```
### 代码库的Issue引用

所有引用Issue和Pull Request的数字都会被自动转换成为一个链接。
```
#1
mojombo#1
mojombo/github-flavored-markdown#1
```
### 用户@

输入一个"@"符号，紧跟上一个用户名，将自动通知这个用户来查看这条评论。这个语法被称为"@"，因为你提到了这个用户。你也可以使用"@"语法提醒组织内的团队。


### 自动链接至URL

所有URL\(类似http://www.github.com/ )将会自动转换成一个可以点击的地址。


### 删除线

任何被两个"\~~"符号包裹的词会添加上删除线。例如：~~废弃字段~~。


### Emoji

Github 支持emoji!

想要查看支持列表，可以访问[Emoji](http://www.emoji-cheat-sheet.com/)。

