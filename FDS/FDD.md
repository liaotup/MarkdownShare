# 前后端完全分离方案
### 由于无session  需要使用作为鉴权机制 OAUTH2.0
### 后端通过暴露RESTful API 向前端提供服务
### 前端通过异步请求调用后端服务，并通过路由控制页面跳转逻辑
### 相关框架
* Vue.js (v2.0 支持 虚拟DOM 前端性能大幅提升)
* React.js
* Avalon.js (IE支持)

### 相关组件库，组件应有尽有，无需经过UI设计，可以有非常专业的UI效果.
##### React
* Ant Design —— 阿里蚂蚁金服推出的一整套基于React的前端方案 （包括：UI组件，设计规范，案例代码，交互指引...）
##### Vue
* 饿了么的Elements 后台
* 传说Ant Design 也有一套Vue的版本。

### 现代前端相关工具集
* webpack2 模块化打包工具
* babel ES6 转换


### Vue相关内容，现代前端基本无需JQuery
* vue-router 页面路由组件
* vue-resource  与后端异步请求组件
* vue-validator 表单验证

### RESTfull相关
##### RESTfull 接口定义标准
##### Swagger 可执行接口文档，包括两个部分(springfox 、 Swagger UI)
* Swagger UI 会将API文档数据渲染成可执行、可阅读的文档。
* springfox通过Maven引入后端，可通过接口注解生成API文档数据.

### 相关术语
* SPA (single page application)
* MVVM (Model-View-ViewModel)
* OAUTH2 安全机制
