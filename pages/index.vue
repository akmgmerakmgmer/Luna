<template>
  <div>
    <nav-1></nav-1>
    <carousel-1 title="Creative and Profit" title2="Modern" image1="agency1.jpg" image2="slider1.jpg"></carousel-1>
    <Heading1 headings='Look what we do best' paragraphs='Look at our projects. We presented just a part of works. Our team of experts has competences of different branches and specializations.' id="features" />
    <mixit-1></mixit-1>
    <grid-1></grid-1>
    <Heading1 headings='Our magic team.' paragraphs='Our team of experts has competences of different branches and specializations.' />
    <grid-2></grid-2>
    <div class="bg-light pt-5 pb-16">
      <Heading1 headings='Clients about us..' paragraphs='Our team of experts has competences of different branches and specializations.' />
      <slider-1></slider-1>
    </div>
    <slider-2></slider-2>
    <contact-1></contact-1>
    <footer-1></footer-1>
    <footer-2></footer-2>
  </div>
</template>

<script>
import Nav1 from '../components/Navbars/Navbar1.vue'
import Carousel1 from '../components/Carousels/Carousel1.vue'
import Heading1 from '~/components/Headings/Heading1.vue'
import Mixit1 from '~/components/Mixit/Mixit1.vue'
import Grid1 from '~/components/Grids/Grid1.vue'
import Grid2 from '~/components/Grids/Grid2.vue'
import Slider1 from '~/components/Sliders/Slider1.vue'
import Slider2 from '~/components/Sliders/Slider2.vue'
import Contact1 from '~/components/Contacts/Contact1.vue'
import Footer1 from '~/components/Footers/Footer1.vue'
import Footer2 from '~/components/Footers/Footer2.vue'
export default {
  components:{
    Nav1,
    Carousel1,
    Heading1,
    Mixit1,
    Grid1,
    Grid2,
    Slider1,
    Slider2,
    Contact1,
    Footer1,
    Footer2
  }
}
</script>
<style lang="sass" scoped>
.background2
  background: #1C1C1C
  color: white
.background1
  background: #222222
  color: white
.features
  margin-top: 12px
  background: #222222
  color: white
</style>
