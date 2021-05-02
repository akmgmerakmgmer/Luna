<template>
  <div class="background2 py-2">
    <v-container>
      <div class="d-flex flex-sm-row flex-column justify-space-between">
        <div class="paragraphs3">
          <i class="fa fa-facebook icons" aria-hidden="true"></i>
          <i class="fa fa-twitter icons ml-6" aria-hidden="true"></i>
          <i class="fa fa-instagram icons ml-6" aria-hidden="true"></i>
          <i class="fa fa-linkedin icons ml-6" aria-hidden="true"></i>
        </div>
        <div class="mt-3 mt-sm-0">
          <p class="pa-0 ma-0 paragraphs6 grey--text">© Copyright 2021 Luna. All Rights Reserved</p>
        </div>
      </div>
      </v-container>
  </div>
</template>

<style lang="sass" scoped>
@import "~/assets/style.sass"
.background2
  .icons
    cursor: pointer
    @include transition(all, 0.3s, ease-in-out)
    &:hover
      color: $main-color
</style>

