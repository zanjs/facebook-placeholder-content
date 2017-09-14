<template>
  <div class="hello">
    <placeholderContent></placeholderContent>
  </div>
</template>

<script>
import placeholderContent from './placeholder-content'

export default {
  name: 'hello',
  data () {
    return {
    }
  },
  components: {
    placeholderContent
  }
}
</script>


<style scoped>
.hello {
  width: 1200px;
  max-width: 90%;
  margin: 0 auto;
}
</style>
