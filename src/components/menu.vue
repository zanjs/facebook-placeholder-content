<template>
<div>

<div class="relative-menu">
  <div class="menu-full">
    <div class="menu container justify-content-between align-items-center">
      <router-link :to="{ name: 'Home' }">
      <div class="logo-menu container align-items-center">
        <img src="../assets/images/logo-01.svg" width="40" alt="">
        <h1>Monk Placeholder Content</h1>
      </div>
      </router-link>
      <div class="link-menu">
        <ul class="container">
          <li><router-link :to="{ name: 'Home' }">Home</router-link></li>
          <li><router-link :to="{ name: 'Docs' }">Docs</router-link></li>
          <li><router-link :to="{ name: 'Examples' }">Examples</router-link></li>
          <li><router-link :to="{ name: 'Testes' }">Testes</router-link></li>
        </ul>
      </div>
    </div>
  </div>
</div>



</div>
</template>

<style scoped>
.logo-menu h1,
.logo-menu a {
  font-size: 20px;
  margin-left: 10px;
  font-weight: 500
}
.link-menu ul.container {
  list-style: none;
}
.link-menu ul.container a {
  text-decoration: none;
  padding: 10px;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  font-size: 14px;
  font-weight: 500
}
.relative-menu {
  height: 60px;
  width: 100%;
  position: relative;
  margin-bottom: 20px
}
.menu-full {
  height: 60px;
  width: 100%;
  position: fixed;
  z-index: 99;
  background: #fff;
}
.menu {
  height: 60px;
  width: 95%;
  margin: 0 auto
}
@media screen and (max-width: 720px) {
  .logo-menu h1 {
    font-size: 16px!important;
  }
}
@media screen and (max-width: 480px) {
  .link-menu {
    display: none
  }
}
</style>

<script>
export default {
  data () {
    return {}
  }
}
</script>
