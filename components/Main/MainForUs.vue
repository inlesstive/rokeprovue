<script setup>

</script>


<template>
  <section class="mainforus container">
    <Swiper 
    :slides-per-view="2"
    :loop="true"
    :space-between="50"
    >
      <SwiperSlide v-for="slide in 10" :key="slide">
        <div class="slide">{{ slide }}</div>
      </SwiperSlide>
      <MainSwiperCon></MainSwiperCon>
    </Swiper>
  </section>
</template>


<style lang="scss" scoped>

.mainforus {
  padding-top: 150px;
  padding-bottom: 150px;
}
.slide {
  height: 500px;
  background-color: #ddd;
}
</style>