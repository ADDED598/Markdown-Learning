# Markdown & VSCode  

> 文章内涉及一些超链接网页，如有侵权请联系我。

**Table of Contents**

- [Markdown & VSCode](#markdown--vscode)
- [前言](#%E5%89%8D%E8%A8%80)
- [现实需求](#%E7%8E%B0%E5%AE%9E%E9%9C%80%E6%B1%82)
- [学习归档](#%E5%AD%A6%E4%B9%A0%E5%BD%92%E6%A1%A3)
  - [安装Markdown](#%E5%AE%89%E8%A3%85markdown)
  - [语法](#%E8%AF%AD%E6%B3%95)
    - [标题](#%E6%A0%87%E9%A2%98)
    - [段落&换行](#%E6%AE%B5%E8%90%BD%E6%8D%A2%E8%A1%8C)
    - [字体](#%E5%AD%97%E4%BD%93)
    - [引用](#%E5%BC%95%E7%94%A8)
    - [列表](#%E5%88%97%E8%A1%A8)
    - [代码块](#%E4%BB%A3%E7%A0%81%E5%9D%97)
    - [分割线](#%E5%88%86%E5%89%B2%E7%BA%BF)
    - [超链接](#%E8%B6%85%E9%93%BE%E6%8E%A5)
    - [图片](#%E5%9B%BE%E7%89%87)
    - [转义字符](#%E8%BD%AC%E4%B9%89%E5%AD%97%E7%AC%A6)
    - [内嵌HTML标签](#%E5%86%85%E5%B5%8Chtml%E6%A0%87%E7%AD%BE)
    - [表格](#%E8%A1%A8%E6%A0%BC)
    - [Emoji](#emoji)
  - [目录生成](#%E7%9B%AE%E5%BD%95%E7%94%9F%E6%88%90)
  - [注意事项](#%E6%B3%A8%E6%84%8F%E4%BA%8B%E9%A1%B9)
  - [需求复现](#%E9%9C%80%E6%B1%82%E5%A4%8D%E7%8E%B0)

# 前言
> 今天系统学习了一下Markdown的语法，我也用我自己好理解的方式给大家讲述一下md这个语言。
>
> 注：以下操作均在VSCode编辑器中完成。

首先给大家简介一下Markdown：

    Markdown在我看来是一种简易的语言，用于包括但不限于文档、文章、朋友圈等有关文字的写作工作

    据我了解，Markdown不只可以用于本地文章的编写，也可以将md文件上传到服务器上显示在网页中，代表框架有VuePress，这可以使我们快速地搭建一个以文章为主的网站。

在我们学习计算机的人看来，它称得上一种计算机语言，因为它是使用标签(markdown)设置文章的外观，这会让其他人觉得计算机语言定是生涩难懂而放弃，但并不是这样的。  

    Markdown适合80%的普通人(这里指的是除计算机工作者之外的人)来写文章。在我看来，它可以让我们专注于文章内容框架的组织，例如使用标题标签(#、##、##，分别代表一级标题、二级标题、三级标题)、引言标签(>)、代码标签(制表符或者```cpp xxx ```)。当你开始使用Markdown，你就会有深刻的体会。
    下面请跟着我的脚步了解并快速入门Markdown吧！  

> 我的学习资源来自[Markdown官方文档](https://markdown.com.cn/)，大家也可以结合着进行学习。

# 现实需求
比如你现在有一个需求：使用Markdown做出超链接中的效果  
http://www.added.icu/docs/c%e8%89%b9%e5%9f%ba%e7%a1%8099%e9%a2%98/  

我们将需求分解为如下几点：
1. 标题
2. 目录
3. 列表(有序、无序)
4. 超链接
5. 引言
6. 图片
7. 代码块

就只有这些需求了对吧，其实他们实现起来也是非常简单的，带着你的疑问，让我们开始下面的学习。

# 学习归档
## 安装Markdown
- 安装VSCode编辑器  
官网 https://code.visualstudio.com/
- 编写第一个Markdown程序
```cpp
# Hello Markdown!
```
**渲染效果如下：**  
# Hello Markdown!

## 语法
> 注：各种标签可以嵌套使用

### 标题  
```cpp
`# 一级标题`  
`## 二级标题`  
`### 三级标题`  
`#### 四级标题`  
`##### 五级标题`  
`###### 六级标题`
```  

**渲染效果如下：**  

# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题

### 段落&换行  
- `在前一行后添加两个及以上的空格+回车`  
- `使用两次回车增加空行换行`  
- `使用<br>标签换行(我不喜欢这种方式)`
```cpp
: what?

: you jump<br>
: i jump
```
**渲染效果如下：**  
: what?

: you jump<br>
: i jump

### 字体  
```cpp
`**粗体文字(推荐)**`  
`__粗体文字__`  
`*斜体文字(推荐)*`  
`_斜体文字_`  
`***粗斜体文字(推荐)***`  
`***___粗斜体文字____***`  
```
    
**渲染效果如下：**  

**粗体文字(推荐)**  
__粗体文字__  
*斜体文字(推荐)*  
_斜体文字_  
***粗斜体文字(推荐)***  
***___粗斜体文字____***

### 引用  
```cpp
`> 这是一段引用`  
`> 推荐使用`  
    `> `  
    `> 多行引用`
`> 多行嵌套`  
    `>> 多行嵌套`
```

**渲染效果如下：**  
> 这是一段引用  

> 推荐使用
> 
> 多行引用  

> 引用嵌套
>> 引用嵌套

### 列表  
```cpp
1. 有序列表
2. 有序列表
3. 有序列表
- 无序列表
- 无序列表
- 无序列表
```
**渲染效果如下：**  
1. 有序列表
2. 有序列表
3. 有序列表
- 无序列表
- 无序列表
- 无序列表

### 代码块
- `使用Tab缩进`
- `使用```cpp ``` `
````cpp
    <html>
        <head>
        </head>
    </html>

```cpp
<html>
    <head>
    </head>
</html>
```
```` 
**渲染效果如下：**  
    `<html>  
        <head>  
        </head>  
    </html>`

```cpp
<html>
    <head>
    </head>
</html>
```

### 分割线
- `-------------`

**渲染效果如下：**

-------------

注：需在分割线前后增加空白行，防止分割线被解析成标题。

### 超链接
- `链接[这是个链接](http://www.added.icu "我的博客网站")`  
- <http://www.added.icu>
- http://www.added.icu
- [引用链接][1]  
    [1]:http://www.added.icu  

**渲染效果如下：**  

链接 [这是个链接](http//:www.added.icu "我的博客网站")
<http://www.added.icu>
http://www.added.icu   
[引用链接][1]  
[1]:http://www.added.icu

### 图片
- `![图片](http://8.210.124.175/wp-content/uploads/2023/02/Snipaste_2023-02-20_21-21-59.png 这是个图片)`

**渲染效果如下：**  
    ![图片](http://8.210.124.175/wp-content/uploads/2023/02/Snipaste_2023-02-20_21-21-59.png "这是个图片")

### 转义字符
使用较少，参考该链接<https://markdown.com.cn/basic-syntax/escaping-characters.html>

### 内嵌HTML标签
使用较少，参考该链接<https://markdown.com.cn/basic-syntax/htmls.html>

### 表格
`| Markdown语法 | 预览效果 | 测试语法 |`  
`| :--- | :---: | ---: ||`  
`| **加粗** | `**加粗**` | 加粗 |` 

**渲染效果如下：**  
| Markdown语法 | 预览效果 | 测试语法 |
| :--- | :---: | ---: |
| `**加粗**` | **加粗** | 加粗 |
| 左对齐 | 居中对齐 | 右对齐 |

### Emoji
- 如果没有下载插件，无法在VScode中使用Emoji表情
- 插件为：Markdown Emoji

**渲染效果如下：**  

:joy: :tent:


## 目录生成
- 安装node  
https://nodejs.org/en
- 下载doctoc插件  
https://www.jianshu.com/p/b0a18eb32d09  
遇到的问题：  
https://blog.csdn.net/yuan2019035055/article/details/128401965
- 使用命令生成目录  
    ```cpp
    doctoc markdown学习.md
    ```
> 目录生成后会出现在文章的最上方。  
> 目录本质上是超链接，我们也可以根据需要修改目录，实现自己的需求。

## 注意事项
我在使用Markdown期间遇到很多语法重叠导致出错的问题，下面采用一问一答的方式进行总结：  

> Q: 如何在代码块中写三个反引号类的语法？  
> A：可以将代码块语法的三个反引号改为四个反引号  


    ````cpp  
        ```cpp
        #include<bits/stdc++.h>  
        ```  
    ````    


## 需求复现
> 下面是我网页的Markdown源码，大家可以互相学习借鉴一下。  
> 大家最好把源码复制到自己的VSCode或者其他Markdown编辑器中，显示会好一些。  

**算法学习.md**  
````Markdown
<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [算法学习](#%E7%AE%97%E6%B3%95%E5%AD%A6%E4%B9%A0)
  - [题目归纳](#%E9%A2%98%E7%9B%AE%E5%BD%92%E7%BA%B3)
  - [题目总结](#%E9%A2%98%E7%9B%AE%E6%80%BB%E7%BB%93)
    - [第一题](#%E7%AC%AC%E4%B8%80%E9%A2%98)
    - [第二题](#%E7%AC%AC%E4%BA%8C%E9%A2%98)
    - [第三题](#%E7%AC%AC%E4%B8%89%E9%A2%98)
    - [第四题](#%E7%AC%AC%E5%9B%9B%E9%A2%98)
    - [第五题](#%E7%AC%AC%E4%BA%94%E9%A2%98)
    - [第六题](#%E7%AC%AC%E5%85%AD%E9%A2%98)
    - [第七题](#%E7%AC%AC%E4%B8%83%E9%A2%98)
    - [第八题](#%E7%AC%AC%E5%85%AB%E9%A2%98)
    - [第九题](#%E7%AC%AC%E4%B9%9D%E9%A2%98)
    - [第十题](#%E7%AC%AC%E5%8D%81%E9%A2%98)
    - [第十一题](#%E7%AC%AC%E5%8D%81%E4%B8%80%E9%A2%98)
    - [第十二题](#%E7%AC%AC%E5%8D%81%E4%BA%8C%E9%A2%98)
    - [第十三题](#%E7%AC%AC%E5%8D%81%E4%B8%89%E9%A2%98)
    - [第十四题](#%E7%AC%AC%E5%8D%81%E5%9B%9B%E9%A2%98)
    - [第十五题](#%E7%AC%AC%E5%8D%81%E4%BA%94%E9%A2%98)
    - [第十六题](#%E7%AC%AC%E5%8D%81%E5%85%AD%E9%A2%98)
    - [第十七题](#%E7%AC%AC%E5%8D%81%E4%B8%83%E9%A2%98)
    - [第十八题](#%E7%AC%AC%E5%8D%81%E5%85%AB%E9%A2%98)
    - [第十九题](#%E7%AC%AC%E5%8D%81%E4%B9%9D%E9%A2%98)
    - [第二十题](#%E7%AC%AC%E4%BA%8C%E5%8D%81%E9%A2%98)
    - [第二十一题](#%E7%AC%AC%E4%BA%8C%E5%8D%81%E4%B8%80%E9%A2%98)
    - [第二十二题 | 第二十三题](#%E7%AC%AC%E4%BA%8C%E5%8D%81%E4%BA%8C%E9%A2%98--%E7%AC%AC%E4%BA%8C%E5%8D%81%E4%B8%89%E9%A2%98)
    - [第二十四题 | 第二十五题](#%E7%AC%AC%E4%BA%8C%E5%8D%81%E5%9B%9B%E9%A2%98--%E7%AC%AC%E4%BA%8C%E5%8D%81%E4%BA%94%E9%A2%98)
    - [第二十六题](#%E7%AC%AC%E4%BA%8C%E5%8D%81%E5%85%AD%E9%A2%98)
    - [第二十七题（可以直接使用循环，也可以使用堆）](#%E7%AC%AC%E4%BA%8C%E5%8D%81%E4%B8%83%E9%A2%98%E5%8F%AF%E4%BB%A5%E7%9B%B4%E6%8E%A5%E4%BD%BF%E7%94%A8%E5%BE%AA%E7%8E%AF%E4%B9%9F%E5%8F%AF%E4%BB%A5%E4%BD%BF%E7%94%A8%E5%A0%86)
    - [第二十八题](#%E7%AC%AC%E4%BA%8C%E5%8D%81%E5%85%AB%E9%A2%98)
    - [第二十九题](#%E7%AC%AC%E4%BA%8C%E5%8D%81%E4%B9%9D%E9%A2%98)
    - [第三十题](#%E7%AC%AC%E4%B8%89%E5%8D%81%E9%A2%98)
    - [第三十一题](#%E7%AC%AC%E4%B8%89%E5%8D%81%E4%B8%80%E9%A2%98)
    - [第三十二题](#%E7%AC%AC%E4%B8%89%E5%8D%81%E4%BA%8C%E9%A2%98)
    - [第三十三题](#%E7%AC%AC%E4%B8%89%E5%8D%81%E4%B8%89%E9%A2%98)
    - [第三十四题](#%E7%AC%AC%E4%B8%89%E5%8D%81%E5%9B%9B%E9%A2%98)
    - [第三十五题](#%E7%AC%AC%E4%B8%89%E5%8D%81%E4%BA%94%E9%A2%98)
    - [第三十六题](#%E7%AC%AC%E4%B8%89%E5%8D%81%E5%85%AD%E9%A2%98)
    - [第三十七题](#%E7%AC%AC%E4%B8%89%E5%8D%81%E4%B8%83%E9%A2%98)
    - [**第三十八题 | 第三十九题**](#%E7%AC%AC%E4%B8%89%E5%8D%81%E5%85%AB%E9%A2%98--%E7%AC%AC%E4%B8%89%E5%8D%81%E4%B9%9D%E9%A2%98)
    - [第四十题](#%E7%AC%AC%E5%9B%9B%E5%8D%81%E9%A2%98)
    - [第四十一题 | 第四十二题](#%E7%AC%AC%E5%9B%9B%E5%8D%81%E4%B8%80%E9%A2%98--%E7%AC%AC%E5%9B%9B%E5%8D%81%E4%BA%8C%E9%A2%98)
    - [第四十三题](#%E7%AC%AC%E5%9B%9B%E5%8D%81%E4%B8%89%E9%A2%98)
    - [第四十四题](#%E7%AC%AC%E5%9B%9B%E5%8D%81%E5%9B%9B%E9%A2%98)
    - [第四十五题](#%E7%AC%AC%E5%9B%9B%E5%8D%81%E4%BA%94%E9%A2%98)
    - [第四十六题](#%E7%AC%AC%E5%9B%9B%E5%8D%81%E5%85%AD%E9%A2%98)
    - [第四十七题](#%E7%AC%AC%E5%9B%9B%E5%8D%81%E4%B8%83%E9%A2%98)
    - [第四十八题](#%E7%AC%AC%E5%9B%9B%E5%8D%81%E5%85%AB%E9%A2%98)
    - [第四十九题](#%E7%AC%AC%E5%9B%9B%E5%8D%81%E4%B9%9D%E9%A2%98)
    - [第五十题](#%E7%AC%AC%E4%BA%94%E5%8D%81%E9%A2%98)
    - [第五十一题](#%E7%AC%AC%E4%BA%94%E5%8D%81%E4%B8%80%E9%A2%98)
    - [第五十二题](#%E7%AC%AC%E4%BA%94%E5%8D%81%E4%BA%8C%E9%A2%98)
    - [第五十三题](#%E7%AC%AC%E4%BA%94%E5%8D%81%E4%B8%89%E9%A2%98)
    - [第五十四题](#%E7%AC%AC%E4%BA%94%E5%8D%81%E5%9B%9B%E9%A2%98)
    - [第五十五题](#%E7%AC%AC%E4%BA%94%E5%8D%81%E4%BA%94%E9%A2%98)
    - [第五十六题 | 第五十七题](#%E7%AC%AC%E4%BA%94%E5%8D%81%E5%85%AD%E9%A2%98--%E7%AC%AC%E4%BA%94%E5%8D%81%E4%B8%83%E9%A2%98)
    - [第五十八题](#%E7%AC%AC%E4%BA%94%E5%8D%81%E5%85%AB%E9%A2%98)
    - [第五十九题](#%E7%AC%AC%E4%BA%94%E5%8D%81%E4%B9%9D%E9%A2%98)
    - [第六十题](#%E7%AC%AC%E5%85%AD%E5%8D%81%E9%A2%98)
    - [第六十一题](#%E7%AC%AC%E5%85%AD%E5%8D%81%E4%B8%80%E9%A2%98)
    - [第六十二题](#%E7%AC%AC%E5%85%AD%E5%8D%81%E4%BA%8C%E9%A2%98)
    - [第六十三题](#%E7%AC%AC%E5%85%AD%E5%8D%81%E4%B8%89%E9%A2%98)
    - [第六十四题](#%E7%AC%AC%E5%85%AD%E5%8D%81%E5%9B%9B%E9%A2%98)
    - [第六十五题](#%E7%AC%AC%E5%85%AD%E5%8D%81%E4%BA%94%E9%A2%98)
    - [第六十六题](#%E7%AC%AC%E5%85%AD%E5%8D%81%E5%85%AD%E9%A2%98)
    - [第六十七题](#%E7%AC%AC%E5%85%AD%E5%8D%81%E4%B8%83%E9%A2%98)
    - [第六十八题](#%E7%AC%AC%E5%85%AD%E5%8D%81%E5%85%AB%E9%A2%98)
    - [第六十九题 | 第七十题](#%E7%AC%AC%E5%85%AD%E5%8D%81%E4%B9%9D%E9%A2%98--%E7%AC%AC%E4%B8%83%E5%8D%81%E9%A2%98)
    - [第七十一题](#%E7%AC%AC%E4%B8%83%E5%8D%81%E4%B8%80%E9%A2%98)
    - [第七十二题](#%E7%AC%AC%E4%B8%83%E5%8D%81%E4%BA%8C%E9%A2%98)
    - [第七十三题](#%E7%AC%AC%E4%B8%83%E5%8D%81%E4%B8%89%E9%A2%98)
    - [第七十四题](#%E7%AC%AC%E4%B8%83%E5%8D%81%E5%9B%9B%E9%A2%98)
    - [第七十五题](#%E7%AC%AC%E4%B8%83%E5%8D%81%E4%BA%94%E9%A2%98)
    - [**第七十六题**](#%E7%AC%AC%E4%B8%83%E5%8D%81%E5%85%AD%E9%A2%98)
    - [**第七十七题**](#%E7%AC%AC%E4%B8%83%E5%8D%81%E4%B8%83%E9%A2%98)
    - [第七十八题](#%E7%AC%AC%E4%B8%83%E5%8D%81%E5%85%AB%E9%A2%98)
    - [第七十九题](#%E7%AC%AC%E4%B8%83%E5%8D%81%E4%B9%9D%E9%A2%98)
    - [第八十题](#%E7%AC%AC%E5%85%AB%E5%8D%81%E9%A2%98)
    - [第八十一题](#%E7%AC%AC%E5%85%AB%E5%8D%81%E4%B8%80%E9%A2%98)
    - [第八十二题](#%E7%AC%AC%E5%85%AB%E5%8D%81%E4%BA%8C%E9%A2%98)
    - [第八十三题](#%E7%AC%AC%E5%85%AB%E5%8D%81%E4%B8%89%E9%A2%98)
    - [第八十四题](#%E7%AC%AC%E5%85%AB%E5%8D%81%E5%9B%9B%E9%A2%98)
    - [第八十五题](#%E7%AC%AC%E5%85%AB%E5%8D%81%E4%BA%94%E9%A2%98)
    - [第八十六题](#%E7%AC%AC%E5%85%AB%E5%8D%81%E5%85%AD%E9%A2%98)
    - [第八十七题](#%E7%AC%AC%E5%85%AB%E5%8D%81%E4%B8%83%E9%A2%98)
    - [第八十八题](#%E7%AC%AC%E5%85%AB%E5%8D%81%E5%85%AB%E9%A2%98)
    - [第八十九题](#%E7%AC%AC%E5%85%AB%E5%8D%81%E4%B9%9D%E9%A2%98)
    - [第九十题](#%E7%AC%AC%E4%B9%9D%E5%8D%81%E9%A2%98)
    - [第九十一题](#%E7%AC%AC%E4%B9%9D%E5%8D%81%E4%B8%80%E9%A2%98)
    - [**第九十二题 | 第九十三题**](#%E7%AC%AC%E4%B9%9D%E5%8D%81%E4%BA%8C%E9%A2%98--%E7%AC%AC%E4%B9%9D%E5%8D%81%E4%B8%89%E9%A2%98)
    - [第九十四题 | 第九十五题](#%E7%AC%AC%E4%B9%9D%E5%8D%81%E5%9B%9B%E9%A2%98--%E7%AC%AC%E4%B9%9D%E5%8D%81%E4%BA%94%E9%A2%98)
    - [**第九十六题**](#%E7%AC%AC%E4%B9%9D%E5%8D%81%E5%85%AD%E9%A2%98)
    - [第九十七题](#%E7%AC%AC%E4%B9%9D%E5%8D%81%E4%B8%83%E9%A2%98)
    - [第九十八题](#%E7%AC%AC%E4%B9%9D%E5%8D%81%E5%85%AB%E9%A2%98)
    - [第九十九题](#%E7%AC%AC%E4%B9%9D%E5%8D%81%E4%B9%9D%E9%A2%98)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

> 题目转自B站英雄哪里出来
> [《C++零基础99题》](https://www.bilibili.com/video/BV1da411M798?p=1&amp;vd_source=80f8923966e2343bff0d0ca66d809e40)

# 算法学习
> 学而不思则罔，思而不学则殆。在算法学习这个栏目里，我计划将自己刷过的算法题进行整理归纳、反思总结，整理成解题报告的形式，将所学知识进行反复巩固加深印象。

## 题目归纳
[![链接](http://8.210.124.175/wp-content/uploads/2023/02/Snipaste_2023-02-20_21-21-59.png)](http://8.210.124.175/wp-content/uploads/2023/02/Snipaste_2023-02-20_21-21-59.png)
[**点我进入刷题链接！**](https://l4wo9dnnzr.feishu.cn/mindnotes/bmncnu7zykCgHvjIBmR85CbjMp4#mindmap)

## 题目总结
> 在这里给出我的一个刷题思路：简单题尽快刷过；重复题直接点链接，做一道相当于做了两道题，会很爽；第一遍做选择你最熟悉的方法，过了就好，第二遍第三遍做的时候考虑更加简单的方法，会让你受益良多；不会做没关系，看过答案之后理解思路，不看答案写代码，或者如果你感到心烦意乱，可以先把这道题抄进答题框中，过了以后的几天反复观看记忆这道题，总有一天你会掌握这道题的！

### 第一题
```cpp
return a + b;
```
### 第二题
### 第三题
### 第四题
### 第五题
### 第六题
### 第七题
### 第八题
### 第九题
### 第十题
### 第十一题
### 第十二题
### 第十三题
### 第十四题
### 第十五题
### 第十六题
### 第十七题
### 第十八题
### 第十九题
### 第二十题
### 第二十一题
### 第二十二题 | 第二十三题
```cpp
法一：
int hammingWeight(uint32_t n) {
    int cnt = 0;
    while(n) {
        n = n &amp; (n-1);
        cnt++;
    }
    return cnt;
}

法二：
int hammingWeight(uint32_t n) {
    int cnt = 0;
    while(n) {
        if(n &amp; 1) {
        cnt++;
    }
        n = n &gt;&gt; 1;
    }
    return cnt;
}
```
### 第二十四题 | 第二十五题
    1、异或两个数 可以得到一个数字x和y所有不同的位置
    2、通过上一题计算不同位置的个数
### 第二十六题
### 第二十七题（可以直接使用循环，也可以使用堆）
### 第二十八题
### 第二十九题
### 第三十题
### 第三十一题
### 第三十二题
### 第三十三题
### 第三十四题
### 第三十五题
### 第三十六题
### 第三十七题
### **第三十八题 | 第三十九题**
```cpp
class Solution {
public:
    bool findNumberIn2DArray(vector&lt;vector&lt;int&gt;&gt;&amp; matrix, int target) {
        for(int i = 0 ; i &lt; matrix.size() ; i ++) {
            int l = 0, r = matrix[0].size();
            while(l &lt;= r) {
                int mid = l + (r l) / 2;
                if(matrix[i][mid] &gt; target) {
                    r = mid 1;   
                } else if(matrix[i][mid] &lt; target) {
                    l = mid + 1;
                } else {
                    return true;
                }
            }
        }
        return false;
    }
};
```
### 第四十题
### 第四十一题 | 第四十二题
```cpp
class Solution {
public:
    bool isPalindrome(string s) {
        for(int i = 0 ; i &lt; s.size() ; i ++) {
            if(s[i] &gt;= 'a' &amp;&amp; s[i] &lt;= 'z') {
                s[i] = s[i] 'a' + 'A';
            }
        }

        int l = 0, r = s.size() 1;
        while(l &lt; r) {
            if(!(s[l] &gt;= 'a' &amp;&amp; s[l] &lt;= 'z' || s[l] &gt;= '0' &amp;&amp; s[l] &lt;= '9')) {
                l++;
                continue;
            }

            if(!(s[r] &gt;= 'a' &amp;&amp; s[r] &lt;= 'z' || s[r] &gt;= '0' &amp;&amp; s[r] &lt;= '9')) {
                r--;
                continue;
            }

            if(s[l] != s[r]) {
                return false;
            }

            l++;
            r--;
        }
        return true;
    }
};
```
### 第四十三题
### 第四十四题
### 第四十五题
### 第四十六题
### 第四十七题
### 第四十八题
### 第四十九题
### 第五十题
### 第五十一题
### 第五十二题
```cpp
class RecentCounter {
    queue&lt;int&gt; q;
public:
    RecentCounter() {

    }
    
    int ping(int t) {
        while(!q.empty()) {
            if(t - q.front() &gt; 3000) {
                q.pop();
            } else {
                break;
            }
        }
        q.push(t);
        return q.size();
    }
};
```
### 第五十三题
```cpp
class MovingAverage {
    int s;
    queue&lt;int&gt; q;
    double sum;
public:
    /** Initialize your data structure here. */
    MovingAverage(int size) {
        s = size;
    }
    
    double next(int val) {
        if(q.size() &gt;= s) {
            sum -= q.front();
            q.pop();
        }
        sum += val;
        q.push(val);
        return sum / q.size();

    }
};
```
### 第五十四题
### 第五十五题
### 第五十六题 | 第五十七题
    这两道题完全一样，和五十五题有所不同
    这两道题求的是平方值，mid的最终值应当是这样的mid * mid &lt;= target，
    而第五十五题找的ans应当是一个大于等于nums[mid]的值，
    两道题在条件判断处的语句是有所不同的
### 第五十八题
### 第五十九题
### 第六十题
### 第六十一题
```cpp
class Solution {
public:
    int uniquePaths(int m, int n) {
        int a[110][110];
        int i, j;
        for(i = 1 ; i &lt;= m ; i ++) {
            for(j = 1 ; j &lt;= n ; j ++) {
                if(i == 1 &amp;&amp; j == 1) {
                    a[i][j] = 1;
                } else if(i == 1) {
                    a[i][j] = a[i][j-1];
                } else if(j == 1) {
                    a[i][j] = a[i-1][j];
                } else {
                    a[i][j] = a[i-1][j] + a[i][j-1];
                }
            }
        }
        return a[m][n];
    }
};
```
### 第六十二题
### 第六十三题
### 第六十四题
### 第六十五题
### 第六十六题
### 第六十七题
### 第六十八题
### 第六十九题 | 第七十题
```cpp
class Solution {
    int f[1010];
public:
    int minCostClimbingStairs(vector&lt;int&gt;&amp; cost) {
        f[0] = 0;
        f[1] = 0;        
        for(int i = 2 ; i &lt;= cost.size() ; i ++) {
            f[i] = min(f[i-1]+cost[i-1], f[i-2]+cost[i-2]);
        }
        return f[cost.size()];
    }
};
```
### 第七十一题
### 第七十二题
### 第七十三题
```cpp
int f[110];
int sum = 0;
for(int j = 0 ; j &lt; nums.size() ; j ++) {
    sum += f[nums[j]];
    f[nums[m]]++;
}
return sum;
```
### 第七十四题
### 第七十五题
### **第七十六题**
```cpp
int hash[101];
int ans = 0;
memset(hash, 0, sizeof(hash));
for(int i = 0 ; i &lt; nums.size() ; i ++) {
    int x = nums[i] + k;
    if(x &gt;= 1 &amp;&amp; x &lt;= 100) {
        ans += hash[nums[i]];
    }

    x = nums[i] - k;
    if(x &gt;= 1 &amp;&amp; x &lt;= 100) {
        ans += hash[nums[i]];
    }
    hash[nums[i]]++;
}
return ans;
```
### **第七十七题**
```cpp
class Solution {
public:
    int numSubarraysWithSum(vector&lt;int&gt;&amp; nums, int goal) {
        int hash[60010];
        int i;
        int ans = 0;
        for(i = 1 ; i &lt; nums.size() ; i ++) {
            nums[i] += nums[i-1];
        }
        memset(hash, 0, sizeof(hash));
        hash[goal] = 1;
        for(i = 0 ; i &lt; nums.size() ; i ++) {
            ans += hash[nums[i]];
            hash[nums[i] + goal]++;
        }
        return ans;
    }
};
```
### 第七十八题
### 第七十九题
### 第八十题
### 第八十一题
### 第八十二题
### 第八十三题
### 第八十四题
### 第八十五题
### 第八十六题
```cpp
class Solution {
public:
    int rangeSumBST(TreeNode* root, int low, int high) {
        if(!root) {
            return 0;
        }
        int sum = rangeSumBST(root-&gt;left, low, high) + rangeSumBST(root-&gt;right, low, high);
        if(root-&gt;val &gt;= low &amp;&amp; root-&gt;val &lt;= high) {
            sum += root-&gt;val;
        }
        return sum;
    }
};
```
### 第八十七题
### 第八十八题
### 第八十九题
### 第九十题
### 第九十一题
### **第九十二题 | 第九十三题**
```cpp
class BSTIterator {
    vector&lt;int&gt; ret;
    int idx;

    void dfs(TreeNode* root) {
        if(!root) {
            return ;
        }

        dfs(root-&gt;left);
        ret.push_back(root-&gt;val);
        dfs(root-&gt;right);
    }
public:
    BSTIterator(TreeNode* root) {
        dfs(root);
        idx = -1;
    }
    
    int next() {
        return ret[++idx];
    }
    
    bool hasNext() {
        return idx &lt; (int)ret.size() - 1;
    }
};
```
### 第九十四题 | 第九十五题
### **第九十六题**
```cpp
class MyCalendarThree {
    map&lt;int, int&gt; cnt;
public:
    MyCalendarThree() {
        cnt.clear();
    }
    
    int book(int startTime, int endTime) {
        cnt[startTime]++;
        cnt[endTime]--;
        int sum = 0, maxv = 0;
        for(auto iter = cnt.begin() ; iter != cnt.end() ; iter++) {
            sum += iter-&gt;second;
            maxv = max(maxv, sum);
        }
        return maxv;
    }
};
```
### 第九十七题
```cpp
// unordered_set 集合，
// find(element)方法可以查找集合中是否存在该变量
class Solution {
    unordered_set&lt;ListNode*&gt; headSet;
public:
    ListNode *getIntersectionNode(ListNode *headA, ListNode *headB) {
        while(headA) {
            headSet.insert(headA);
            headA = headA-&gt;next;
        }
        while(headB) {
            if(headSet.find(headB) != headSet.end()) {
                return headB;
            }
            headB = headB-&gt;next;
        }
        return NULL;
    }
};
```
### 第九十八题
```cpp
class KthLargest {
    priority_queue&lt;int, vector&lt;int&gt;, greater&lt;&gt;&gt; q;
    int K;
public:
    KthLargest(int k, vector&lt;int&gt;&amp; nums) {
        K = k;
        for(int i = 0 ; i &lt; nums.size() ; i ++) {
            add(nums[i]);
        }
    }
    
    int add(int val) {
        q.push(val);
        while(q.size() &gt; K) {
            q.pop();
        }
        return q.top();
    }
};
```
### 第九十九题
    若[0,0]==[1,0] || [0,0]==[1,1] return [0,0]
    else return [0,1]  
````
