<template>
  <div>
    <nav-1></nav-1>
    <carousel-2 title="Let's Get Closer." image="bg-video1.jpg"></carousel-2>
    <grid-6 id="features"></grid-6>
    <contact-2></contact-2>
    <footer-1></footer-1>
    <footer-2></footer-2>
  </div>
</template>

<style lang="sass" scoped>
.background2
  background: #1C1C1C
  color: white
.background1
  background: #222222
  color: white
</style>

<script>
import Nav1 from '../components/Navbars/Navbar1.vue'
import Grid6 from '../components/Grids/Grid6'
import Carousel2 from '../components/Carousels/Carousel2.vue'
import Contact2 from '~/components/Contacts/Contact2.vue'
import Footer1 from '~/components/Footers/Footer1.vue'
import Footer2 from '~/components/Footers/Footer2.vue'
export default {
  components:{
    Nav1,
    Carousel2,
    Grid6,
    Contact2,
    Footer1,
    Footer2,
  }
}
</script>
