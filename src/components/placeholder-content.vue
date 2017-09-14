<template>
<div class="hello">
  component
</div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.size1 {
  flex-basis: 100px
}

.size2 {
  flex-basis: 200px
}

.size3 {
  flex-basis: 300px
}

.size4 {
  flex-basis: 400px
}

.size5 {
  flex-basis: 500px
}

.size6 {
  flex-basis: 600px
}

.flex1 {
  flex-grow: 1
}

.flex2 {
  flex-grow: 2
}

.flex3 {
  flex-grow: 3
}

.flex4 {
  flex-grow: 4
}

.flex5 {
  flex-grow: 5
}

.flex6 {
  flex-grow: 6
}


.loader-container {
  margin: 0 auto;
  width: 400px;
  max-width: 90%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center
}

@keyframes placeholder {
  0% {
    background-position: -600px 0
  }
  100% {
    background-position: 600px 0
  }
}

.animated-background {
  animation-duration: 1s;
  animation-fill-mode: forwards;
  animation-iteration-count: infinite;
  animation-name: placeholder;
  animation-timing-function: linear;
  background: #ddd;
  background: linear-gradient(to right, #ddd 8%, #ccc 18%, #ddd 33%);
  background-size: 1200px 100px;
  min-height: 30px;
  width: 100%;
  margin: 5px 5px 5px 0;
  border-radius: 3px;
  opacity: .5
}

.profile-image {
  margin-top: 10px;
  border-radius: 50%;
  width: 100px;
  height: 100px
}
</style>
