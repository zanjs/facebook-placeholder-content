<template>
  <div id="app">
    <headerMenu></headerMenu>
    <router-view></router-view>
  </div>
</template>

<script>
import headerMenu from './components/menu'

export default {
  name: 'app',
  components: {
    headerMenu
  }
}
</script>

<style>
@import '../node_modules/the-grid-flexbox/css/the-grid.min.css';
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
a {
  text-decoration: none;
  color: #2c3e50
}
* {
  margin: 0;
  padding: 0
}
.btn {
  background: #ccc;
  height: 60px;
  line-height: 60px;
  padding: 10px 25px 10px 25px ;
  margin: 10px;
  border: 1px solid #4fc08d;
  color: #4fc08d;
  text-decoration: none;
  background: transparent;
  font-size: 14px;
  font-weight: 700;
  border-radius: 20px;
  transition: all 0.15s ease;
  cursor: pointer;
}
.btn:hover {
  background: #449872;
  color: #fff;
  border-color: #449872;
}
.btn.start {
  background: #4fc08d;
  color: #fff;
}
.btn.start:hover {
  background: #449872;
  color: #fff;
}
</style>
