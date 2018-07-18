# Vue H5 Seed with Cube UI and VW

> 使用 vw 实现移动端适配

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

## 注意

1. cube ui组建库需要设置为375 * 667， 不能设置为750 * 1334

```js
'postcss-px-to-viewport': {
  viewportWidth: 375, // (Number) The width of the viewport.
  viewportHeight: 667, // (Number) The height of the viewport.
}
```

2. 原文中, 在.postcssrc.js中，如下配置会引样式抖动(如cube ui中的showToast闪烁）

```js
"cssnano": {
  preset: "advanced",
  autoprefixer: false,
  "postcss-zindex": false
}
```

3. 因css新特性比较少用，故postcss-cssnext插件没有使用，还是使用原来的autoprefixer。

## 参考文档

[如何在 Vue 项目中使用 vw 实现移动端适配](https://www.w3cplus.com/mobile/vw-layout-in-vue.html)