---
tags: ['SMHO手册说明']
---

# 编辑规则

## 基本形式

用户编辑SMHO手册上的内容的基本方式为提交“拉取请求”(Pull Request, PR)。关于Pull Request的更多信息可以在GitHub的官方文档（[中文](https://docs.github.com/cn/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/proposing-changes-to-your-work-with-pull-requests)/[英文](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/proposing-changes-to-your-work-with-pull-requests)）上找到。在这里仅进行最简单的概述。

注：以下操作请在登录[GitHub](https://github.com)后再进行。

1. 进入SMHO手册的[代码仓库(repo)](https://github.com/S-M-H-O/handbook)，点击页面右上角的“Fork”，将整个代码仓库复制到您自己的账户中，这个复制得到的仓库称为您的“本地仓库”；
2. 如果您要更改词条内容，可以直接在“本地仓库”中的`/docs/item/`文件夹下的词条文件夹中更改；如果您要增加词条，请将编写好的词条文件夹上传至“本地仓库”中的`/docs/item/`文件夹下；具体更改或上传方法略（请遵循GitHub网页上的按钮提示），编写词条的格式以及词条文件夹的构成见下；
3. 在SMHO手册的代码仓库中提请一个新的PR，请求将“本地仓库”合并到SMHO手册的`main`分支（默认）；
4. 等待审核通过后，您的更改将在SMHO手册中生效。

## 编辑方法

注：以下内容中，标注**(dev)**的是针对开发者的提示，普通用户可以跳过。

### 结构

SMHO手册的词条以文件夹的形式呈现，下面是词条的文件结构图：

```
[词条名称]
    ├── index.md
    └── ...
```

SMHO手册的所有词条都应置于`/docs/item/`文件夹下。

SMHO手册中的词条内容由两部分组成：**正文**和**附件**。其中，附件主要为插图。

### 正文

`index.md`存储的是正文部分，应由markdown语言写成。SMHO手册提供了GitHub风格的markdown语法，关于GitHub风格的markdown的更多信息请参考[官方文档](https://guides.github.com/features/mastering-markdown/)。  
除markdown以外，SMHO手册还提供了基于MathJax的$\LaTeX$（LaTeX，一种数学符号标记语言）支持：MathJax默认支持以`\[...\]`或`$$...$$`包裹的块状行间公式，SMHO手册还支持以`$...$`包裹的行内公式。关于$\LaTeX$的更多信息可以在互联网上找到。  
**(dev)**另外，对于markdown无法表现的内容（如字体、颜色等），可以在markdown文件中直接使用原生的HTML代码。

词条的`index.md`中应有且仅有一个一级（最高级）标题，这个一级标题将被作为此词条的总标题，显示在浏览器上放的标签栏中。如，某词条中含有的唯一一个一级标题为“xxx”，那么用户访问这个词条时标签栏中的标题就会是“xxx \| SMHO手册”。

**(dev)**如果不想使用词条中的一级标题作为总标题（不推荐！），可以在`index.md`的YAML头中加入如下内容：

```yaml
title: 新标题
```

### 标签

您可以为词条添加标签（推荐）。

要给词条增加标签，您需要使用YAML头。在`index.md`文件的头部，增加如下的内容：

```
---
...
---

```

其中，`...`的部分使用YAML语法，为YAML部分。要添加标签，在YAML部分添加（注意把`...`删掉）如下YAML代码：

```yaml
tags: ['标签1', '标签2', ... ]
```

您可以添加任意数量的标签。建议您在添加标签前，先查看已有的标签，以免添加含义相近但名称不同的标签。您可以在[这里]({{ site.baseurl }}/tags.html)查看已有的标签。SMHO手册的标签是大小写敏感的；另外，请注意尽量不要在标签中使用空格（请用连字符`-`或下划线`_`代替）。

**注意：事实上，由于SMHO手册的搜索机制是基于标签的，所以您必须为您的词条添加至少一个标签，否则您的词条将无法被搜索到（但仍然可以通过网址访问）。**

### 附件

词条文件夹中除`index.md`以外的文件都是附件，用户可以自行安排。最简单的形式是在词条文件夹下再建立一个`images`文件夹用于存储图片。  
**(dev)**除图片以外，可能用到的本词条专用的样式表（CSS）或脚本（javascript）都可以放在词条文件夹下。  
需要注意的是，`index.md`中对图片等附件的引用需要与附件的文件结构相一致。比如，需要引用本词条文件夹下的`images`文件夹中的图片`pic.png`，那么在`index.md`中的引用就应是

```markdown
![pic](./images/pic.png)
```

其中，`.`表示词条文件夹（即`index.md`所在的文件夹）。

## 编辑规范

SMHO手册的词条需要遵循一定的规范。

1. 内容必须是真实的、准确的、合法的，请勿上传虚假或非法内容；
2. 结构清晰，由多级标题组成；内容通俗易懂，又不失专业性；
3. 排版美观；

## 结语

SMHO手册提供了一个[词条示例]({{ site.baseurl }}/item/example/)，供参考。

感谢您为SMHO手册做出的伟大贡献！
