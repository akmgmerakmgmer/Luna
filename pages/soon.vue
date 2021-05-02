<template>
  <div>
    <nav-1></nav-1>
    <carousel-2 title="Comming Soon..." image="bg-comming-soon.jpg"></carousel-2>
    <footer-1 id="features"></footer-1>
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
import Carousel2 from '../components/Carousels/Carousel2.vue'
import Footer1 from '~/components/Footers/Footer1.vue'
import Footer2 from '~/components/Footers/Footer2.vue'
export default {
  components:{
    Nav1,
    Carousel2,
    Footer1,
    Footer2,
  }
}
</script>
