<template>
  <div class="my-16 mx-md-16 mx-8">
    <h2 class="text-center font-weight-bold mb-5">Main <span>features</span> of my design.</h2>
    <div class="row text-center mt-10">
        <div class="col-lg-4 col-md-6 main6-divisions" v-for="service in services" :key="service.id">
            <div class="hvr-underline-from-center">
                <i :class="service.icon" aria-hidden="true"></i>
                <h5 class="paragraphs1">{{service.text}}</h5>
            </div>
        </div>
    </div>
  </div>
</template>


<style lang="sass" scoped>
@import "~/assets/style.sass"
h2
    font-weight: 600
    font-size: 38px
    margin-top: 50px
    color: rgba(0, 0, 0, 0.78)
    @media (max-width: 575.98px)
      font-size: 28px
    @media (min-width: 576px) and (max-width: 767.98px)
      font-size: 32px
    @media (min-width: 768px) and (max-width: 991.98px)
      font-size: 36px

    span
        display: inline-block
        position: relative
    span::before
      position: absolute
      content: ""
      left: 0px
      right: 4px
      height: 5px
      bottom: 3px
      background-color: $main-color
.main6-divisions
    .hvr-underline-from-center:before
      background: $main-color
      transition: 0.6s
    div
        border: 1px solid #e4e4e4
        width: 100%
        padding: 75px 20px
        border-radius: 10px
        h5
            margin-top: 20px
            font-weight: 400
            letter-spacing: 1.2px
            color: rgba(0, 0, 0, 0.8)
        i
            color: $main-color
            font-size: 40px
</style>

<script>
export default {
  data(){
    return{
      services:[
        {
          icon:"fa fa-desktop",
          text:"Fully Responsive"
        },
        {
          icon:"fa fa-picture-o",
          text:"Unlimited Color Skins"
        },
        {
          icon:"fa fa-tasks",
          text:"Fast Loading Speed"
        },
        {
          icon:"fa fa-cogs",
          text:"Easy Customize"
        },
        {
          icon:"fa fa-google",
          text:"Google Fonts"
        },
        {
          icon:"fa fa-compass",
          text:"Cross Browser"
        },
        {
          icon:"fa fa-code",
          text:"Clean Code"
        },
        {
          icon:"fa fa-refresh",
          text:"Awesome Animation"
        },
        {
          icon:"fa fa-user",
          text:"Contact Form"
        },
      ],
    }
  }
}
</script>
