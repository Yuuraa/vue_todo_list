<template>
  <div id="app">
    <router-link to="/todos"> todos </router-link>
    <img src="./assets/logo.png">
    <!-- 이 부분을 통해 /test1 과 같이 페이지로 들어갈 때마다 아래에 다른 것이 뜨게 한다 -->
    <router-view/>
  </div>
</template>

<script>
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
