<template>
  <div class="features">
    <div class="container">
      <div class="row padding-y-100 mx-md-0 mx-1">
        <div v-for="feature in features" :key="feature.id" :h4="feature.h4" :p="feature.p" class="col-md-6 col-lg-4 my-md-4 my-3">
          <i :class="feature.class" aria-hidden="true"></i>
          <h4 class=" my-4 text-uppercase">{{feature.h4}}</h4>
          <p class="paragraphs4">{{feature.p}}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="sass" scoped>
@import "~/assets/style.sass"
.features
  padding:0
  i
    color: $main-color
    font-size: 42px
  h4
    font-weight: 700
    letter-spacing: 5px
    font-size: 20px
    @media (max-width: 575.98px)
      font-size: 17px
    @media (min-width: 576px) and (max-width: 767.98px)
      font-size: 18px
    @media (min-width: 768px) and (max-width: 991.98px)
      font-size: 19px
  p
    color: #9A9A9A
    letter-spacing: 1.5px
    font-family: lora,serif
</style>

<script>
export default {
  data(){
    return{
       features:[
        {
          id:1,
          class:'fa fa-windows',
          h4:'Web Design',
          p:'Ever wondered how some graphic designers always manage to produce beautiful looking designs for their brochures, website designs'
        },
        {
          id:2,
          class:'fa fa-cog',
          h4:'MEDIA & CONTENT',
          p:'Ever wondered how some graphic designers always manage to produce beautiful looking designs for their brochures, website designs logo designs handful of more important things.'
        },
        {
          id:3,
          class:'fa fa-user-o',
          h4:'VIDEO PROD.',
          p:'Ever wondered how some graphic designers always manage to produce beautiful looking designs for their brochures, website designs'
        },
        {
          id:4,
          class:'fa fa-chrome',
          h4:'ADV. & PR',
          p:'Ever wondered how some graphic designers always manage to produce beautiful looking designs for their brochures, website designs'
        },
        {
          id:5,
          class:'fa fa-lightbulb-o',
          h4:'DEVELOPMENT',
          p:'Ever wondered how some graphic designers always manage to produce beautiful looking designs for their brochures, website designs logo designs handful of more important things.'
        },
        {
          id:6,
          class:'fa fa-pie-chart',
          h4:'STRATEGY',
          p:'Ever wondered how some graphic designers always manage to produce beautiful looking designs for their brochures, website designs'
        },
      ],
    }
  },
}
</script>
