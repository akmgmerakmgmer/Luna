<template>
  <div>
    <v-row no-gutters>
      <v-col v-for="info in infos" :key="info.id" cols="12" md="4">
        <div :class="info.class">
          <v-icon :class="info.iconClass">{{info.icon}}</v-icon>
          <span class="d-block mx-16 mt-7 text-center">{{info.paragraph}}</span>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<style lang="sass" scoped>
@import "~/assets/style.sass"
.padding-y-100-fixed
  padding-top: 100px
  padding-bottom: 100px
.icon-border2
  border: 1px solid rgba(0, 0, 0, 0.5)
  border-radius: 50%
  color: $main-color
.icon-border
  border: 1px solid rgba(255,255,255,0.15)
  border-radius: 50%
.main-background
  background: $main-color
.white-background
  background: #F7F7F7
  color: rgba(0, 0, 0, 0.7)
.black-background
  background: #222222
</style>

<script>
export default {
  data(){
    return{
      infos:[
        {
          icon:'mdi-cellphone',
          paragraph:'+8 800 555 35 35',
          class:'d-flex flex-column justify-content-center align-items-center main-background padding-y-100-fixed text-white h-100',
          iconClass:'icon-border pa-5 text-white text-h4'
        },
        {
          icon:'mdi-email',
          paragraph:'info@virgo.com',
          class:'d-flex flex-column justify-content-center align-items-center white-background padding-y-100-fixed h-100',
          iconClass:'icon-border2 pa-5 text-h4'
        },
        {
          icon:'mdi-map-marker',
          paragraph:'Beechwood Dr, Lawrence, NY 11559, USA',
          class:'d-flex flex-column justify-content-center align-items-center black-background padding-y-100-fixed text-white h-100',
          iconClass:'icon-border pa-5 text-white text-h4'
        },
      ]
    }
  }
}
</script>
