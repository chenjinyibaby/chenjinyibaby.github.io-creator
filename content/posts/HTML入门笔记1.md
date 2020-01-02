---
title: "HTML入门笔记1"
date: 2020-01-02T21:15:24+08:00
draft: false
---

# 入门笔记
## HTML的起手式
```
<!DOCTYPE html>
<html lang="en">
<head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta http-equiv="X-UA-Compatible" content="ie=edge">
        <title>Document</title>
</head>
<body>

</body>
</html>
```
在上述代码中
1. DOCTYPE 指文档，告诉浏览器我要使用html来写这篇
2. html lang="en"；我所用的语言是英文，可以将en改为zh-CN，表示中文简体
3. head和body元素是子元素，一般不缩进
4. UTF-8为字符编码
5. content="width=device-width" 防止页面缩放，可以兼容手机
6. content="ie=edge" 页面在IE浏览器打开时，请更新到最新的版本。
7. Document可改为文章的标题。
8. meta为自结束标签

## 标签
### 表示文章和书的层级的标签
* h1~h6 标题的大小，和hugo中的#一样的用法
* section 章节
* header 头部内容（顶部）
* footer 底部内容
* p       段落
* main  主要内容
* aside 不是主要的内容
* div 划分区域

### 全局属性（所有的标签都会有的属性）
* class  标签的分类
* contenteditable   表示元素是否可被用户编辑。 如果可以，浏览器会修改元素的部件以允许编辑。
* id 全页面只有唯一元素的id属性，不到万不得已不要用
* hidden  隐藏属性
* style  包含应用到元素的 CSS 样式声明。要注意样式最好定义在单独的文件中。这个属性以及 <style> 元素的主要目的是快速装饰。例如用于测试目的。
* tabindex 指示其元素是否可以聚焦，以及它是否/在何处参与顺序键盘导航（通常使用Tab键，因此得名）
* title 用来显示不完整的内容，一般配合省略号使用
  
## 常用内容标签
* ol+li 标签 指得是有序的列表
```
<ol>
    <li>你好</li>
    <li>我是xxx</li>
</ol>
```
* ul+li 标签 指无序列表
```
<ul>
    <li>小美</li>
    <li>小中</li>
    <li>小李</li>
</ul>
```
* dl+dt+dd  定义性列表，dt是被定义的内容，dd是对定义的描述
```
<dl>
    <dt>小美</dt>
    <dd>是个大美女</dd>
    <dt>小中</dt>
    <dd>是个大帅哥</dd>
</dl>
```
* pre 表示预定义格式文本。在该元素中的文本通常按照原文件中的编排，以等宽字体的形式展现出来，文本中的空白符（比如空格和换行符）都会显示出来。(紧跟在 <pre> 开始标签后的换行符也会被省略)
* code  用来报过代码，code内的字体是等宽的
```
<pre>
    <code>
    hello
    today is very well
    </code>
</pre>
```
* br 换行
* hr 分割线
* a 超链接标签
* em 表示强调，语气上的强调
* strong 表示自身的强调
* quota 表示引用（默认为内联样式），可以blockquota ，块级引用。