<template>
  <div>
    <nav-1></nav-1>
    <carousel-2 title="Welcome to our digital world." image="startup.jpg"></carousel-2>
    <heading-2 h2='We create own history.' p='In efforts to expand our horizons, we welcome every investment-minded individual to join us in the Condotel Investment Opportunity.You can also freely advertise with us, exchange links.' id="features"></heading-2>
    <grid-1-light></grid-1-light>
    <grid-4></grid-4>
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
import Carousel2 from '../components/Carousels/Carousel2.vue'
import Heading1 from '~/components/Headings/Heading1.vue'
import Heading2 from '~/components/Headings/Heading2.vue'
import Mixit1 from '~/components/Mixit/Mixit1.vue'
import Grid1Light from '~/components/Grids/Grid1Light.vue'
import Grid4 from '~/components/Grids/Grid4.vue'
import Slider1 from '~/components/Sliders/Slider1.vue'
import Slider2 from '~/components/Sliders/Slider2.vue'
import Contact1 from '~/components/Contacts/Contact1.vue'
import Footer1 from '~/components/Footers/Footer1.vue'
import Footer2 from '~/components/Footers/Footer2.vue'
export default {
  components:{
    Nav1,
    Carousel2,
    Heading1,
    Heading2,
    Mixit1,
    Grid1Light,
    Grid4,
    Slider1,
    Slider2,
    Contact1,
    Footer1,
    Footer2
  }
}
</script>
<style lang="sass" scoped>
@import "~/assets/style.sass"
.background1
  background: #F7F7F7
  color: rgba(0, 0, 0, 0.75)
.background2
  background: #F2F2F2
  color: rgba(0, 0, 0, 0.75)
.features
  background: #F7F7F7
  color: rgba(0, 0, 0, 0.75)
</style>
