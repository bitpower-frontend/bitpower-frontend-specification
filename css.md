## 介绍
此文档主要介绍 CSS 的编码规范以及基本风格要求。

<br/>

## 检测工具
使用 [stylelint](https://stylelint.io) 进行检查，基于 [stylelint-config-bitpower](https://github.com/bitpower-frontend/stylelint-config-bitpower) 配置。

<br/>

## 具体规范
1.&nbsp;**必须** 使用两个空格进行代码缩进。（IDE 设置 tab 用两个空格代替）

2.&nbsp;类名的格式

1. 必须全部小写。
2. 以连接符 `-` 连接单词。
3. 简短且有意义，不使用表象名称，而是表意或表明作用的名称。
```css
// 不推荐
.green-btn {}
.navigation {}

// 推荐
.submit-btn {}
.nav {}
```

3.&nbsp;如果元素确定唯一，**尽量** 使用 id 选择器。

4.&nbsp;**禁止** 滥用 `*` 选择器。

5.&nbsp;选择器与花括号之间保留一个空格。
```css
.user-info {
  //
}
```

6.&nbsp;包含多个属性时，花括号之间 **尽量** 新起一行。
```css
// 不推荐
.user-info { color: white; font-size: 14px; }

// 推荐
.user-info {
  color: white;
  font-size: 14px;
}
```

7.&nbsp;属性 `key` 与 `value` 之间的冒号之前不留空格，之后留 **单个** 空格

```css
// 不推荐
.user-info {
  color:white;
  font-size : 14px;
}

// 推荐
.user-info {
  color: white;
  font-size: 14px;
}
```

8.&nbsp;**推荐** 使用单引号代替双引号。
```css
// 不推荐
.user-info {
  font-family: "Microsoft Yahei";
}

// 推荐
.user-info {
  font-family: 'Microsoft Yahei';
}
```

9.&nbsp;关于浏览器前缀属性。

如果有 `autoprefixer` 处理，**尽量** 不要写浏览器前缀属性，否则按照 `浏览器前缀属性在前，标准属性在后` 的方式书写。
```css
.user-info {
  -webkit-border-radius: 10px;
  -moz-border-radius: 10px;
  -o-border-radius: 10px;
  -ms-border-radius: 10px;
  border-radius: 10px;
}
```

10.&nbsp;**尽量** 剔除多余没有用到的代码或者注释。

你可以使用一些工具，例如 [W3C CSS validator](https://jigsaw.w3.org/css-validator/) 去验证你页面上 CSS 的有效性和使用率。

11.&nbsp;**尽量** 避免标签和类，ID选择器混用。
```css
// 不推荐
h1.title {}
img#avatar {}

// 推荐
.title {}
#avatar {}
```

12.&nbsp;**尽量** 使用简写属性代替多个属性。
```css
// 不推荐
.title {
  border-width: 1px;
  border-style: solid;
  border-color: #ccc;
}

// 推荐
.title {
  border: 1px solid #ccc;
}
```

13.&nbsp;颜色十六进制 **推荐** 使用简写。
```css
// 不推荐
.title {
  color: #cccccc;
  border-color: #eebbcc;
}

// 推荐
.title {
  color: #ccc;
  border-color: #ebc;
}
```

14.&nbsp;**尽量** 不要使用 `!important` 覆盖属性。

15.&nbsp;规则之间 **必须** 以一个空行隔开。
```css
// 规则一
.title {
  color: #cccccc;
}

// 规则二
.avatar {
  width: 40px;
}
```

16.&nbsp; `url()` **尽量** 不要使用引号。
```css
// 不推荐
@import url("https://www.google.com/css/maia.css");

// 推荐
@import url(https://www.google.com/css/maia.css);
```

17.&nbsp;属性声明的顺序 **推荐** 按字母排序。
```css
.title {
  background: fuchsia;
  border: 1px solid;
  -moz-border-radius: 4px;
  -webkit-border-radius: 4px;
  border-radius: 4px;
  color: black;
  text-align: center;
  text-indent: 2em;
}
```

<br>

## 参考
Google CSS Style Guide: https://google.github.io/styleguide/htmlcssguide.html#CSS