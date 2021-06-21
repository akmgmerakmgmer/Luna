<template>
  <v-app dark class="background-main">
    <v-main>
      <loading-1>
        <nuxt />
      </loading-1>
    </v-main>
  </v-app>
</template>
<style lang="sass">
@import "~/assets/style.sass"
</style>

<script>
import Loading1 from '~/components/Loadings/loading1.vue'
export default {
  components:{
    Loading1
  }
}
</script>
