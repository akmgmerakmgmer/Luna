<template>
  <div>
    <div class="container-fluid">
      <div class="row">
        <div class="col-md-4 position-relative image-container">
          <img src="~/assets/images/portfolio3.jpg" alt="portfolios" class="w-100 h-100">
          <div class="position-absolute all-content text-center">
            <div class="white--text inner-content inner-content1">
              <h5 class="mb-5"><strong>Branding</strong></h5>
              <span>Stationary Design</span>
            </div>
          </div>
        </div>
        <div class="col-md-8 row">
          <div class="col-md-6 position-relative image-container">
            <img src="~/assets/images/5-637x465.jpg" alt="portfolios" class="w-100 h-100">
            <div class="position-absolute all-content text-center">
              <div class="white--text inner-content inner-content2">
                <h5 class="mb-5"><strong>Branding</strong></h5>
                <span>Stationary Design</span>
              </div>
            </div>
          </div>
          <div class="col-md-6 position-relative image-container">
            <img src="~/assets/images/portfolio4.jpg" class="w-100 h-100" alt="portfolios">
            <div class="position-absolute all-content text-center">
              <div class="white--text inner-content inner-content2">
                <h5 class="mb-5"><strong>Branding</strong></h5>
                <span>Stationary Design</span>
              </div>
            </div>
          </div>
          <div class="col-md-12 position-relative image-container">
            <img src="~/assets/images/1-1275x466.jpg" class="w-100 h-100" alt="portfolios">
            <div class="position-absolute all-content text-center">
              <div class="white--text inner-content inner-content3">
                <h5 class="mb-5"><strong>Branding</strong></h5>
                <span>Stationary Design</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="sass" scoped>
@import "~/assets/style.sass"

div
  margin: 0 !important
  padding: 0 !important
.image-container
  &:hover span
    @include animator(text-animation,0.3s,linear,0s,forwards)
  &:hover h5
    @include animator(text-animation,0.3s,linear,0s,forwards)
  &:hover>.all-content
    opacity: 1
  .all-content
    top: 0
    left: 0
    background: rgba($color:$main-color,$alpha:0.8)
    height: 100%
    width: 100%
    opacity: 0
    @include transition(all, 0.3s, ease-in-out)
    .inner-content3
      margin-top: 15% !important
    .inner-content2
      margin-top: 30% !important
    .inner-content1
      margin-top: 65% !important
    .inner-content
      h5
        color: white
        font-size: 32px
        @media (max-width: 575.98px)
          font-size: 22px
        @media (min-width: 576px) and (max-width: 767.98px)
          font-size: 24px
        @media (min-width: 768px) and (max-width: 991.98px)
          font-size: 26px
</style>
