<template>
  <div>
      <router-link to="page1">第一个页面</router-link>
      <router-link to="page2">第二个页面</router-link>
      <router-link to="page3">第三个页面</router-link>
  </div>
</template>
<script>
export default {
    beforeRouteLeave(to, from, next) {
    // 路由导航钩子，此时还不能获取组件实例 `this`，所以无法在data中定义变量（利用vm除外）
    // 参考 https://router.vuejs.org/zh-cn/advanced/navigation-guards.html
    // 所以，利用路由元信息中的meta字段设置变量，方便在各个位置获取。这就是为什么在meta中定义isBack
    // 参考 https://router.vuejs.org/zh-cn/advanced/meta.html
    // if(from.name=='page2'){
    //     to.meta.isBack=true;
    //     //判断是从哪个路由过来的，
    //     //如果是page2过来的，表明当前页面不需要刷新获取新数据，直接用之前缓存的数据即可
    // }
    next();
},
}
</script>
<style scoped>
a{
    display: block;
    margin-top: 20px;
}
</style>
