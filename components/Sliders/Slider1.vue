<template>
  <div class="container text-center">
    <carousel class="mx-4" paginationActiveColor="#6534FF" :perPageCustom="[[0,1],[575.98,2],[767.98, 1], [991.98, 2],[1199.98,2]]">
      <slide v-for="slide in slides" :key="slide.id" class="text-left">
        <div class="px-md-16 px-8">
          <p>{{slide.paragraph}}</p>
          <h5 class="mt-8">{{slide.h5}}</h5>
          <span class="font-italic paragraphs2">- {{slide.span}}</span>
        </div>
      </slide>
    </carousel>
  </div>
</template>
<style lang="sass">
h5
  color: rgba(0, 0, 0, 0.75)
  font-weight: 600
span
  letter-spacing: 3px
p
  line-height: 2
  letter-spacing: 2px
button.VueCarousel-dot
  width: 20px !important
  border-radius: 42% !important
  height: 7px !important
  outline: none !important
</style>

<script>
import Vue from 'vue';
import VueCarousel from 'vue-carousel';
Vue.use(VueCarousel);
import { Carousel, Slide } from 'vue-carousel';
export default {
  data(){
    return{
      slides:[
        {
          paragraph:'Do you want to be even more successful?Learn to love learning and growth. The more effort you put into improving your skills,the bigger the payoff you will get. Realize that things will be hard at first, but rewards worth it.',
          h5:'Calum Chambers',
          span:'Adobe sales manager'
        },
        {
          paragraph:'Do you want to be even more successful?Learn to love learning and growth. The more effort you put into improving your skills,the bigger the payoff you will get. Realize that things will be hard at first, but rewards worth it.',
          h5:'Calum Chambers',
          span:'Adobe sales manager'
        },
        {
          paragraph:'Do you want to be even more successful?Learn to love learning and growth. The more effort you put into improving your skills,the bigger the payoff you will get. Realize that things will be hard at first, but rewards worth it.',
          h5:'Calum Chambers',
          span:'Adobe sales manager'
        },
        {
          paragraph:'Do you want to be even more successful?Learn to love learning and growth. The more effort you put into improving your skills,the bigger the payoff you will get. Realize that things will be hard at first, but rewards worth it.',
          h5:'Calum Chambers',
          span:'Adobe sales manager'
        },
        {
          paragraph:'Do you want to be even more successful?Learn to love learning and growth. The more effort you put into improving your skills,the bigger the payoff you will get. Realize that things will be hard at first, but rewards worth it.',
          h5:'Calum Chambers',
          span:'Adobe sales manager'
        },
        {
          paragraph:'Do you want to be even more successful?Learn to love learning and growth. The more effort you put into improving your skills,the bigger the payoff you will get. Realize that things will be hard at first, but rewards worth it.',
          h5:'Calum Chambers',
          span:'Adobe sales manager'
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
