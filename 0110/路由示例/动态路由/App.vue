<template>
  <div id="app">
    <p>
    <router-link to="/">首页</router-link>
    <router-link to="/news">新闻</router-link>
    <router-link to="/about">关于我们</router-link>
    <router-link to="/player/1">墨鱼</router-link>
    <router-link to="/player/2">丁长生</router-link>
    </p>
	
	<router-view/>
  </div>
</template>

<script>
import './assets/css/style.css'
export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
