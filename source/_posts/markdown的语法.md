---
title: markdown的语法
date: 2017-05-29 11:54:44
category: [前端]
tags: [markdown css]
---
- 段落引用标签 markdown支持html语法，所以有两种写法，html段落引用标签，前后会缩进，并且第一行会有< p>效果，但是可以添加自定义的css样式，使用markdown的语法写比较简洁：
<!-- more -->
  - 效果：
<blockquote style="text-align: center;">
html标签可以实现居中的效果
  <blockquote style="text-align: center;">
    嵌套使用
  </blockquote>
</blockquote>
> markdown标签
>> markdown引用第二次

  - 代码：
``` html
<blockquote style="text-align: center;">
html标签可以实现居中的效果
  <blockquote style="text-align: center;">
    嵌套使用
  </blockquote>
</blockquote>
> markdown标签
>> markdown引用第二次
```
<hr style="border: 1px solid green"/>
- 短引用标签 html普通引用标签, 会使包含在标签里面的文字被前后两个引号包含和段落引用的效果有区别：
 - ⚠️ 短引用并没有使文字加红的效果，这里只是为了更好的区分
 - 效果：
短引用标签之前<q><font style="color:red">我是短引用标签</font></q>短引用标签之前
 - 代码：
``` html
短引用标签之前<q><font style="color:red">我是短引用标签</font></q>短引用标签之前
```
<hr style="border: 1px solid green"/>
- 分割线效果 最终都是被解析为hr 使用原生的hr标签 可以定制自己的需求，一般使用markdown语法即可：
 - 效果：

 ---
 ***
<hr style="border: 1px solid red"/>
 - 代码 _ 上面要空一行：
``` html

---
***
<hr style="border: 1px solid red"/>
```
<hr style="border: 1px solid green"/>
- 向文章里面添加代码，分为两种 行内代码插入和代码块插入(前文黑色部分)：
 - 效果：
 `
  这是行内代码引用的效果<br/>
  这是行内代码引用的效果
 `
 - 行内代码：
```
`
 这是行内代码引用的效果<br/>
 这是行内代码引用的效果
`
```
 - 代码块代码：
```
<pre>
  ``` html 设置要高亮的代码风格 使用时去掉 pre 标签
  <hr style="border: 1px solid red"/>
  ```</pre>
```
<hr style="border: 1px solid green"/>
- 有序和无需列表
 - 有序列表
 - 效果：
 1\. 第一行
 2\. 第二行
 - 有序列表 代码 目前列表是默认从1递增，跟所输入的数字没有关系：
```
 1. 第一行
 200. 第二行
```
 - 无序列表代码
```
+ 实现无序列表的第一种方式
- 实现无序列表的第二种方式
* 实现无序列表的第三种方式
```
<hr style="border: 1px solid green"/>
- 插入图片
 - 效果：
 ![图片显示不出来时提示](/static/image/avatar.jpeg '我的头像')![图片显示不出来时提示](/static/image/avatar.jpeg '我的头像')
 - 代码 目前没办法自定义宽高 有这个需求可以该用image标签：
```
![图片显示不出来时提示](/static/image/avatar.jpeg '我的头像')![图片显示不出来时提示](/static/image/avatar.jpeg '我的头像')
```
<hr style="border: 1px solid green"/>
- 链接
 - 效果：
 邮箱链接：<admin@admin.com>
 超链接：[Google](https://www.google.com/ncr)
 - 代码：
```
邮箱链接：<chenhongvvei@gmail.com>
超链接：[Google](https://www.google.com/ncr)
```
<hr style="border: 1px solid green"/>
### 特别感谢:
 - [Markdown 语法说明 \(简体中文版\)](http://wowubuntu.com/markdown/#img)
 - [makrdown-wiki](https://en.wikipedia.org/wiki/Markdown#Example)
 - [简书 markdown常用的语法](http://www.jianshu.com/p/82e730892d42)
<hr style="border: 1px solid green"/>
  前人栽树，后人乘凉，感谢他们的贡献！
