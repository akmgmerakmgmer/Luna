<template>
  <div class="mixit text-center secondery-coloring">
    <div class="controls my-8">
      <v-btn elevation="0" type="button" class="control paragraphs3 mr-md-5 mr-2 main-coloring" data-filter="all">All</v-btn>
      <v-btn elevation="0" type="button" class="control paragraphs3 mr-md-5 mr-2" data-filter=".digital">Digital</v-btn>
      <v-btn elevation="0" type="button" class="control paragraphs3 mr-md-5 mr-2" data-filter=".branding">Branding</v-btn>
      <v-btn elevation="0" type="button" class="control paragraphs3 mr-md-5 mr-2" data-filter=".marketing">Marketing</v-btn>
      <v-btn elevation="0" type="button" class="control paragraphs3 mr-md-5 mr-2" data-filter=".video">Video</v-btn>
      <v-btn elevation="0" type="button" class="control paragraphs3" data-filter=".photo">Photo</v-btn>
    </div>
    <div class="mixit-slider row">
      <img v-for="image in images" :key="image.id" :src="require('~/assets/images/'+image.img)" :class="image.class" alt="Mixits" >
    </div>
  </div>
</template>
<style lang="sass" scoped>
@import "~/assets/style.sass"
.mixit
  .controls
    .control
      text-transform: capitalize
      letter-spacing: 3px
      background-color: transparent
      font-family: montserrat,sans-serif
  .mixit-slider
    position: relative
    img
      height: 60vh
      object-fit: cover
      padding: 0
      z-index: 0
</style>
<script>
export default{
  data () {
    return {
      images:[
        {
          id:1,
          img:'portfolio3.jpg',
          class:'mix digital w-100 col-md-4'
        },
        {
          id:2,
          img:'portfolio2.jpg',
          class:'mix branding w-100 col-md-4'
        },
        {
          id:3,
          img:'portfolio1.jpg',
          class:'mix marketing w-100 col-md-4'
        },
        {
          id:4,
          img:'portfolio4.jpg',
          class:'mix video w-100 col-md-4'
        },
        {
          id:5,
          img:'portfolio5.jpg',
          class:'mix photo w-100 col-md-4'
        },
      ]

    }
  },
  methods:{

  },
  mounted () {
    $(".control").click(function(){
      $(this).addClass("main-coloring")
      $(this).siblings().removeClass("main-coloring")
    })
    var containerEl = document.querySelector('.mixit-slider');
    var mixer = mixitup(containerEl);
  }
}
</script>
