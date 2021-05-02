<template>
  <div class="background1 py-8" >
    <v-container>
      <v-row no-gutters>
        <v-col sm="6" md="4" xs="12" cols="12">
          <h4 class="font-weight-bold">Luna.</h4>
          <p>We create web products for the help and growth of your business.</p>
        </v-col>
        <v-col sm="6" md="4" xs="12" cols="12" class="mt-sm-0 mt-5">
          <ul class="ml-sm-16">
            <li v-for="link in links" :key="link" class="mb-5 ml-sm-16">{{link}}</li>
          </ul>
        </v-col>
        <v-col sm="6" md="4" xs="12" cols="12" class="mt-sm-0 mt-5">
          <div class="ml-md-16">
            <span>+8 800 555 35 35</span>
            <p class="mt-3">info@virgo.com</p>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<style lang="sass" scoped>
@import "~/assets/style.sass"
.background1
  ul
    li
      @include transition(all, 0.3s, ease-in-out)
      &:hover
        color: $main-color
</style>

<script>
export default {
  data(){
    return{
      links:['Home','Pages','Blog','Shortcodes','Contacts']
    }
  }
}
</script>
