<script setup>
const counter = ref(1);

const increment = () => {
  counter.value++;
};
const decrement = () => {
  if (counter.value <= 1) {
  } else {
    counter.value--;
  }
};
</script>

<template>
  <div class="favorites__counter-controls">
    <button class="favorites__counter-button" @click="decrement">
      <UiIconMinus></UiIconMinus>
    </button>
    <span class="favorites__counter-value">{{ counter }}</span>
    <button class="favorites__counter-button" @click="increment">
      <UiIconPlus></UiIconPlus>
    </button>
  </div>
</template>

<style lang="scss" scoped>
.favorites__counter {
  display: flex;
  padding: 10px;
  justify-content: center;
  align-items: center;
  gap: 10px;
  max-width: 80px;
  &-button {
    cursor: pointer;
    background-color: white;
  }
  &-controls {
    max-width: 143px;
    flex-grow: 1;
    border: 1px solid #d9d9d9;
    color: #000;
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 600;
    line-height: 90%;
    display: flex;
    justify-content: space-between;
    padding: 11px;
    background: #fff;
    align-items: center;
  }
}
</style>
