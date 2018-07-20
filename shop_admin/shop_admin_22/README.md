# shop_admin_22

## 初始化项目

- 将 `src` 目录中原来默认生成的内容，全部删除

```html
源码全部放在 src 目录，只要修改 src 目录中的内容即可：

/assets           资源文件夹，放：图片、样式等等
/components       组件文件夹，所有的组件，都放到该目录中，并且每个组件都使用文件夹包裹
/router           路由
App.vue           根组件，就包含一个路由出口 <router-view></router-view>
main.js           整个项目的入口，也是webpack打包的入口
```

## 如何开一个新功能

- 1 在 `components` 目录中创建组件
- 2 在 `router/index.js` 中配置路由

## Element-UI的使用

- 1 安装：`npm i element-ui -S`
- 2 在 `main.js` 文件中导入element-ui的js和样式，并且安装称为插件

```js
import Vue from 'vue'
// 1 导入EelmentUI
import ElementUI from 'element-ui'
// 2 导入 ElementUI的样式
import 'element-ui/lib/theme-chalk/index.css'
import App from './App.vue'
// 3 安装插件
Vue.use(ElementUI)

new Vue({
  el: '#app',
  render: h => h(App)
})
```

- 3 打开element-ui的文档，从左侧菜单中找到对应的组件，参考示例代码，复制到自己页面中使用即可

## axios发送请求

- 1 安装：`npm i -S axios`
- 2 导入：`import axios from 'axios'`
- 3 使用：`axios.post(接口地址, 参数).then(成功).catch(失败)`

## vue-router 编程式导航

- 通过JS代码来实现跳转：`this.$router.push('/home')`
