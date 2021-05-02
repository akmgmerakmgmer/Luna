<template>
  <div class="text-center pt-16 pb-md-5 pb-16">
    <h2>{{headings}}</h2>
    <p class="paragraphs1">{{paragraphs}}</p>
  </div>
</template>
<style lang="sass" scoped>
h2
  font-size: 38px
  font-weight: 700
  color: rgba(0, 0, 0, 0.78)
  @media (max-width: 575.98px)
    font-size: 30px
  @media (min-width: 576px) and (max-width: 767.98px)
    font-size: 32px
  @media (min-width: 768px) and (max-width: 991.98px)
    font-size: 34px
  @media (min-width: 992px) and (max-width: 1199.98px)
    font-size: 36px
p
  font-family: lora,serif
  margin-left: 25%
  margin-right: 25%
  color: rgba(0, 0, 0, 0.78)
  letter-spacing: 1.5px
  @media (max-width: 575.98px)
    margin-left: 5%
    margin-right: 5%
  @media (min-width: 576px) and (max-width: 767.98px)
    margin-left: 15%
    margin-right: 15%
  @media (min-width: 768px) and (max-width: 991.98px)
    margin-left: 20%
    margin-right: 20%
</style>
<script>
export default {
  props:['headings','paragraphs'],
}
</script>
