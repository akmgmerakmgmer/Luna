<template>
  <div id="carouselExampleCaptions" class="carousel slide" data-ride="carousel">
  <div class="carousel-inner slider">
    <div class="carousel-item active position-relative" >
      <img :src="require(`@/assets/images/${image}`)" class="d-block w-100" alt="startup">
      <div class="carousel-caption d-block w-75">
        <h5 class="animate__animated animate__fadeInRight white--text">{{title}}</h5>
        <div class="border-header mt-md-0 mt-5"></div>
        <p class="animate__animated animate__fadeInUp paragraphs1 d-sm-block d-none mt-10">We receive results combining marketing, a creative and industry experience</p>
        <a href="https://www.youtube.com/watch?v=VW2xRR75lKE" target="_blank"><v-icon class="play mt-md-3 mt-16 py-6 px-6" large>mdi-play</v-icon></a>
        <div class="scroll-down w-100 d-sm-block d-none">
          <span class="paragraphs3 text-uppercase d-block">Scroll Down</span>
          <a href="#features"><i class="fa fa-arrow-down paragraphs1 mt-3" aria-hidden="true"></i></a>
        </div>
      </div>
    </div>
  </div>
</div>
</template>
<style lang="sass" scoped>
@import "~/assets/style.sass"
.slider
  .carousel-item
    .carousel-caption
      top: 54%
      left: 50%
      transform: translate(-50%, -50%)
      h5
        --animate-duration: 1s
        font-size: 52px
        font-weight: 800
        @media (max-width: 575.98px)
          font-size: 32px
        @media (min-width: 576px) and (max-width: 767.98px)
          font-size: 36px
        @media (min-width: 768px) and (max-width: 991.98px)
          font-size: 42px
        @media (min-width: 992px) and (max-width: 1199.98px)
          font-size: 48
      .border-header
        border-bottom: 5px solid $main-color !important
        margin-left: 40%
        margin-right: 40%
      p
        --animate-duration: 1.7s
      .play
        color: $main-color
        border: 3px solid $main-color
        border-radius: 50%
        cursor: pointer
        @include transition(all, 0.3s, ease-in-out)
        &:hover
          background: $main-color
          color: $white-color
      .scroll-down
        margin-top: 5%
        span
          letter-spacing: 5px
          font-weight: 300
        i
          @include animator(arrow-animation,0.7s,linear,0s,infinite)
          cursor: pointer
          color: $white-color
    img
      height: 100vh
      object-position: center
      object-fit: cover

@keyframes arrow-animation
  0%
    padding-top: 0px
  50%
    padding-top: 15px
  100%
    padding-top: 0px

</style>
<script>
import 'animate.css'
export default {
  data(){
    return{
      dialog:false
    }
  },
  methods:{
  },
  props:['title','image']
}
</script>
