<template>
<div class="hello">

  <div class="" v-show="isLoading" v-cloak>
    <div class="container wrap">
      <div class="col-12 col-xl-4 col-lg-4 col-md-6 col-sm-12 box" v-for="x in 3">
        <placeholderContent type="card" :photo="true" :title="true" :description="false" :number="1" :button="false" :imageSize="400"></placeholderContent>
      </div>
    </div>
  </div>

  <div class="" v-show="!isLoading" v-cloak>
    <div class="container wrap justify-content-center align-items-center">
      <div class="col-12 col-xl-4 col-lg-4 col-md-6 col-sm-12 box" v-for="x in teste">
        <div class="container justify-content-start align-items-center">
          <div class="picture">
            <img :src="x.profile" width="180%" alt="">
          </div>
          <div class="container column justify-content-start align-items-center">
            <div class="example-text">
              <h1>{{x.name}}</h1>
              <p>{{x.time}}</p>
            </div>
          </div>
        </div>
        <div class="image-ex" v-bind:style="{ 'background-image': 'url(' + x.img + ')' }">
          <!-- <img :src="x.img" width="100%" alt=""> -->
        </div>
      </div>
    </div>
  </div>

  <span class="btn start" :to="{ name: 'Docs' }" @click="tryAgain">Try again</span>


</div>
</template>

<script>
import placeholderContent from './placeholder-content'

export default {
  name: 'hello',
  data () {
    return {
      isLoading: true,
      teste: [{
        name: 'Will smith',
        time: 'Agora pouco',
        profile: 'https://fashionfoodandflirts.files.wordpress.com/2013/04/fresh-prince-will-smith.jpg',
        img: 'https://s2.glbimg.com/aAjW1O_ErEF6fbcfh9nkZh9mBxw=/227x0:779x600/570x620/smart/http://s2.glbimg.com/_wZd-4_-aTqEE3ZaZITdonmzvpo=/0x0:1060x600/1060x600/s.glbimg.com/po/tt2/f/original/2017/09/13/iphone_8_plus_tela_aplicativos_apps_mao.jpg'
      },
      {
        name: 'Will smith',
        time: 'Agora pouco',
        profile: 'https://www.rickey.org/wp-content/uploads/2015/08/fresh_prince_header.jpg',
        img: 'https://jovemnerd.com.br/wp-content/uploads/2016/08/fresh-prince-vitrine-760x428.jpg'
      },
      {
        name: 'Will smith',
        time: 'Agora pouco',
        profile: 'https://fashionfoodandflirts.files.wordpress.com/2013/04/fresh-prince-will-smith.jpg',
        img: 'https://art-s.nflximg.net/ef14e/f435deeec5987212d8fe76b75ab7015bb73ef14e.jpg'
      }]
    }
  },
  components: {
    placeholderContent
  },
  methods: {
    fakeFetch: function () {
      this.isLoading = !this.isLoading
    },
    Loading: function () {
      setTimeout(this.fakeFetch, 2000)
    },
    tryAgain: function () {
      this.isLoading = !this.isLoading
      setTimeout(this.fakeFetch, 2000)
    }
  },
  mounted () {
    this.Loading()
  }
}
</script>


<style scoped>
.btn {
  cursor: pointer
}

.card-ex {
  background: blue;
  width: 100%;
}

.image-ex {
  height: 400px;
  margin-top: 12px;
  overflow: hidden;
  background-position: center;
  background-size: cover;
  border-radius: 3px
}

.example-text {
  text-align: left;
  /*background: red*/
}

.example-text h1 {
  font-size: 18px
}

.example-text p {
  font-size: 14px
}

.picture {
  height: 60px;
  width: 60px;
  border-radius: 50%;
  margin-right: 20px;
  background: red;
  overflow: hidden;
}

.photo {
  height: 400px;
  border-radius: 40px!important;
  overflow: hidden;
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
</style>
