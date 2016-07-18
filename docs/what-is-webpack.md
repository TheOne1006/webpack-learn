# 什么是 webpack

webpack 是模块打包器.

![](images/what-is-webpack.png)

## 目标

- 将依赖树拆分，保证按需加载
- 保证初始加载的速度
- 所有静态资源可以被模块化
- 能够向模块一样整合第三方库
- 能够接近自定义模块打捆的每一个部分
- 适合构建大项目

## 不同

#### 1. Code Splitting 代码拆分
Webpack 有两种组织模块依赖的方式，同步和异步。异步依赖作为分割点，形成一个新的块。在优化了依赖树后，每一个异步区块都作为一个文件被打包。

#### 2. Loaders
Webpack 本身只能处理原生的 JavaScript 模块，但是 loader 转换器可以将各种类型的资源转换成 JavaScript 模块。这样，任何资源都可以成为 Webpack 可以处理的模块。

#### 3. Clever parsing 智能解析

Webpack 有一个智能解析器，几乎可以处理任何第三方库，无论它们的模块形式是 CommonJS、 AMD 还是普通的 JS 文件。甚至在加载依赖的时候，允许使用动态表达式 require("./templates/" + name + ".jade")。

#### 4. Plugin system 插件系统

Webpack 还有一个功能丰富的插件系统。大多数内容功能都是基于这个插件系统运行的，还可以开发和使用开源的 Webpack 插件，来满足各式各样的需求
