<template>
  <div :class="overflow">
    <div id="loading" :class="loading">
      <img src="~/assets/images/vectorpaint.svg" alt="Loading" />
    </div>
    <a href="#" id="top"><i class="fa fa-arrow-up fa-2x" aria-hidden="true"></i></a>
    <slot></slot>
  </div>
</template>

<style lang="sass" scoped>
@import "~/assets/style.sass"
.loading-fixed
  overflow: hidden !important
  max-height: 100vh
.d-none
  display: none
.opacity
  opacity: 1
.no-opacity
  opacity: 0
.no-zindex
  z-index: -1
.zindex
  z-index: 999999999999999
#loading
  width: 100vw
  height: 100vh
  position: fixed
  background-color: #222222
  top: 0
  left: 0
  display: flex
  justify-content: center
  align-items: center
  @include transition(all, 0.2s, ease-in-out)
  img
    width: 160px
    height: 150px
#top
  position: fixed
  bottom: 20px
  right: 20px
  z-index: 2
  padding: 12px 15px
  cursor: pointer
  background: $secondery-color
  border-radius: 10px
  transition: 0.3s
  opacity: 0
  @include transition(all, 0.3s, ease-in-out)
  i
    color: white
  &:hover
    background: $main-color
</style>

<script>
export default {
  data(){
    return{
      loading:'opacity zindex',
      overflow:'loading-fixed'
    }
  },
  methods:{
    arrow () {
      if(window.scrollY>100){
        document.getElementById('top').style.opacity=1
      }else{
        document.getElementById('top').style.opacity=0

      }
    }
  },
  mounted(){
    window.addEventListener("scroll", this.arrow)
      setTimeout(() => {
        this.loading="no-opacity no-zindex"
        this.overflow=""
      },4000)
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.arrow)
  },
}
</script>
