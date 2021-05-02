<template>
  <div>
    <nav-1></nav-1>
    <carousel-1 title="Let's Contact." title2="Be Unique." image1="bg-video1.jpg" image2="bg-portfolio.jpg"></carousel-1>
    <Heading1 headings='Look what we do best' paragraphs='Look at our projects. We presented just a part of works. Our team of experts has competences of different branches and specializations.' id="features" />
    <grid-3></grid-3>
    <grid-1-light></grid-1-light>
    <Heading1 headings='Our magic team.' paragraphs='Our team of experts has competences of different branches and specializations.' />
    <grid-2></grid-2>
    <div class="bg-light pt-5 pb-16">
      <Heading1 headings='Clients about us..' paragraphs='Our team of experts has competences of different branches and specializations.' />
      <slider-1></slider-1>
    </div>
    <contact-2></contact-2>
    <footer-1></footer-1>
    <footer-2></footer-2>
  </div>
</template>

<script>
import Nav1 from '../components/Navbars/Navbar1.vue'
import Carousel1 from '../components/Carousels/Carousel1.vue'
import Heading1 from '~/components/Headings/Heading1.vue'
import Grid1Light from '~/components/Grids/Grid1Light.vue'
import Grid2 from '~/components/Grids/Grid2.vue'
import Slider1 from '~/components/Sliders/Slider1.vue'
import Contact2 from '~/components/Contacts/Contact2.vue'
import Footer1 from '~/components/Footers/Footer1.vue'
import Footer2 from '~/components/Footers/Footer2.vue'
import Grid3 from '~/components/Grids/Grid3.vue'
export default {
  components:{
    Nav1,
    Carousel1,
    Heading1,
    Grid1Light,
    Grid2,
    Slider1,
    Contact2,
    Footer1,
    Footer2,
    Grid3
  }
}
</script>
<style lang="sass" scoped>
@import "~/assets/style.sass"
.background2
  background: #1C1C1C
  color: white
.background1
  background: #222222
  color: white
.features
  background: #F7F7F7
  color: rgba(0, 0, 0, 0.75)
</style>
