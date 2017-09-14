<template>
<div class="hello">



  <div class="example example1">
    <label for="">Simple content</label>
    <placeholderContent type="simple" :title="true" :number="3" :button="true"></placeholderContent>
  </div>

  <div class="example example2">
    <label for="">Table content</label>
    <placeholderContent type="table" :title="true" :button-title="true" :number="1" :button="true"></placeholderContent>
  </div>

  <div class="example example3">
    <label for="">Card content</label>
    <div class="container wrap">
      <div class="col-12 col-xl-4 col-lg-4 col-md-6 col-sm-12 box" v-for="x in 3">
        <placeholderContent type="card" :title="false" :description="true" :number="3" :photo="false" :button="false"></placeholderContent>
      </div>
    </div>
  </div>

  <div class="example example4">
    <label for="">Card content</label>
    <div class="container wrap">
      <div class="col-12 col-xl-4 col-lg-4 col-md-6 col-sm-12 box" v-for="x in 3">
        <placeholderContent type="card" :title="true" :description="true" :number="2" :photo="false" :button="false"></placeholderContent>
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
</style>
