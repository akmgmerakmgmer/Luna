<template>
  <div>
    <v-row no-gutters class="pa-0 pt-16">
      <v-col
        v-for="image in images"
        :key="image.id"
        cols="12"
        lg="3"
        md="6"
      >
        <div class="image-container">
          <img :src="require('~/assets/images/'+image.img)" alt="Grids" class="w-100 h-100">
          <div class="image-content text-center">
            <div class="image-details">
              <h5 class="mb-10 white--text font-weight-normal"><strong>Jack Wilshere</strong></h5>
              <span class="white--text">SEO / Founder</span>
            </div>
            <div class="white--text">
                <i class="fa fa-facebook icons" aria-hidden="true"></i>
                <i class="fa fa-instagram icons ml-10" aria-hidden="true"></i>
                <i class="fa fa-twitter icons ml-10" aria-hidden="true"></i>
                <i class="fa fa-linkedin icons ml-10" aria-hidden="true"></i>
            </div>
          </div>
        </div>
      </v-col>
    </v-row>
  </div>
</template>
<style lang="sass" scoped>
@import "~/assets/style.sass"
.image-container
  position: relative
  display: flex
  align-items: center
  justify-content: center
  &:hover .image-details
    @include animator(text-animation,0.3s,linear,0s,forwards)
  &:hover>.image-content
    opacity: 1
  .image-content
    @include transition(all, 0.3s, ease-in-out)
    position: absolute
    top: -15%
    left: 0
    width: 90%
    height: 110%
    margin-left: 5%
    z-index: 1
    background: rgba($color:$main-color,$alpha:0.8)
    opacity: 0
    .image-details
      margin-top: 55% !important
    .icons
      cursor: pointer
      margin-top: 50%
      &:hover
        color: white !important
</style>

<script>
export default {
  data(){
    return{
      images:[
        {
          img:'1-480x580.jpg'
        },
        {
          img:'2-480x580.jpg'
        },
        {
          img:'3-480x580.jpg'
        },
        {
          img:'4-480x580.jpg'
        },
      ]
    }
  }
}
</script>
