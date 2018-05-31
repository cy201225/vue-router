# vue-goback

> vue单页面，多路由，前进刷新，后退不刷新。
## 详细介绍
  　[另辟蹊径：vue单页面，多路由，前进刷新，后退不刷新](https://segmentfault.com/a/1190000012083511)

## Build Setup

``` bash
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

##使用vue-router中的多个钩子，当vue使用`this.$router.go(-1)`时，需要缓存时，可以使用`vue-router`里的其他钩子来给指定页面设置是否缓存，或者是否使用`<keep-active>`，通过动态设置`vue-router`的`meta`