<template>
  <div id="carouselExampleCaptions" class="carousel slide" data-ride="carousel">
  <div class="carousel-inner slider">
    <div class="carousel-item active position-relative">
      <img :src="require(`@/assets/images/${image1}`)" class="d-block w-100" alt="agency">
      <div class="carousel-caption d-block w-75">
        <h2 class="animate__animated animate__fadeInRight">{{title}}</h2>
        <p class="animate__animated animate__fadeInUp paragraphs1 d-sm-block d-none">We receive results combining marketing, a creative and industry experience</p>
        <div class="mt-5">
          <nuxt-link to="/business"><button class="default-button mr-md-5 paragraphs3 mr-sm-3 animate__animated animate__slow animate__fadeInLeft about_button">About Us</button></nuxt-link>
          <nuxt-link to="/contacts1"><button class="default-button ml-md-5 paragraphs3 ml-sm-3 mt-sm-0 mt-3 animate__animated animate__slow shadow animate__fadeInRight">Get Start</button></nuxt-link>
        </div>
        <div class="scroll-down w-100 d-sm-block d-none">
          <span class="paragraphs3 text-uppercase d-block">Scroll Down</span>
          <a href="#features"><i class="fa fa-arrow-down paragraphs1 mt-3" aria-hidden="true"></i></a>
        </div>
      </div>
    </div>
    <div class="carousel-item">
      <img :src="require(`@/assets/images/${image2}`)" class="d-block w-100" alt="slider">
      <div class="carousel-caption d-block w-75 ">
        <h2 class="animate__animated animate__fadeInRight">{{title2}}</h2>
        <p class=" animate__animated animate__fadeInUp paragraphs1 d-sm-block d-none">We receive results combining marketing, a creative and industry experience</p>
        <div class="mt-5">
          <button class="default-button mr-md-5 paragraphs3 mr-sm-3 animate__animated animate__slow animate__fadeInLeft about_button">About Us</button>
          <button class="default-button mr-md-5 paragraphs3 mr-sm-3 mt-sm-0 mt-3 animate__animated animate__slow shadow animate__fadeInRight">Get Start</button>
        </div>
        <div class="scroll-down w-100 d-sm-block d-none">
          <span class="paragraphs3 text-uppercase d-block">Scroll Down</span>
          <a href="#features"><i class="fa fa-arrow-down paragraphs1 mt-3" aria-hidden="true"></i></a>
        </div>
      </div>
    </div>
  </div>
  <a class="carousel-control-prev" href="#carouselExampleCaptions" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="carousel-control-next" href="#carouselExampleCaptions" role="button" data-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>
</template>
<style lang="sass" scoped>
@import "~/assets/style.sass"
.carousel-control-next, .carousel-control-prev
  width: 10%
.slider
  .carousel-item
    .carousel-caption
      top: 57%
      left: 50%
      transform: translate(-50%, -50%)
      h2
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
      p
        --animate-duration: 1.7s
      button
        padding: 10px 35px
        background: $main-color
        font-weight: 600
        letter-spacing: 2.5px
        @include transition(all, 0.3s, ease-in-out)
        @media (max-width: 575.98px)
          padding: 10px 20px
          letter-spacing: 2px
        @media (min-width: 576px) and (max-width: 767.98px)
          padding: 10px 20px
          letter-spacing: 2px
        &:hover
          background: darken($main-color,3%) !important
      .about_button
        background: rgba(255, 255, 255, 0.3) !important
      .scroll-down
        margin-top: 10%
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
  props:['title','title2','image1','image2']
}
</script>
