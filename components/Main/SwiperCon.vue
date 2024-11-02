<script setup lang="ts">
const swiper = useSwiper();
</script>

<template>
  <button @click="swiper.slidePrev()"><UiButtonArrowsButtonLeft /></button>
  <button @click="swiper.slideNext()"><UiButtonArrowsButtonRight /></button>
</template>
