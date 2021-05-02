<template>
  <div class="container text-center py-16">
    <carousel class="mx-4" paginationActiveColor="#6534FF" :perPageCustom="[[0,1],[575.98,2],[767.98, 3], [991.98, 4],[1199.98,5]]">
      <slide v-for="image in images" :key="image.id">
        <img :class="image.class" :src="require('~/assets/images/'+image.img)" alt="Sliders">
      </slide>
    </carousel>
  </div>
</template>
<style lang="sass" scoped>
.d1
  width: 65
  height: 130
.d2
  width: 63
  height: 137
</style>

<script>
import Vue from 'vue';
import VueCarousel from 'vue-carousel';
Vue.use(VueCarousel);
import { Carousel, Slide } from 'vue-carousel';
export default {
  data(){
    return{
      images:[
        {
          id:0,
          img:'1.png',
          class:'d1'
        },
        {
          id:1,
          img:'2.png',
          class:'d2'
        },
        {
          id:2,
          img:'1.png',
          class:'d1'
        },
        {
          id:3,
          img:'2.png',
          class:'d2'
        },
        {
          id:4,
          img:'1.png',
          class:'d1'
        },
      ]
    }
  },
  components: {
    Carousel,
    Slide
  }
}
</script>
