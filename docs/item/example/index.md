---
tags: ['SMHO手册说明', '词条示例']
---

# 词条编辑示例

上面是一级标题

## 这是二级标题

### 这是三级标题

> 这是引用

这是普通文本  
_This is Italic words_  
**这是粗体文本**  
~~这是带删除线的文本~~  
[这是链接（前往首页）]({{ site.baseurl }})  
<span style="color: #ff0000">这是用原生HTML代码实现的彩色文本</span>

这是行内代码：`:(){ :|:& };:`

这是代码块（python）：

```python
x = a if a > 0 else b
```

这是表格：

|第一列|第二列|
|-----|-----|
|甲|乙|

这是LaTeX块状公式：

$$ a + b + c $$

这是LaTeX行内公式：$ a^b $。

这是用HTML实现的输入框：<input type="text" name="test" />

这是图片：

![logo](./images/logo.png)

这是分割线：

-----

以下是此示例的代码（到分割线为止）：

````markdown
---
tags: ['SMHO手册说明']
---

# 词条编辑示例

上面是一级标题

## 这是二级标题

### 这是三级标题

> 这是引用

这是普通文本  
_This is Italic words_  
**这是粗体文本**  
~~这是带删除线的文本~~  
[这是链接（前往首页）]({{ site.baseurl }})  
<span style="color: #ff0000">这是用原生HTML代码实现的彩色文本</span>

这是行内代码：`:(){ :|:& };:`

这是代码块（python）：

```python
x = a if a > 0 else b
```

这是表格：

|第一列|第二列|
|-----|-----|
|甲|乙|

这是LaTeX块状公式：

$$ a + b + c $$

这是LaTeX行内公式：$ a^b $。

这是用HTML实现的输入框：<input type="text" name="test" />

这是图片：

![logo](./images/logo.png)

这是分割线：

-----
````

以下是此词条的文件夹结构（`example`为词条文件夹）：

```
example
   ├── index.md
   └── images
         └──logo.png
```
