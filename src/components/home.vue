<template>
<div class="hello">

  <div class="intro container align-items-center justify-content-center">
    <div class="intro-block">
      <h1>A flexible, responsive, touch-friendly palceholder content for Vue.js</h1>
      <div class="intro-buttons container align-items-center justify-content-center">
        <div class="">
          <router-link class="btn start" :to="{ name: 'Home' }">GET STARTED</router-link>
        </div>
        <div class="">
          <router-link class="btn" :to="{ name: 'Home' }">GITHUB</router-link>
        </div>
      </div>
    </div>
  </div>

  <div class="example example5">
    <label for="">Card content</label>
    <div class="container wrap">
      <div class="col-12 col-xl-4 col-lg-4 col-md-6 col-sm-12 box" v-for="x in 3">
        <placeholderContent type="card" :photo="true" :title="true" :description="false" :number="1" :button="false"></placeholderContent>
      </div>
    </div>
  </div>


</div>
</template>

<script>
import placeholderContent from './placeholder-content'

export default {
  name: 'hello',
  data () {
    return {}
  },
  components: {
    placeholderContent
  }
}
</script>


<style scoped>
@import '../../node_modules/the-grid-flexbox/css/the-grid.min.css';
.intro {
  min-height: 250px;
  padding-top: 100px
}
.intro .intro-block {
  width: 700px;
  max-width: 90%;
}
.intro .intro-block h1 {
  font-size: 2.5rem;
  font-weight: 500
}
.box {
  padding: 20px;
  box-sizing: border-box;
}

.hello {
  width: 1200px;
  max-width: 90%;
  margin: 0 auto;
}

.example {
  padding-top: 100px;
  padding-bottom: 100px;
  text-align: left
}

.example label {
  font-weight: 600;
  padding-bottom: 20px
}
@media screen and (max-width: 480px) {
  .intro .intro-block h1 {
    font-size: 1.5rem;
  }
}
</style>
