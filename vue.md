参见 [Vue 官方风格指南](https://cn.vuejs.org/v2/style-guide/) 进行编码，同时有以下几点强制要求。

1.&nbsp;组件名以连接线风格（hyphen-style）命名

```js
new Vue({
  name: 'my-component', // good
  name: 'myComponent',  // not good
});
```

2.&nbsp;单文件组件的文件名以连接线风格命名

```js
my-component.vue  // good
myComponent.vue   // not good
```

3.&nbsp;组件文件夹以连接线风格命名

```js
|—— user-manage     // good
  |—— my-component.vue

|—— userManage     // not good
  |—— myComponent.vue
```
