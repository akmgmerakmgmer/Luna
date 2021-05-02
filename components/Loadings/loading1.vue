<template>
  <div>
    <div id="loading" class="zindex">
      <img src="~/assets/images/vectorpaint.svg" alt="Loading" />
    </div>
    <a href="#" id="top"><i class="fa fa-arrow-up fa-2x" aria-hidden="true"></i></a>
  </div>
</template>

<style lang="sass" scoped>
@import "~/assets/style.sass"
.zindex
  z-index: 999999999999999
#loading
  width: 100%
  height: 100vh
  position: fixed
  background-color: #222222
  top: 0
  left: 0
  display: flex
  justify-content: center
  align-items: center
  opacity: 1
  @include transition(all, 0.3s, ease-in-out)
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
        document.getElementById('loading').style.opacity=0
      },3000)
      setTimeout(() => {
        document.getElementById('loading').classList.remove('zindex')
      },3500)
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.arrow)
  },
}
</script>
