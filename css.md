## 介绍
此文档主要介绍 CSS 的编码规范以及基本风格要求。

<br/>

## 具体规范
1.&nbsp;**必须** 使用两个空格进行代码缩进。（IDE 设置 tab 用两个空格代替）

2.&nbsp;类名的格式

1. 必须全部小写。
2. 以连接符 `-` 连接单词
```css
.user-info {
  //
}
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
// 推荐
.user-info {
  color: white;
  font-size: 14px;
}
// 不推荐
.user-info { color: white; font-size: 14px; }
```

7.&nbsp;属性 `key` 与 `value` 之间的冒号之前不留空格，之后留 **单个** 空格

```js
// 推荐
.user-info {
  color: white;
  font-size: 14px;
}
// 不推荐
.user-info {
  color:white;
  font-size : 14px;
}
```

8.&nbsp;**推荐** 使用单引号代替双引号。
```css
// 推荐
.user-info {
  font-family: 'Microsoft Yahei';
}
// 不推荐
.user-info {
  font-family: "Microsoft Yahei";
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