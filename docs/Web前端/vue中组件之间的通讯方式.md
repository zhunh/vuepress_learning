###  vue中组件之间的通讯方式

1.父 -> 子			prop

2.子 -> 父			$emit 触发自定义事件

3.其他方式		  中央事件管理器

4.如果是页面路由组件 ？ Vue

### vuex 的简介

vue 官方提供的 状态管理器

整个项目中需要在多个地方共享的数据存放在同一的位置进行管理

### 什么时候需要用vuex

1.使用了 vue- router,并且多个路由之间需要共享数据的时候

2.页面数据太多难以管理

### 使用vuex

1.安装 vuex

```shell
npm install --save vuex
```

2.在 src 目录下创建一个 store/index.js 文件

​	2.1思考项目的哪些数据要放到仓库中

3.需要在 main.js 中，也就是 new Vue 的时候，配置 store 这个选项，选项的值就是 store 的实例对象

4.如何使用仓库的数据

​	4.1使用 mapState 辅助函数

5.如何在组件中修改仓库的数据

​	5.1首先在仓库的 mutations 中定义一个修改 state 的方法

​	5.2组件中使用 mapMutations 辅助函数

