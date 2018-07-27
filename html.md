## 介绍
此文档主要介绍 HTML 的编码规范以及基本风格要求。

<br/>

## 具体规范
1.&nbsp;**推荐** `doctype` 使用 `html5` 的声明，并且位于文件首行。
```html
<!DOCTYPE html>
```

2.&nbsp;**必须** 使用两个空格进行代码缩进。（IDE 设置 tab 用两个空格代替）

3.&nbsp;除非额外情况，所有 `html` 代码 **必须** 使用小写。

4.&nbsp;**尽量** 剔除多余没有用到的标签或者注释。

你可以使用一些工具，例如 [W3C HTML validator](https://validator.w3.org/nu/) 去验证你页面上 HTML 的有效性和使用率。

5.&nbsp;**尽量** 根据标签原先设计目的使用。

例如 div 一般用于布局，无其他额外语义，p 用于文字段落，h1-h6 用于标题，a 用于链接等等。

6.&nbsp;**尽量** 优先使用语义化的标签。

例如，`article, section`，等等。

7.&nbsp;有闭合的标签 **必须** 闭合，无需闭合的标签不要闭合。
```html
<p>hello, world</p>
<br>

// 不推荐
<br/>
```

8.&nbsp;标签属性 **必须** 使用双引号括起来，且移除多余的空格。
```html
<!-- 不推荐 -->
<p id='greet'>hello, world</p>
<p id=' greet '>hello, world</p>
<p id= 'greet'>hello, world</p>

<!-- 推荐 -->
<p id="greet">hello, world</p>
```

9.&nbsp;`img` 标签 **尽量** 加上 `alt` 说明。
```html
<img src="https://xxx.com/static/logo.png" alt="site logo">
```

10.&nbsp;页面编码无特殊情况下 **必须** 使用 `UTF-8` 编码。
```html
<meta chartset="UTF-8">
```

11.&nbsp;页面语言无特殊情况下 **必须** 使用 `zh-CN` 。
```html
<html lang="zh-CN">
```

12.&nbsp;**尽量** 减少多层标签嵌套，剔除多余、无用的标签，精简代码结构。

<br>

## 参考
Google HTML Style Guide: https://google.github.io/styleguide/htmlcssguide.html#HTML