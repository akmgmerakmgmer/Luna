<template>
  <div>
    <nav-1></nav-1>
    <carousel-2 title="Let's Get Closer." image="bg-about-2.jpg"></carousel-2>
    <grid-4 id="features"></grid-4>
    <grid-3></grid-3>
    <slider-2></slider-2>
    <contact-1></contact-1>
    <footer-1></footer-1>
    <footer-2></footer-2>
  </div>
</template>
<style lang="sass">
.background1
  background: #F7F7F7
  color: rgba(0, 0, 0, 0.75)
.background2
  background: #F2F2F2
  color: rgba(0, 0, 0, 0.75)
</style>
<script>
import Nav1 from '../components/Navbars/Navbar1.vue'
import Carousel2 from '../components/Carousels/Carousel2.vue'
import Grid3 from '~/components/Grids/Grid3.vue'
import Grid4 from '~/components/Grids/Grid4.vue'
import Slider2 from '~/components/Sliders/Slider2.vue'
import Contact1 from '~/components/Contacts/Contact1.vue'
import Footer1 from '~/components/Footers/Footer1.vue'
import Footer2 from '~/components/Footers/Footer2.vue'
export default {
  components:{
    Nav1,
    Carousel2,
    Grid3,
    Grid4,
    Slider2,
    Contact1,
    Footer1,
    Footer2
  }
}
</script>

