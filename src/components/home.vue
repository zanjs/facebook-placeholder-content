<template>
<div class="hello">

  <div class="intro container align-items-center justify-content-center">
    <div class="intro-block">
      <h1>A flexible, responsive, touch-friendly palceholder content for Vue.js</h1>
      <div class="intro-buttons container align-items-center justify-content-center">
        <div class="">
          <router-link class="btn start" :to="{ name: 'Docs' }">GET STARTED</router-link>
        </div>
        <div class="">
          <a href="https://github.com/HelpySolutions/facebook-placeholder-content" class="btn" target="_blank">GITHUB</a>
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
    <div class="container">
<pre><code class="html" id="foo">
  &lt;placeholderContent type=&quot;card&quot; :photo=&quot;true&quot; :title=&quot;true&quot; :description=&quot;false&quot; :number=&quot;1&quot; :button=&quot;false&quot;&gt;&lt;/placeholderContent&gt;

</code></pre>
<a class="btn btn-copy" data-clipboard-target="#foo">copy</a>
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
.btn-copy {
  height: 40px;
  line-height: 20px
}
pre {
  /*max-width: 90%;
  margin: 0 auto*/
  margin: 0 20px;
}
pre, code {
  border-radius: 4px;
  overflow: hidden
}
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
