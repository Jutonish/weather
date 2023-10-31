<template>
    <section class="section-bottom">
      <div class="block-bottom">
        <div class="block-bottom-inner">
          <div class="block-bottom-pic pic-coords"></div>
          <img class="img" src="/src/assets/img/compass.png" alt="">
          <div class="block-bottom-texts">
            <div class="block-bottom-text-block">
              <div class="block-bottom-text-block-title">Longitude: {{ coord?.lon }}</div>
              <div class="block-bottom-text-block-desc">
                Longitude measures distance east or west of the prime meridian.
              </div>
            </div>
            <div class="block-bottom-text-block">
              <div class="block-bottom-text-block-title">Latitude: {{ coord?.lat }}</div>
              <div class="block-bottom-text-block-desc">
                Latitude lines start at the equator (0 degrees latitude) and run
                east and west, parallel to the equator.
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
</template>

<script setup>
const props = defineProps({
  coord: {
    type: Object,
    required: true,
  }
})
</script>

<style lang="sass" scoped>
@import '../assets/style/main.sass'

.section-bottom
  background: url('/src/assets/img/gradient-4.jpg') no-repeat 0% 0%
  background-size: cover
  border-radius: 25px
  padding: 28px 16px 16px
  width: 50%
  margin-top: 16px
  margin-right: 20px
  color: $white
  @media (max-width: 767px)
    width: 100%
.block-bottom-inner
  display: flex
  align-items: center
.img
  width: 120px
  height: 120px
  margin-right: 10px
.block
  &-bottom
    &-text
      &-block
        &-title
          font-size: 20px
          padding-bottom: 10px
        &-desc
          font-size: 15px
          color: #8f96a3
</style>