<template>
  <div id="app">
  <keep-alive>
      <router-view v-if="$route.meta.keepAlive"></router-view>
  </keep-alive>
  <router-view v-if="!$route.meta.keepAlive"></router-view>
  <el-publish></el-publish>
  </div>
</template>

<script>
import publish from './components/publish/publish' 
import less from './components/less'
export default {
  name: 'app',
  components: {
    'el-less' : less,
    'el-publish' : publish
  }
}
</script>

<style>
#app {
  font-family: '宋体', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 100%;
  height: 100%;
  overflow-x:hidden;
}
a{
  color: #2c3e50;
}
</style>
