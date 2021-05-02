<template>
  <div>
    <div class="row pa-0">
      <div class="col-md-4 position-relative pa-0 content-height">
        <img src="~/assets/images/2-480x580.jpg" alt="" class="h-100 w-100">
        <div class="position-absolute content-container text-white d-flex flex-column justify-content-center">
          <div class="mx-16">
            <p class="paragraphs8 font-weight-bold">Investment is a key to long-term wealth</p>
            <span class="d-block text-left">- Hector Bellerin</span>
            <span class="d-block text-left">CEO of Luna.</span>
          </div>
        </div>
      </div>
      <div class="col-md-8 content2 padding-x-100 py-16">
        <div class="my-md-16 my-8 ml-5 mr-16">
          <h2>We are Virgo and we solve business problems.</h2>
          <p class="paragraphs9">So many of us are demotivated to achieve anything. Such people are not enthusiastic about anything. They don’t want to work towards any goal. Nothing motivates them to work. Why many of us are not motivated? What is wrong?</p>
          <p class="paragraphs9">We think in different ways and our thinking is decided by many factors. Some are known and some are unknown. The known factors are – thinking, circumstances. early upbringing, living style, culture, family support, friends, own intelligence etc. Our thoughts and our mental makeup is also decided by many factors that are yet not known. Two persons of similar upbringing may be facing similar situation, but react in opposite ways? there are so many whys about the human mind that it is very difficult to determine about what may happen.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="sass" scoped>
@import "~/assets/style.sass"
img
  object-fit: cover
.content-height
  margin-top: 12px
  margin-bottom: 12px
.content-container
  font-family: lora,serif
  top: 0
  left: 0
  background: rgba($color:$main-color,$alpha:0.8)
  height: 100%
  width: 100%
  p
    line-height: 1.2
  span
    font-style: italic
.content2
  h2
    font-size: 36px
    font-weight: 700
    color: rgba(0, 0, 0, 0.78)
    @media (max-width: 575.98px)
      font-size: 28px
    @media (min-width: 576px) and (max-width: 767.98px)
      font-size: 30px
    @media (min-width: 768px) and (max-width: 991.98px)
      font-size: 32px
    @media (min-width: 992px) and (max-width: 1199.98px)
      font-size: 34px
</style>
