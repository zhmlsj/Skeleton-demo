# Skeleton-demo

> A Vue.js project

## Build Setup

```bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

# 实现步骤

## 安装插件

- npm install vue-skeleton-webpack-plugin

## 首先建立一个文件夹 Skeleton

- 先写好骨架屏组件 Skeleton.vue
- 创建一个仅使用骨架屏组件的入口文件 js skeleton.entry.js

## 在 build 里面建立文件 webpack.skeleton.conf.js

## 在 webpack.dev.conf.js 和 webpack.dev.conf.js 里面插入

```bash
const SkeletonWebpackPlugin = require("vue-skeleton-webpack-plugin");

 new SkeletonWebpackPlugin({
      webpackConfig: require('./webpack.skeleton.conf'),
      quiet: true
    })

```
